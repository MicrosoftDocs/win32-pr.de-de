---
description: Windows sendet allen Fenstern der obersten Ebene eine Reihe von STANDARD-WM DEVICECHANGE-Nachrichten, wenn neue Geräte oder Medien (z. B. eine CD oder DVD) hinzugefügt und verfügbar werden und vorhandene Geräte oder Medien entfernt \_ werden.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Erkennen des Einfügens oder Entfernens von Medien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3f6d579ed654ae2d2f77d00f70b88dc1441d03bbce59c0f8cb39ca6800c6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318350"
---
# <a name="detecting-media-insertion-or-removal"></a>Erkennen des Einfügens oder Entfernens von Medien

Windows allen Fenstern der obersten Ebene eine Reihe von [**STANDARD-WM \_ DEVICECHANGE-Nachrichten,**](wm-devicechange.md) wenn neue Geräte oder Medien (z. B. eine CD oder DVD) hinzugefügt und verfügbar werden und vorhandene Geräte oder Medien entfernt werden. Sie müssen sich nicht registrieren, um diese Standardnachrichten zu empfangen. Weitere Informationen dazu, welche Nachrichten standardmäßig gesendet werden, finden Sie im Abschnitt "Hinweise" in [**RegisterDeviceNotification.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Die Nachrichten im folgenden Codebeispiel gehören zu den Standardmeldungen.

> [!Note]  
> Windows werden nur [**WM \_ DEVICECHANGE-Nachrichten**](wm-devicechange.md) für CD- oder DVD-Medienereignisse an Fenster der obersten Ebene gesendet, die sich im Besitz von Anwendungen befinden, die in der aktiven Konsolensitzung ausgeführt werden. Fenster der obersten Ebene, die sich im Besitz von Anwendungen befinden, die in einer Remotedesktopsitzung ausgeführt werden, empfangen keine [**WM \_ DEVICECHANGE-Nachrichten**](wm-devicechange.md) für CD- oder DVD-Medienereignisse.

 

Jede [**WM \_ DEVICECHANGE-Nachricht**](wm-devicechange.md) verfügt über ein zugeordnetes Ereignis, das die Änderung beschreibt, und eine Struktur, die ausführliche Informationen zur Änderung enthält. Die -Struktur besteht aus einem ereignisunabhängigen Header, [**DEV \_ BROADCAST \_ HDR,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)gefolgt von ereignisabhängigen Membern. Die ereignisabhängigen Member beschreiben das Gerät, für das das Ereignis gilt. Um diese Struktur zu verwenden, müssen Anwendungen zuerst den Ereignistyp und den Gerätetyp bestimmen. Anschließend können sie die richtige Struktur verwenden, um entsprechende Maßnahmen zu ergreifen.

Wenn der Benutzer eine neue CD oder DVD in ein Laufwerk einfüge, erhalten Anwendungen eine [**WM \_ DEVICECHANGE-Nachricht**](wm-devicechange.md) mit einem [DBT \_ DEVICEARRARRARR-Ereignis.](dbt-devicearrival.md) Die Anwendung muss das Ereignis überprüfen, um sicherzustellen, dass der Typ des eintreffenden Geräts ein Volume ist **(das dbch \_ devicetype-Member** **ist DBT \_ DEVTYP \_ VOLUME),** und dass sich die Änderung auf das Medium auswirken (dbcv **\_ flags-Member** ist **DBTF \_ MEDIA).**

Wenn der Benutzer eine CD oder DVD von einem Laufwerk entfernt, erhalten Anwendungen eine [**WM \_ DEVICECHANGE-Nachricht**](wm-devicechange.md) mit einem [DBT \_ DEVICEREMOVECOMPLETE-Ereignis.](dbt-deviceremovecomplete.md) Auch hier muss die Anwendung das Ereignis überprüfen, um sicherzustellen, dass das zu entfernende Gerät ein Volume ist und dass sich die Änderung auf die Medien auswirken kann.

Der folgende Code veranschaulicht, wie sie das Einfügen oder Entfernen einer CD oder DVD überprüfen.


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

[Geräteereignisse](device-events.md)
</dt> </dl>

 

 



