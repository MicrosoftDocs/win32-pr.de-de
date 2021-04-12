---
description: Die Dateisystem Erkennung ist die Fähigkeit, Speichermedien zu erkennen, die ein gültiges Dateisystem-/volumenlayout enthalten, das noch nicht definiert wurde, aber die Medien können sich selbst durch das vorhanden sein der von Windows definierten Erkennungs Struktur identifizieren.
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: Abrufen von Informationen zur Datei System Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cafa9f1c7cf6cbbe11d434aff3db424a1cd0a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344289"
---
# <a name="obtaining-file-system-recognition-information"></a><span data-ttu-id="6543e-103">Abrufen von Informationen zur Datei System Erkennung</span><span class="sxs-lookup"><span data-stu-id="6543e-103">Obtaining File System Recognition Information</span></span>

<span data-ttu-id="6543e-104">Die [Dateisystem Erkennung](file-system-recognition.md) ist die Fähigkeit, Speichermedien zu erkennen, die ein gültiges Dateisystem-/volumenlayout enthalten, das noch nicht definiert wurde, aber die Medien können sich selbst durch das vorhanden sein der von Windows definierten Erkennungs Struktur identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6543e-104">[File system recognition](file-system-recognition.md) is the ability to recognize storage media that contain a valid file system/volume layout that has not been defined yet, but the media is able to identify itself through the presence of the recognition structure defined internally by Windows.</span></span>

<span data-ttu-id="6543e-105">Da kein vorhandenes Dateisystem ein neues Datenträger Layout erkennt, wird das Volume vom RAW-Dateisystem bereitgestellt, und es wird direkter Zugriff auf Blockebene bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6543e-105">Because no existing file system will recognize a new disk layout, the "RAW" file system will mount the volume and provide direct block level access.</span></span> <span data-ttu-id="6543e-106">Das "RAW"-Dateisystem, das in *Ntoskrnl* integriert ist, kann die Dateisystem-Erkennungs Struktur lesen und Anwendungen Zugriff auf solche Strukturen über die [**FSCTL \_ Query \_ file \_ System \_ Recognition**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)der Dateisystem Steuerung anfordern, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6543e-106">The "RAW" file system, incorporated in *NtosKrnl*, will have the ability to read the file system recognition structure and provide applications access to such structures through the file system control request [**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), shown in the following example.</span></span>


```C++
STDMETHODIMP CheckFileSystem(
    PCWSTR pcwszDrive
    ) 
{
    HRESULT hr = S_OK;
    HANDLE  hDisk = INVALID_HANDLE_VALUE;
    BOOL    fResult = FALSE;    
    ULONG   BytesReturned = 0;    
    FILE_SYSTEM_RECOGNITION_INFORMATION     FsRi = {0};
    
    //
    // Open the target, for example "\\.\C:"
    //
    wprintf( L"CreateFile on %s...", pcwszDrive );
    hDisk = CreateFile( pcwszDrive, 
                        FILE_READ_ATTRIBUTES|SYNCHRONIZE|FILE_TRAVERSE,                        
                        FILE_SHARE_READ|FILE_SHARE_WRITE,
                        NULL, OPEN_EXISTING, 0, NULL );    
    if( hDisk == INVALID_HANDLE_VALUE ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"CreateFile failed on %s, GLE = 0x%x\n", pcwszDrive, GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"\nPress Any Key to send down the FSCTL\n" );
    _getwch();

    //
    // Send down the FSCTL
    //
    wprintf( L"Calling DeviceIoControl( FSCTL_QUERY_FILE_SYSTEM_RECOGNITION ) " );
    
    fResult = DeviceIoControl( hDisk, 
                               FSCTL_QUERY_FILE_SYSTEM_RECOGNITION, 
                               NULL, 
                               0, 
                               &FsRi, 
                               sizeof(FsRi), 
                               &BytesReturned, 
                               NULL );
    if( !fResult ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"failed GLE = 0x%x\n", GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION returned success.\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION retrieved \"%S\".\n",
              FsRi.FileSystem );

exit:

    if( hDisk != INVALID_HANDLE_VALUE ) 
    {
        CloseHandle( hDisk );
        hDisk = INVALID_HANDLE_VALUE;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6543e-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6543e-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6543e-108">Datei System Erkennung</span><span class="sxs-lookup"><span data-stu-id="6543e-108">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="6543e-109">**Datei \_ System- \_ Erkennungs \_ Struktur**</span><span class="sxs-lookup"><span data-stu-id="6543e-109">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> <dt>

[<span data-ttu-id="6543e-110">**FSCTL- \_ Abfrage \_ Datei \_ System \_ Erkennung**</span><span class="sxs-lookup"><span data-stu-id="6543e-110">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
