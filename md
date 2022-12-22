#!/usr/bin/env ruby

require "redcarpet"

renderer = Redcarpet::Markdown.new(
  Redcarpet::Render::HTML,
  tables: true,
  no_intra_emphasis: true,
)

STDOUT.write renderer.render(STDIN.read)
