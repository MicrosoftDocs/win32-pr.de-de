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
# <a name="detecting-media-insertion-or-removal"></a><span data-ttu-id="c2399-103">Erkennen von Medien einfügen oder entfernen</span><span class="sxs-lookup"><span data-stu-id="c2399-103">Detecting Media Insertion or Removal</span></span>

<span data-ttu-id="c2399-104">Windows sendet allen Fenstern der obersten Ebene eine Reihe von standardmäßigen [**WM \_ devicechange**](wm-devicechange.md) -Nachrichten, wenn neue Geräte oder Medien (z. b. eine CD oder DVD) hinzugefügt und verfügbar werden und vorhandene Geräte oder Medien entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c2399-104">Windows sends all top-level windows a set of default [**WM\_DEVICECHANGE**](wm-devicechange.md) messages when new devices or media (such as a CD or DVD) are added and become available, and when existing devices or media are removed.</span></span> <span data-ttu-id="c2399-105">Sie müssen sich nicht registrieren, um diese Standard Meldungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c2399-105">You do not need to register to receive these default messages.</span></span> <span data-ttu-id="c2399-106">Ausführliche Informationen dazu, welche Nachrichten standardmäßig gesendet werden, finden Sie im Abschnitt "Hinweise" unter [**registerdevicenotifi.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)</span><span class="sxs-lookup"><span data-stu-id="c2399-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details on which messages are sent by default.</span></span> <span data-ttu-id="c2399-107">Die Nachrichten im folgenden Codebeispiel gehören zu den Standard Meldungen.</span><span class="sxs-lookup"><span data-stu-id="c2399-107">The messages in the code example below are among the default messages.</span></span>

> [!Note]  
> <span data-ttu-id="c2399-108">Windows sendet nur [**WM \_ devicechange**](wm-devicechange.md) -Nachrichten für CD-oder DVD-Medienereignisse an Fenster der obersten Ebene, die sich im Besitz von Anwendungen befinden, die in der aktiven Konsolen Sitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c2399-108">Windows only sends [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events to top-level windows that are owned by applications that run in the active console session.</span></span> <span data-ttu-id="c2399-109">Fenster der obersten Ebene, die sich im Besitz von Anwendungen befinden, die in einer Remote Desktop Sitzung ausgeführt werden, empfangen keine [**WM \_ devicechange**](wm-devicechange.md) -Nachrichten für CD-oder DVD-Medienereignisse.</span><span class="sxs-lookup"><span data-stu-id="c2399-109">Top-level windows that are owned by applications that run in a remote desktop session do not receive [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events.</span></span>

 

<span data-ttu-id="c2399-110">Jede [**WM \_ devicechange**](wm-devicechange.md) -Nachricht verfügt über ein zugeordnetes Ereignis, das die Änderung beschreibt, und eine Struktur, die ausführliche Informationen zur Änderung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c2399-110">Each [**WM\_DEVICECHANGE**](wm-devicechange.md) message has an associated event that describes the change, and a structure that provides detailed information about the change.</span></span> <span data-ttu-id="c2399-111">Die Struktur besteht aus einem Ereignis unabhängigen Header ( [**dev \_ Broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)), gefolgt von Ereignis abhängigen Membern.</span><span class="sxs-lookup"><span data-stu-id="c2399-111">The structure consists of an event-independent header, [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), followed by event-dependent members.</span></span> <span data-ttu-id="c2399-112">Die Ereignis abhängigen Member beschreiben das Gerät, für das das Ereignis gilt.</span><span class="sxs-lookup"><span data-stu-id="c2399-112">The event-dependent members describe the device to which the event applies.</span></span> <span data-ttu-id="c2399-113">Um diese Struktur verwenden zu können, müssen Anwendungen zuerst den Ereignistyp und den Gerätetyp ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c2399-113">To use this structure, applications must first determine the event type and the device type.</span></span> <span data-ttu-id="c2399-114">Anschließend können Sie die richtige-Struktur verwenden, um die entsprechende Aktion durchführen.</span><span class="sxs-lookup"><span data-stu-id="c2399-114">Then, they can use the correct structure to take appropriate action.</span></span>

<span data-ttu-id="c2399-115">Wenn der Benutzer eine neue CD oder DVD in ein Laufwerk einfügt, erhalten Anwendungen eine [**WM \_ devicechange**](wm-devicechange.md) -Nachricht mit einem [DBT \_ devicearrival](dbt-devicearrival.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c2399-115">When the user inserts a new CD or DVD into a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEARRIVAL](dbt-devicearrival.md) event.</span></span> <span data-ttu-id="c2399-116">Die Anwendung muss das Ereignis überprüfen, um sicherzustellen, dass der Typ des eintreffenden Geräts ein Volume ist (der **dbch \_ den DeviceType "** -Member ist **DBT \_ \_ devypvolume**) und dass sich die Änderung auf die Medien auswirkt (der **dbcv- \_ Flags** -Member ist **dbtf- \_ Medien**).</span><span class="sxs-lookup"><span data-stu-id="c2399-116">The application must check the event to ensure that the type of device arriving is a volume (the **dbch\_devicetype** member is **DBT\_DEVTYP\_VOLUME**) and that the change affects the media (the **dbcv\_flags** member is **DBTF\_MEDIA**).</span></span>

<span data-ttu-id="c2399-117">Wenn der Benutzer eine CD oder DVD von einem Laufwerk entfernt, erhalten Anwendungen eine [**WM \_ devicechange**](wm-devicechange.md) -Nachricht mit einem [DBT \_ deviceremovecomplete](dbt-deviceremovecomplete.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c2399-117">When the user removes a CD or DVD from a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) event.</span></span> <span data-ttu-id="c2399-118">Die Anwendung muss das Ereignis erneut überprüfen, um sicherzustellen, dass das Gerät, das entfernt wird, ein Volume ist und dass sich die Änderung auf die Medien auswirkt.</span><span class="sxs-lookup"><span data-stu-id="c2399-118">Again, the application must check the event to ensure that the device being removed is a volume and that the change affects the media.</span></span>

<span data-ttu-id="c2399-119">Der folgende Code veranschaulicht, wie Sie das Einfügen oder Entfernen einer CD oder DVD überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c2399-119">The following code demonstrates how to check for insertion or removal of a CD or DVD.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c2399-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2399-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2399-121">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c2399-121">Device Events</span></span>](device-events.md)
</dt> </dl>

 

 



