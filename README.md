# Kace VS Extension

Provides a button in VS to run the CleanTable.exe and then stop the debugger.

## Problem

On process teardown, if the processes page table doesn't match up with the memory manager has tracked, the system will bug check on `MEMORY MANAGEMENT`

This tool runs an executable that will restore the page table to a state that will pass the page table walks performed by the memory manager on Kace's teardown.
