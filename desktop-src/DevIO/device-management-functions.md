---
description: Die folgenden Funktionen werden in der Geräteverwaltung verwendet.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Geräte Verwaltungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958334"
---
# <a name="device-management-functions"></a><span data-ttu-id="4a1eb-103">Geräte Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4a1eb-103">Device Management Functions</span></span>

<span data-ttu-id="4a1eb-104">Die folgenden Funktionen werden in der Geräteverwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-104">The following functions are used in device management.</span></span>



| <span data-ttu-id="4a1eb-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="4a1eb-105">Function</span></span>                                                             | <span data-ttu-id="4a1eb-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a1eb-106">Description</span></span>                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a1eb-107">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="4a1eb-107">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | <span data-ttu-id="4a1eb-108">Sendet einen Steuerungs Code direkt an einen angegebenen Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-108">Sends a control code directly to a specified device driver.</span></span>                           |
| [<span data-ttu-id="4a1eb-109">**Installnewdevice**</span><span class="sxs-lookup"><span data-stu-id="4a1eb-109">**InstallNewDevice**</span></span>](installnewdevice.md)                         | <span data-ttu-id="4a1eb-110">Installiert ein neues Gerät.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-110">Installs a new device.</span></span> <span data-ttu-id="4a1eb-111">Der Benutzer wird aufgefordert, das Gerät auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-111">The user is prompted to select the device.</span></span>                     |
| [<span data-ttu-id="4a1eb-112">**Registerdevicenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="4a1eb-112">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | <span data-ttu-id="4a1eb-113">Registriert das Gerät oder den Typ des Geräts, für das ein Fenster Benachrichtigungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-113">Registers the device or type of device for which a window will receive notifications.</span></span> |
| [<span data-ttu-id="4a1eb-114">**Unregisterdevicenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="4a1eb-114">**UnregisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | <span data-ttu-id="4a1eb-115">Schließt das angegebene Benachrichtigungs Handle des Geräts.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-115">Closes the specified device notification handle.</span></span>                                      |



 

<span data-ttu-id="4a1eb-116">Die folgenden Funktionen werden mit CD-ROM-und DVD-Laufwerken verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-116">The following functions are used with CD-ROM and DVD drives.</span></span>



| <span data-ttu-id="4a1eb-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="4a1eb-117">Function</span></span>                                                               | <span data-ttu-id="4a1eb-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a1eb-118">Description</span></span>                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a1eb-119">**Cdromdisabledigitalplayback**</span><span class="sxs-lookup"><span data-stu-id="4a1eb-119">**CdromDisableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | <span data-ttu-id="4a1eb-120">Deaktiviert die digitale Wiedergabe für das angegebene CD-ROM-oder DVD-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-120">Disables digital playback for the specified CD-ROM or DVD drive.</span></span>                                    |
| [<span data-ttu-id="4a1eb-121">**Cdromenabledigitalplayback**</span><span class="sxs-lookup"><span data-stu-id="4a1eb-121">**CdromEnableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | <span data-ttu-id="4a1eb-122">Aktiviert die digitale Wiedergabe für das angegebene CD-ROM-oder DVD-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-122">Enables digital playback for the specified CD-ROM or DVD drive.</span></span>                                     |
| [<span data-ttu-id="4a1eb-123">**Cdromisdigitalplaybackaktivierte**</span><span class="sxs-lookup"><span data-stu-id="4a1eb-123">**CdromIsDigitalPlaybackEnabled**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | <span data-ttu-id="4a1eb-124">Bestimmt, ob die digitale Wiedergabe für das angegebene CD-ROM-oder DVD-Laufwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-124">Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.</span></span>               |
| [<span data-ttu-id="4a1eb-125">**Cdromknowngooddigitalplayback**</span><span class="sxs-lookup"><span data-stu-id="4a1eb-125">**CdromKnownGoodDigitalPlayback**</span></span>](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | <span data-ttu-id="4a1eb-126">Bestimmt, ob das angegebene CD-ROM-oder DVD-Laufwerk eine digitale Wiedergabe aufweist, die bekanntermaßen gut ist.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-126">Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.</span></span> |
| [<span data-ttu-id="4a1eb-127">**DVDLauncher**</span><span class="sxs-lookup"><span data-stu-id="4a1eb-127">**DvdLauncher**</span></span>](dvdlauncher.md)                                     | <span data-ttu-id="4a1eb-128">Überprüft, ob der Medienbereich im DVD-Laufwerk mit dem DVD-Laufwerks Bereich übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-128">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>                       |



 

 

 
