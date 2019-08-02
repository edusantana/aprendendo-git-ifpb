require 'rake/clean'

directory 'tmp'

desc "Cria a página html"
task :html => ['tmp']do
  sh "claat export -o tmp/ guia-nord-hotels.md"

  puts "Criando conteúdo em tmp/"
  puts "Execute 'rake serve' para levantar servidor localmente"
end

task :default => [:html]

desc 'atualiza código gerado'
task :update do
  sh "claat update -o tmp/ guia-nord-hotels.md"
end

file 'tmp/guia-nord-hotels/index.html'

desc 'Serve localmente arquivo gerado'
task 'serve' do
  Dir.chdir('tmp/guia-nord-hotels') do
    sh "claat serve"
  end
end

desc 'Gera documentação em docs'
task :docs => ['tmp/guia-nord-hotels/index.html'] do
  FileUtils.cp_r 'tmp/guia-nord-hotels/.', 'docs'
end
