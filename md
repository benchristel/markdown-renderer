#!/usr/bin/env ruby

require "redcarpet"

renderer = Redcarpet::Markdown.new(
  Redcarpet::Render::HTML.new(
    with_toc_data: true,
  ),
  tables: true,
  no_intra_emphasis: true,
)

STDOUT.write renderer.render(STDIN.read)
