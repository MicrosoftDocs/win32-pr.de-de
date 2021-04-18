---
description: Nachdem Sie die Funktionen eines Telefon Geräts ermittelt haben, muss eine Anwendung das Gerät öffnen, bevor es auf die Funktionen auf diesem Telefon zugreifen kann.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Öffnen und Schließen von Telefongeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345779"
---
# <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="f19f3-103">Öffnen und Schließen von Telefongeräten</span><span class="sxs-lookup"><span data-stu-id="f19f3-103">Opening and Closing Phone Devices</span></span>

<span data-ttu-id="f19f3-104">Nachdem Sie die Funktionen eines Telefon Geräts ermittelt haben, muss eine Anwendung das Gerät öffnen, bevor es auf die Funktionen auf diesem Telefon zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="f19f3-104">After determining the capabilities of a phone device, an application must open the device before it can access functions on that phone.</span></span> <span data-ttu-id="f19f3-105">Nachdem ein Telefongerät erfolgreich geöffnet wurde, wird der Anwendung ein Handle zurückgegeben, das das geöffnete Telefon darstellt.</span><span class="sxs-lookup"><span data-stu-id="f19f3-105">After a phone device has been successfully opened, the application is returned a handle representing the open phone.</span></span> <span data-ttu-id="f19f3-106">Ein Telefongerät kann in verschiedenen Modi geöffnet werden, sodass eine strukturierte Methode zur Freigabe eines Telefon Geräts bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f19f3-106">A phone device can be opened in different modes, thus providing a structured way of sharing a phone device.</span></span>

<span data-ttu-id="f19f3-107">Die [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) -Funktion öffnet das angegebene Telefongerät, damit die Anwendung Zugriff auf Funktionen auf dem Telefon erhält.</span><span class="sxs-lookup"><span data-stu-id="f19f3-107">The [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) function opens the specified phone device to give the application access to functions on the phone.</span></span> <span data-ttu-id="f19f3-108">Ein Telefongerät wird mit dem zugehörigen Geräte Bezeichner als **phoneopen** identifiziert, das als *dwtoviceid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f19f3-108">A phone device is identified to **phoneOpen** by means of its device identifier, which is passed as the *dwDeviceID* parameter.</span></span>

 

 



