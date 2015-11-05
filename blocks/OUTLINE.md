# Blocks in Drupal 8

## Block Overview

### What is a Block?

Blocks are contents that can be placed in regions.

### What is a Region?

Regions are the locations where you're blocks can be placed.

### Types of Blocks

#### Module-defined Blocks

Blocks that are defined in modules are cannot be changed.

#### Custom Blocks (or Database Blocks)

Blocks that are created through the admin interface. They can be modified and deleted.

## Implementation of Blocks in Drupal 7

### Hook System

Blocks are created using the following hooks:

* `hook_block_info()`
* `hook_block_configure()`
* `hook_block_save()`
* `hook_block_view()`

### Other Implementations

#### Boxes

* Configuration and not content.
* Can be exported.
* Option to edit in place for better UX.
* Block system uses the `variable` table for settings.

#### Bean

* Part of Drupal 8.
* Bean is "Block Entities Aren't Nodes".
* Allows creation of other "bundles".

## Block System in Drupal 8

* Uses Plugin API
* They are entities.

## Programmatically Creating Blocks in Drupal 7 vs Drupal 8
