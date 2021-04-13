---
title: Verwenden von Ressourcen
description: Dieser Abschnitt enthält Code, der sich auf Ressourcen Programmierungsaufgaben bezieht.
ms.assetid: 73678045-1518-46cd-ab55-5d272852ba73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c197cbec1e2ecf495f7a682d70311edc45c069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473092"
---
# <a name="using-resources"></a>Verwenden von Ressourcen

Dieser Abschnitt enthält Code Ausschnitte für die folgenden Aufgaben:

-   [Aktualisieren von Ressourcen](#updating-resources)
-   [Erstellen einer Ressourcen Liste](#creating-a-resource-list)

## <a name="updating-resources"></a>Aktualisieren von Ressourcen

Im folgenden Beispiel wird eine Dialogfeld Ressource mithilfe der folgenden Schritte aus einer ausführbaren Datei Hand.exe in eine andere Datei Foot.exe kopiert:

1.  Verwenden Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion, um die ausführbare Datei Hand.exe zu laden.
2.  Verwenden Sie die Funktionen [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) und [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) , um die Dialogfeld Ressource zu suchen und zu laden.
3.  Verwenden Sie die [**LockResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource) -Funktion, um einen Zeiger auf die Ressourcen Daten des Dialog Felds abzurufen.
4.  Verwenden Sie die [**beginupdateresource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) -Funktion, um ein Aktualisierungs Handle zum Foot.exe zu öffnen.
5.  Verwenden Sie die [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) -Funktion, um die Dialogfeld Ressource von Hand.exe in Foot.exe zu kopieren.
6.  Verwenden Sie die [**endupdateresource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) -Funktion, um das Update abzuschließen.

Der folgende Code implementiert diese Schritte.

**Sicherheitswarnung:** Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird. Informationen zum ordnungsgemäßen Laden von DLLs mit unterschiedlichen Versionen von Windows finden Sie in der Dokumentation zu **LoadLibrary** .


```C++
HGLOBAL hResLoad;   // handle to loaded resource
HMODULE hExe;       // handle to existing .EXE file
HRSRC hRes;         // handle/ptr. to res. info. in hExe
HANDLE hUpdateRes;  // update resource handle
LPVOID lpResLock;   // pointer to resource data
BOOL result;
#define IDD_HAND_ABOUTBOX   103
#define IDD_FOOT_ABOUTBOX   110

// Load the .EXE file that contains the dialog box you want to copy.
hExe = LoadLibrary(TEXT("hand.exe"));
if (hExe == NULL)
{
    ErrorHandler(TEXT("Could not load exe."));
    return;
}

// Locate the dialog box resource in the .EXE file.
hRes = FindResource(hExe, MAKEINTRESOURCE(IDD_HAND_ABOUTBOX), RT_DIALOG);
if (hRes == NULL)
{
    ErrorHandler(TEXT("Could not locate dialog box."));
    return;
}

// Load the dialog box into global memory.
hResLoad = LoadResource(hExe, hRes);
if (hResLoad == NULL)
{
    ErrorHandler(TEXT("Could not load dialog box."));
    return;
}

// Lock the dialog box into global memory.
lpResLock = LockResource(hResLoad);
if (lpResLock == NULL)
{
    ErrorHandler(TEXT("Could not lock dialog box."));
    return;
}

// Open the file to which you want to add the dialog box resource.
hUpdateRes = BeginUpdateResource(TEXT("foot.exe"), FALSE);
if (hUpdateRes == NULL)
{
    ErrorHandler(TEXT("Could not open file for writing."));
    return;
}

// Add the dialog box resource to the update list.
result = UpdateResource(hUpdateRes,    // update resource handle
    RT_DIALOG,                         // change dialog box resource
    MAKEINTRESOURCE(IDD_FOOT_ABOUTBOX),         // dialog box id
    MAKELANGID(LANG_NEUTRAL, SUBLANG_NEUTRAL),  // neutral language
    lpResLock,                         // ptr to resource info
    SizeofResource(hExe, hRes));       // size of resource info

if (result == FALSE)
{
    ErrorHandler(TEXT("Could not add resource."));
    return;
}

// Write changes to FOOT.EXE and then close it.
if (!EndUpdateResource(hUpdateRes, FALSE))
{
    ErrorHandler(TEXT("Could not write changes to file."));
    return;
}

// Clean up.
if (!FreeLibrary(hExe))
{
    ErrorHandler(TEXT("Could not free executable."));
    return;
}
```



## <a name="creating-a-resource-list"></a>Erstellen einer Ressourcen Liste

Im folgenden Beispiel wird eine Liste aller Ressourcen in der Hand.exe-Datei erstellt. Die Liste wird in die Resinfo.txt Datei geschrieben.

Im Code wird veranschaulicht, wie die ausführbare Datei geladen, eine Datei erstellt wird, in der Ressourcen Informationen geschrieben werden, und die [**enumresourcetypes**](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa) -Funktion aufgerufen wird, um jeden Ressourcentyp im Modul an die Anwendungs definierte Rückruffunktion zu senden `EnumTypesFunc` . Weitere Informationen zu Rückruf Funktionen dieses Typs finden Sie unter [*enumrestypproc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca) . Diese Rückruffunktion verwendet die [**enumresourcenames**](/windows/desktop/api/Winbase/nf-winbase-enumresourcenamesa) -Funktion, um den Namen der einzelnen Ressourcen innerhalb des angegebenen Typs an eine andere Anwendungs definierte Rückruffunktion zu übergeben `EnumNamesFunc` . Weitere Informationen zu Rückruf Funktionen dieses Typs finden Sie unter [*enumresnameproc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca) . `EnumNamesFunc` verwendet die [**enumresourcelanguages**](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa) -Funktion, um die Sprache jeder Ressource des angegebenen Typs und namens an eine dritte Rückruffunktion () zu übergeben `EnumLangsFunc` . Weitere Informationen zu Rückruf Funktionen dieses Typs finden Sie unter [*enumreslangproc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)) . `EnumLangsFunc` schreibt Informationen über die Ressource des angegebenen Typs, des angegebenen Namens und der angegebenen Sprache in die Resinfo.txt Datei.

Beachten Sie, dass der *lpsztype* in [*enumrestypeer proc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca) entweder eine Ressourcen-ID oder ein Zeiger auf eine Zeichenfolge (die eine Ressourcen-ID oder einen Typnamen enthält) ist. " *lpsztype* " und " *lpszname* " in " [*enumresnameproc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca) " und " [*enumreslangproc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)) " ähneln einander. Um eine aufgelistete Ressource zu laden, müssen Sie einfach die entsprechende Funktion aufzurufen. Wenn beispielsweise eine Menü Ressource (**RT- \_ Menü**) aufgezählt wurde, übergeben Sie *lpszname* an [**loadmenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua). Übergeben Sie für benutzerdefinierte Ressourcen " *lpsztype* " und " *lpszname* " an [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea).

Der Code für die [Update Ressourcen](#updating-resources) folgt einem ähnlichen Muster für eine Dialogfeld Ressource.

**Sicherheitswarnung:** Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird. Informationen zum ordnungsgemäßen Laden von DLLs mit unterschiedlichen Versionen von Windows finden Sie in der Dokumentation zu **LoadLibrary** .


```C++
HANDLE g_hFile;   // global handle to resource info file
// Declare callback functions.
BOOL EnumTypesFunc(
       HMODULE hModule,
       LPTSTR lpType,
       LONG lParam);
   
BOOL EnumNamesFunc(
       HMODULE hModule,
       LPCTSTR lpType,
       LPTSTR lpName,
       LONG lParam);
   
BOOL EnumLangsFunc(
       HMODULE hModule,
       LPCTSTR lpType,
       LPCTSTR lpName,
       WORD wLang,
       LONG lParam);
```




```C++
HMODULE hExe;        // handle to .EXE file
TCHAR szBuffer[80];  // print buffer for info file
DWORD cbWritten;     // number of bytes written to resource info file
size_t cbString;     // length of string in szBuffer
HRESULT hResult;

// Load the .EXE whose resources you want to list.
hExe = LoadLibrary(TEXT("hand.exe"));
if (hExe == NULL)
{
    // Add code to fail as securely as possible.
    return;
}

// Create a file to contain the resource info.
g_hFile = CreateFile(TEXT("resinfo.txt"),   // name of file
    GENERIC_READ | GENERIC_WRITE,      // access mode
    0,                                 // share mode
    (LPSECURITY_ATTRIBUTES) NULL,      // default security
    CREATE_ALWAYS,                     // create flags
    FILE_ATTRIBUTE_NORMAL,             // file attributes
    (HANDLE) NULL);                    // no template
if (g_hFile == INVALID_HANDLE_VALUE)
{
    ErrorHandler(TEXT("Could not open file."));
    return;
}

// Find all of the loaded file's resources.
hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR),
    TEXT("The file contains the following resources:\r\n\r\n"));
if (FAILED(hResult))
{
    // Add code to fail as securely as possible.
    return;
}

hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
if (FAILED(hResult))
{
    // Add code to fail as securely as possible.
    return;
}

WriteFile(g_hFile,       // file to hold resource info
    szBuffer,            // what to write to the file
    (DWORD) cbString,    // number of bytes in szBuffer
    &cbWritten,          // number of bytes written
    NULL);               // no overlapped I/O

EnumResourceTypes(hExe,              // module handle
    (ENUMRESTYPEPROC)EnumTypesFunc,  // callback function
    0);                              // extra parameter

// Unload the executable file whose resources were
// enumerated and close the file created to contain
// the resource information.
FreeLibrary(hExe);
CloseHandle(g_hFile);
```




```C++
//    FUNCTION: EnumTypesFunc(HANDLE, LPSTR, LONG)
//
//    PURPOSE:  Resource type callback
BOOL EnumTypesFunc(
        HMODULE hModule,  // module handle
        LPTSTR lpType,    // address of resource type
        LONG lParam)      // extra parameter, could be
                          // used for error checking
{
    TCHAR szBuffer[80];  // print buffer for info file
    DWORD cbWritten;     // number of bytes written to resource info file
    size_t cbString;
    HRESULT hResult;

    // Write the resource type to a resource information file.
    // The type may be a string or an unsigned decimal
    // integer, so test before printing.
    if (!IS_INTRESOURCE(lpType))
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("Type: %s\r\n"), lpType);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }
    else
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("Type: %u\r\n"), (USHORT)lpType);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    WriteFile(g_hFile, szBuffer, (DWORD) cbString, &cbWritten, NULL);
    // Find the names of all resources of type lpType.
    EnumResourceNames(hModule,
        lpType,
        (ENUMRESNAMEPROC)EnumNamesFunc,
        0);

    return TRUE;
}

//    FUNCTION: EnumNamesFunc(HANDLE, LPSTR, LPSTR, LONG)
//
//    PURPOSE:  Resource name callback
BOOL EnumNamesFunc(
        HMODULE hModule,  // module handle
        LPCTSTR lpType,   // address of resource type
        LPTSTR lpName,    // address of resource name
        LONG lParam)      // extra parameter, could be
                          // used for error checking
{
    TCHAR szBuffer[80];  // print buffer for info file
    DWORD cbWritten;     // number of bytes written to resource info file
    size_t cbString;
    HRESULT hResult;

    // Write the resource name to a resource information file.
    // The name may be a string or an unsigned decimal
    // integer, so test before printing.
    if (!IS_INTRESOURCE(lpName))
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("\tName: %s\r\n"), lpName);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }
    else
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("\tName: %u\r\n"), (USHORT)lpName);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }
   
    WriteFile(g_hFile, szBuffer, (DWORD) cbString, &cbWritten, NULL);
    // Find the languages of all resources of type
    // lpType and name lpName.
    EnumResourceLanguages(hModule,
        lpType,
        lpName,
        (ENUMRESLANGPROC)EnumLangsFunc,
        0);

    return TRUE;
}

//    FUNCTION: EnumLangsFunc(HANDLE, LPSTR, LPSTR, WORD, LONG)
//
//    PURPOSE:  Resource language callback
BOOL EnumLangsFunc(
        HMODULE hModule, // module handle
        LPCTSTR lpType,  // address of resource type
        LPCTSTR lpName,  // address of resource name
        WORD wLang,      // resource language
        LONG lParam)     // extra parameter, could be
                         // used for error checking
{
    HRSRC hResInfo;
    TCHAR szBuffer[80];  // print buffer for info file
    DWORD cbWritten;     // number of bytes written to resource info file
    size_t cbString;
    HRESULT hResult;

    hResInfo = FindResourceEx(hModule, lpType, lpName, wLang);
    // Write the resource language to the resource information file.
    hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("\t\tLanguage: %u\r\n"), (USHORT) wLang);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    WriteFile(g_hFile, szBuffer, (DWORD) cbString, &cbWritten, NULL); 
    // Write the resource handle and size to buffer.
    hResult = StringCchPrintf(szBuffer,
        sizeof(szBuffer)/sizeof(TCHAR),
        TEXT("\t\thResInfo == %lx,  Size == %lu\r\n\r\n"),
        hResInfo,
        SizeofResource(hModule, hResInfo));
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    WriteFile(g_hFile, szBuffer, (DWORD)cbString, &cbWritten, NULL);
    return TRUE;
}
```



 

 