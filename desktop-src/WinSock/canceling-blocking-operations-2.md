---
description: Ein Thread kann jederzeit wsaisblockierung aufzurufen, um zu bestimmen, ob zurzeit ein Blockierungs Aufruf ausgeführt wird.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Abbrechen von blockierenden Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349002"
---
# <a name="canceling-blocking-operations"></a><span data-ttu-id="7dbf5-103">Abbrechen von blockierenden Vorgängen</span><span class="sxs-lookup"><span data-stu-id="7dbf5-103">Canceling Blocking Operations</span></span>

<span data-ttu-id="7dbf5-104">Ein Thread kann jederzeit [wsaisblockierung](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) aufzurufen, um zu bestimmen, ob zurzeit ein Blockierungs Aufruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7dbf5-104">A thread may, at any time, call [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) to determine whether or not a blocking call is currently in progress.</span></span> <span data-ttu-id="7dbf5-105">(Diese Funktion ist innerhalb der Windows Sockets 1,1-Kompatibilitäts-Shims implementiert und hat daher kein SPI-Pendant.) Dies ist offensichtlich nur möglich, wenn eine Pseudo Blockierung statt einer echten Blockierung vom Dienstanbieter eingesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="7dbf5-105">(This function is implemented within the Windows Sockets 1.1 compatibility shims and hence has no SPI counterpart.) Clearly this is only possible when pseudo blocking, as opposed to true blocking, is being employed by the service provider.</span></span> <span data-ttu-id="7dbf5-106">Bei Bedarf kann [**wspcancelblockingcalljederzeit**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) aufgerufen werden, um alle aktuellen Pseudo Blockierungs Vorgänge abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="7dbf5-106">When necessary, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) may be called at any time to cancel any current pseudo blocking operation.</span></span>

 

 
