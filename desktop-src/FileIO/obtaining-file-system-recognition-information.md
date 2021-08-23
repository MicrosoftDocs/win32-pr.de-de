---
description: Dateisystemerkennung ist die Fähigkeit, Speichermedien zu erkennen, die ein gültiges Dateisystem-/Volumelayout enthalten, das noch nicht definiert wurde, aber das Medium kann sich selbst identifizieren, indem die Erkennungsstruktur vorhanden ist, die intern durch Windows definiert wird.
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: Abrufen von Informationen zur Dateisystemerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c10b538f9e98ecab3f8f8f72784ef658c068f780388dc7b600be68b76380757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148506"
---
# <a name="obtaining-file-system-recognition-information"></a>Abrufen von Informationen zur Dateisystemerkennung

[Dateisystemerkennung](file-system-recognition.md) ist die Fähigkeit, Speichermedien zu erkennen, die ein gültiges Dateisystem-/Volumelayout enthalten, das noch nicht definiert wurde, aber das Medium kann sich selbst identifizieren, indem die Erkennungsstruktur vorhanden ist, die intern durch Windows definiert wird.

Da kein vorhandenes Dateisystem ein neues Datenträgerlayout erkennt, stellt das RAW-Dateisystem das Volume bereit und bietet direkten Zugriff auf Blockebene. Das in *NtosKrnl* integrierte "RAW"-Dateisystem kann die Dateisystemerkennungsstruktur lesen und Anwendungen über die Dateisystemsteuerungsanforderung [**FSCTL \_ QUERY FILE SYSTEM \_ \_ \_ RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)Zugriff auf solche Strukturen gewähren, wie im folgenden Beispiel gezeigt.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateisystemerkennung](file-system-recognition.md)
</dt> <dt>

[**\_ \_ \_ DATEISYSTEMERKENNUNGSSTRUKTUR**](file-system-recognition-structure.md)
</dt> <dt>

[**FSCTL \_ QUERY \_ FILE \_ SYSTEM \_ RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
