---
description: Eine Anwendung empfängt ein DBT \_ DeviceQueryRemove-Geräte Ereignis, wenn eine Funktion im System beschlossen hat, ein bestimmtes Gerät zu entfernen.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Verarbeiten einer Anforderung zum Entfernen eines Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f6f1089cae0e4c9db964e3877cac8f8f8d8da4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126781"
---
# <a name="processing-a-request-to-remove-a-device"></a>Verarbeiten einer Anforderung zum Entfernen eines Geräts

Eine Anwendung empfängt ein [DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md) -Geräte Ereignis, wenn eine Funktion im System beschlossen hat, ein bestimmtes Gerät zu entfernen. Wenn die Anwendung dieses Ereignis empfängt, sollte Sie ermitteln, ob Sie das angegebene Gerät verwendet, und entweder abbrechen oder die Entfernung vorbereiten.

Im folgenden Beispiel verwaltet eine Anwendung ein geöffnetes Handle (hFile) für die Datei oder das Gerät, dargestellt durch filename. Die Anwendung wird für die Geräte Ereignis Benachrichtigung auf dem zugrunde liegenden Gerät registriert, indem die [**registerdevicenotifi-**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Funktion aufgerufen wird, ein **DBT \_ devtype \_** -Benachrichtigungs Filter verwendet und die hFile-Variable im **dbch- \_ handle** -Member des Filters angegeben wird.

Die Anwendung verarbeitet das [DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md) -Geräte Ereignis, indem das geöffnete Datei Handle für das zu entfernende Gerät geschlossen wird. Wenn das Entfernen dieses Geräts abgebrochen wird, verarbeitet die Anwendung das [DBT \_ devicequeryremovefailed](dbt-devicequeryremovefailed.md) -Geräte Ereignis, um das Handle für das Gerät erneut zu öffnen. Nachdem das Gerät aus dem System entfernt wurde, verarbeitet die Anwendung die Geräte Ereignisse [DBT \_ deviceremovecomplete](dbt-deviceremovecomplete.md) und [DBT \_ deviceremovepend](dbt-deviceremovepending.md) , indem die Registrierung des Benachrichtigungs Handles für das Gerät aufgehoben und alle Handles geschlossen werden, die noch für das Gerät geöffnet sind.


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

[Geräte Ereignis Typen](device-event-types.md)
</dt> </dl>

 

 



