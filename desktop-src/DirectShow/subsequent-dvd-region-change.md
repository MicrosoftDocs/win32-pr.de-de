---
description: Nachfolgende DVD-Regions Änderung
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Nachfolgende DVD-Regions Änderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a28982d6807fa5d90356d15cbf5365a595c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366170"
---
# <a name="subsequent-dvd-region-change"></a><span data-ttu-id="7031c-103">Nachfolgende DVD-Regions Änderung</span><span class="sxs-lookup"><span data-stu-id="7031c-103">Subsequent DVD Region Change</span></span>

<span data-ttu-id="7031c-104">In Windows 2000 und höher ruft der DVD-Navigator eine Eigenschaften Seite auf dem DVD-ROM-Laufwerk Gerät in der Device Manager auf.</span><span class="sxs-lookup"><span data-stu-id="7031c-104">In Windows 2000 and later, the DVD Navigator invokes a property page on the DVD-ROM drive device in the Device Manager.</span></span> <span data-ttu-id="7031c-105">Diese Eigenschaften Seite wird auch von der DVDPlay.exe Anwendung hochgefahren, wenn eine Region geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="7031c-105">This property page is also brought up by the DVDPlay.exe application when a region needs to be changed.</span></span> <span data-ttu-id="7031c-106">Die Benutzeroberfläche dieser Eigenschaften Seite ähnelt der von DVDRgn.exe und wird im Betriebssystem regionalisiert.</span><span class="sxs-lookup"><span data-stu-id="7031c-106">The UI of this property page is very similar to that of DVDRgn.exe and it is regionalized in the operating system.</span></span>

<span data-ttu-id="7031c-107">Für RPC1-Laufwerke verwalten die Komponenten des Windows-Betriebssystems Regions Änderungen.</span><span class="sxs-lookup"><span data-stu-id="7031c-107">For RPC1 drives, the Windows Operating System components manage region changes.</span></span> <span data-ttu-id="7031c-108">Rpc2-Laufwerke behalten die Regions Einstellung in ihrer eigenen Hardware bei.</span><span class="sxs-lookup"><span data-stu-id="7031c-108">RPC2 drives maintain the region setting in their own hardware.</span></span> <span data-ttu-id="7031c-109">Wenn die Anzahl zulässiger Änderungen auf einem rpc2-Laufwerk erschöpft ist, kann das Laufwerk den Wechsel zum Ändern der Region nicht durchführen, und die Komponente zum Ändern der Region im Betriebssystem zeigt den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="7031c-109">When the number of allowed changes are exhausted on a RPC2 drive, the drive will fail the call to change the region and the region-change component in the operating system will indicate that to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7031c-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7031c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7031c-111">Unterstützung der Änderung von DVD-Regionen in Windows</span><span class="sxs-lookup"><span data-stu-id="7031c-111">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



