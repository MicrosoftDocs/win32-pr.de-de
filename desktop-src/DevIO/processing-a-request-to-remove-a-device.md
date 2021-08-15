---
description: Eine Anwendung empfängt ein DBT \_ DEVICEQUERYREMOVE-Geräteereignis, wenn ein Feature im System entschieden hat, ein angegebenes Gerät zu entfernen.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Verarbeiten einer Anforderung zum Entfernen eines Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6432ba2709dd05589acd5f8e0a2d1de6547216c9d24d4c9d742b9ad6dcc838e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956779"
---
# <a name="processing-a-request-to-remove-a-device"></a>Verarbeiten einer Anforderung zum Entfernen eines Geräts

Eine Anwendung empfängt ein [DBT \_ DEVICEQUERYREMOVE-Geräteereignis,](dbt-devicequeryremove.md) wenn ein Feature im System entschieden hat, ein angegebenes Gerät zu entfernen. Wenn die Anwendung dieses Ereignis empfängt, sollte sie bestimmen, ob sie das angegebene Gerät verwendet, und entweder abbrechen oder die Entfernung vorbereiten.

Im folgenden Beispiel verwaltet eine Anwendung ein geöffnetes Handle hFile für die Datei oder das Gerät, das durch FileName dargestellt wird. Die Anwendung registriert sich für die Geräteereignisbenachrichtigung auf dem zugrunde liegenden Gerät, indem sie die [**RegisterDeviceNotification-Funktion**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) **aufruft, einen DBT \_ DEVTYP \_ HANDLE-Typbenachrichtigungsfilter** verwendet und die Variable hFile im **\_ dbch-Handlemember** des Filters angibt.

Die Anwendung verarbeitet das [DBT \_ DEVICEQUERYREMOVE-Geräteereignis,](dbt-devicequeryremove.md) indem das geöffnete Dateihandle für das Gerät geschlossen wird, das entfernt werden soll. Wenn das Entfernen dieses Geräts abgebrochen wird, verarbeitet die Anwendung das [DBT \_ DEVICEQUERYREMOVEFAILED-Geräteereignis,](dbt-devicequeryremovefailed.md) um das Handle für das Gerät erneut zu öffnen. Nachdem das Gerät aus dem System entfernt wurde, verarbeitet die Anwendung die [Geräteereignisse DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) und [DBT \_ DEVICEREMOVEPENDING,](dbt-deviceremovepending.md) indem die Registrierung des Benachrichtigungshandles für das Gerät aufgehoben und alle Handles geschlossen werden, die noch für das Gerät geöffnet sind.


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
  // ...

INT_PTR WINAPI WinProcCallback( HWND hWnd,
                                UINT message,
                                WPARAM wParam,
                                LPARAM lParam )
{
  LPCTSTR FileName = NULL;              // path to the file or device of interest
  HANDLE  hFile = INVALID_HANDLE_VALUE; // handle to the file or device

  PDEV_BROADCAST_HDR    pDBHdr;
  PDEV_BROADCAST_HANDLE pDBHandle;
  TCHAR szMsg[80];

  switch (message)
  {
  //...
  case WM_DEVICECHANGE:
    switch (wParam)
    {
      case DBT_DEVICEQUERYREMOVE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // A request has been made to remove the device;
            // close any open handles to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }
        }
        return TRUE;

      case DBT_DEVICEQUERYREMOVEFAILED:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // Removal of the device has failed;
            // reopen a handle to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            hFile = CreateFile(FileName,
                       GENERIC_READ,
                       FILE_SHARE_READ,
                       NULL,
                       OPEN_EXISTING,
                       FILE_ATTRIBUTE_NORMAL,
                       NULL);
            if (hFile == INVALID_HANDLE_VALUE) 
            {
              StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                               TEXT("CreateFile failed: %lx.\n"), 
                               GetLastError());
              MessageBox(hWnd, szMsg, TEXT("CreateFile"), MB_OK);
            }
        }
        return TRUE;

      case DBT_DEVICEREMOVEPENDING:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
          
            // The device is being removed;
            // close any open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      case DBT_DEVICEREMOVECOMPLETE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            // The device has been removed from the system;
            // unregister its notification handle

            UnregisterDeviceNotification(
              pDBHandle->dbch_hdevnotify);
              
            // The device has been removed;
            // close any remaining open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      default:
        return TRUE;
    }
  }
  default:
    return TRUE;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräteereignistypen](device-event-types.md)
</dt> </dl>

 

 



