# Kace VS Extension

## Usage

Use `Tools->Invoke CleanTable` while debugging to avoid BSOD.

![UsageImage](https://i.imgur.com/Pczvfe4.png)

## About

Provides a button in VS to run `CleanTable.exe` and then stop debugging.  When Kace is being debugged and the page table's been modified, use this method to stop debugging safely avoiding a BSOD.

## Problem

On process teardown, if the processes page table doesn't match up with the memory manager has tracked, the system will bug check on `MEMORY MANAGEMENT`

This tool runs an executable that will restore the page table to a state that will pass the page table walks performed by the memory manager on Kace's teardown.

![PTIntegrityFailure](https://i.imgur.com/tPpAeso.png)
