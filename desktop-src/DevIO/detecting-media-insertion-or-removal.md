---
description: Windows sendet allen Fenstern der obersten Ebene eine Reihe von standardmäßigen WM \_ devicechange-Nachrichten, wenn neue Geräte oder Medien (z. b. eine CD oder DVD) hinzugefügt und verfügbar werden und vorhandene Geräte oder Medien entfernt werden.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Erkennen von Medien einfügen oder entfernen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6cfd4539d6f2ce5eac41e355f56a5a87835505
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132169"
---
# <a name="detecting-media-insertion-or-removal"></a>Erkennen von Medien einfügen oder entfernen

Windows sendet allen Fenstern der obersten Ebene eine Reihe von standardmäßigen [**WM \_ devicechange**](wm-devicechange.md) -Nachrichten, wenn neue Geräte oder Medien (z. b. eine CD oder DVD) hinzugefügt und verfügbar werden und vorhandene Geräte oder Medien entfernt werden. Sie müssen sich nicht registrieren, um diese Standard Meldungen zu empfangen. Ausführliche Informationen dazu, welche Nachrichten standardmäßig gesendet werden, finden Sie im Abschnitt "Hinweise" unter [**registerdevicenotifi.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Die Nachrichten im folgenden Codebeispiel gehören zu den Standard Meldungen.

> [!Note]  
> Windows sendet nur [**WM \_ devicechange**](wm-devicechange.md) -Nachrichten für CD-oder DVD-Medienereignisse an Fenster der obersten Ebene, die sich im Besitz von Anwendungen befinden, die in der aktiven Konsolen Sitzung ausgeführt werden. Fenster der obersten Ebene, die sich im Besitz von Anwendungen befinden, die in einer Remote Desktop Sitzung ausgeführt werden, empfangen keine [**WM \_ devicechange**](wm-devicechange.md) -Nachrichten für CD-oder DVD-Medienereignisse.

 

Jede [**WM \_ devicechange**](wm-devicechange.md) -Nachricht verfügt über ein zugeordnetes Ereignis, das die Änderung beschreibt, und eine Struktur, die ausführliche Informationen zur Änderung bereitstellt. Die Struktur besteht aus einem Ereignis unabhängigen Header ( [**dev \_ Broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)), gefolgt von Ereignis abhängigen Membern. Die Ereignis abhängigen Member beschreiben das Gerät, für das das Ereignis gilt. Um diese Struktur verwenden zu können, müssen Anwendungen zuerst den Ereignistyp und den Gerätetyp ermitteln. Anschließend können Sie die richtige-Struktur verwenden, um die entsprechende Aktion durchführen.

Wenn der Benutzer eine neue CD oder DVD in ein Laufwerk einfügt, erhalten Anwendungen eine [**WM \_ devicechange**](wm-devicechange.md) -Nachricht mit einem [DBT \_ devicearrival](dbt-devicearrival.md) -Ereignis. Die Anwendung muss das Ereignis überprüfen, um sicherzustellen, dass der Typ des eintreffenden Geräts ein Volume ist (der **dbch \_ den DeviceType "** -Member ist **DBT \_ \_ devypvolume**) und dass sich die Änderung auf die Medien auswirkt (der **dbcv- \_ Flags** -Member ist **dbtf- \_ Medien**).

Wenn der Benutzer eine CD oder DVD von einem Laufwerk entfernt, erhalten Anwendungen eine [**WM \_ devicechange**](wm-devicechange.md) -Nachricht mit einem [DBT \_ deviceremovecomplete](dbt-deviceremovecomplete.md) -Ereignis. Die Anwendung muss das Ereignis erneut überprüfen, um sicherzustellen, dass das Gerät, das entfernt wird, ein Volume ist und dass sich die Änderung auf die Medien auswirkt.

Der folgende Code veranschaulicht, wie Sie das Einfügen oder Entfernen einer CD oder DVD überprüfen.


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
#pragma comment(lib, "user32.lib" )

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam );
char FirstDriveFromMask( ULONG unitmask );  //prototype

/*------------------------------------------------------------------
   Main_OnDeviceChange( hwnd, wParam, lParam )

   Description
      Handles WM_DEVICECHANGE messages sent to the application's
      top-level window.
--------------------------------------------------------------------*/

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam )
 {
  PDEV_BROADCAST_HDR lpdb = (PDEV_BROADCAST_HDR)lParam;
  TCHAR szMsg[80];

  switch(wParam )
   {
    case DBT_DEVICEARRIVAL:
      // Check whether a CD or DVD was inserted into a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media has arrived.\n"), 
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE"), MB_OK );
         }
       }
      break;

    case DBT_DEVICEREMOVECOMPLETE:
      // Check whether a CD or DVD was removed from a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media was removed.\n" ),
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE" ), MB_OK );
         }
       }
      break;

    default:
      /*
        Process other WM_DEVICECHANGE notifications for other 
        devices or reasons.
      */ 
      ;
   }
}

/*------------------------------------------------------------------
   FirstDriveFromMask( unitmask )

   Description
     Finds the first valid drive letter from a mask of drive letters.
     The mask must be in the format bit 0 = A, bit 1 = B, bit 2 = C, 
     and so on. A valid drive letter is defined when the 
     corresponding bit is set to 1.

   Returns the first drive letter that was found.
--------------------------------------------------------------------*/

char FirstDriveFromMask( ULONG unitmask )
 {
  char i;

  for (i = 0; i < 26; ++i)
   {
    if (unitmask & 0x1)
      break;
    unitmask = unitmask >> 1;
   }

  return( i + 'A' );
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte Ereignisse](device-events.md)
</dt> </dl>

 

 



