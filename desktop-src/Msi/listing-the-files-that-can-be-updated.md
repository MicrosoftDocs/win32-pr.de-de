---
description: Die MsiGetPatchFileList-Funktion und die PatchFiles-Eigenschaft des Installer-Objekts nehmen eine Liste von Windows Installer-Patches (MSP-Dateien) auf und geben eine Liste von Dateien zurück, die von den Patches aktualisiert werden können.
ms.assetid: cc2eb506-c1fc-4125-b98c-12221b918e23
title: Auflisten der Dateien, die aktualisiert werden können
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad76355c97d62d9c3f1282b5ebd66f54c5fef0f6f7359a41a35f2ebaee9a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945905"
---
# <a name="listing-the-files-that-can-be-updated"></a>Auflisten der Dateien, die aktualisiert werden können

Die [**MsiGetPatchFileList-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) und die [**PatchFiles-Eigenschaft**](installer-patchfiles.md) des [**Installer-Objekts**](installer-object.md) nehmen eine Liste Windows Installer-Patches (MSP-Dateien) auf und geben eine Liste von Dateien zurück, die von den Patches aktualisiert werden können. Die [**MsiGetPatchFileList-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) und [**die PatchFiles-Eigenschaft**](installer-patchfiles.md) sind ab Windows Installer 4.0 verfügbar.

## <a name="listing-files-that-can-be-updated"></a>Auflisten von Dateien, die aktualisiert werden können

Im folgenden Beispiel wird gezeigt, wie Sie die Anwendbarkeitsinformationen für eine Liste von Windows Installer-Patches (MSP-Dateien) mithilfe von [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)extrahieren. Die **MsiGetPatchFileList-Funktion** stellt den Produktcode für das Ziel der Patches und eine Liste von MSP-Dateien bereit, die durch Semikolons getrennt sind. Für dieses Beispiel muss Windows Installer 4.0 unter Windows Vista ausgeführt werden.


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")
#pragma comment(lib, "shell32.lib")

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles);

int __cdecl main()
{
    UINT uiRet = ERROR_SUCCESS;
    int argc;
    WCHAR** argv = CommandLineToArgvW(GetCommandLine(), &argc);
    
    MSIHANDLE *phFileListRec = NULL;
    DWORD dwcFiles = 0;
    WCHAR* szProductCode = argv[1];
    WCHAR* szPatchFileList = argv[2];
    if(ERROR_SUCCESS != (uiRet = MsiGetPatchFileList(szProductCode, szPatchFileList, &dwcFiles, &phFileListRec)))
    {
        printf("MsiGetPatchFileListW(%S, ...) Failed with:%d", szProductCode, uiRet);
        return uiRet;
    }
    
    DWORD cchBuf = 1;
    DWORD cchBufSize = 1;
    WCHAR* szBuf = new WCHAR[cchBufSize];
    if (!szBuf)
    {
        printf("Failed to allocate memory");
        CloseMsiHandles(phFileListRec, dwcFiles);
        return ERROR_OUTOFMEMORY;
    }
    memset(szBuf, 0, sizeof(WCHAR)*cchBufSize);
    
    for(unsigned int i = 0; i < dwcFiles; i++)
    {
        cchBuf = cchBufSize;
        while(ERROR_MORE_DATA == (uiRet = MsiRecordGetString(phFileListRec[i], 0, szBuf, &cchBuf)))
        {
            if (szBuf)
                delete[] szBuf;
            cchBufSize = ++cchBuf;
            szBuf = new WCHAR[cchBufSize];
            if (!szBuf)
            {
                printf("Failed to allocate memory");
                CloseMsiHandles(phFileListRec, dwcFiles);
                return ERROR_OUTOFMEMORY;
            }
        }
        
        if(uiRet != ERROR_SUCCESS)
        {
            printf("MsiRecordGetString(phFileListRec[%d] with %d", i, uiRet);
            CloseMsiHandles(phFileListRec, dwcFiles);
            if (szBuf)
                delete[] szBuf;
            return uiRet;
        }
        else
        {
            printf("File %d:%S\n", i, szBuf);
        }            
    }

    CloseMsiHandles(phFileListRec, dwcFiles);
    if (szBuf)
        delete[] szBuf;
    return 0;
}

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles)
{
    if (!phFileListRec)
        return;
    
    for (unsigned int i = 0; i < dwcFiles; i++)
    {
        if (phFileListRec[i])
            MsiCloseHandle(phFileListRec[i]);
    }    
}
//
```



Im folgenden Beispiel wird gezeigt, wie Sie die Anwendbarkeitsinformationen für eine Liste von Windows Installer-Patches (MSP-Dateien) mithilfe der [**PatchFiles-Eigenschaft**](installer-patchfiles.md) des [**Installerobjekts**](installer-object.md)extrahieren. Die **PatchFiles-Eigenschaft** stellt den Produktcode für das Ziel der Patches und eine Liste von MSP-Dateien bereit, die durch Semikolons getrennt sind. Für dieses Beispiel muss Windows Installer 4.0 unter Windows Vista ausgeführt werden.


```VB
Dim FileList
Dim installer : Set installer = Nothing
Dim argCount:argCount = Wscript.Arguments.Count

Set installer = Wscript.CreateObject("WindowsInstaller.Installer")

If (argCount > 0) Then
    sProdCode = Wscript.Arguments(0)
    sPatchPckgPath = Wscript.Arguments(1)
    Set FileList = installer.PatchFiles (sProdCode, sPatchPckgPath)
    For each File in FileList
           Wscript.Echo "Affected file: " & File
    Next
Else
    Usage
End If

Sub Usage
    Wscript.Echo "Windows Installer utility to list files updated by a patch for an installed product" &_
    vbNewLine & " 1st argument is the product code (GUID) of an installed product" &_
    vbNewLine & " 2nd argument is the list of patches" &_
    vbNewLine &_
    vbNewLine & "Copyright (C) Microsoft. All rights reserved."
    Wscript.Quit 1
End Sub
```



 

 



