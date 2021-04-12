---
title: Aktualisieren von tragbaren Geräten
description: Aktualisieren von tragbaren Geräten
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Windows Media Player Online Stores, Aktualisieren von tragbaren Geräten
- Online Stores, Aktualisieren von tragbaren Geräten
- Geben Sie 1 Online Stores ein, aktualisieren Sie tragbare Geräte.
- Windows Media Player Online Stores, portable Geräte
- Online Stores, portable Geräte
- Typ 1 Online Stores, portable Geräte
- Aktualisieren von tragbaren Geräten
- Portable Geräte, aktualisieren
- Portable Geräte, Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314225"
---
# <a name="updating-portable-devices"></a><span data-ttu-id="bbacb-112">Aktualisieren von tragbaren Geräten</span><span class="sxs-lookup"><span data-stu-id="bbacb-112">Updating Portable Devices</span></span>

<span data-ttu-id="bbacb-113">Windows Media Player ermöglicht Benutzern das Synchronisieren digitaler Medieninhalte mit tragbaren Geräten.</span><span class="sxs-lookup"><span data-stu-id="bbacb-113">Windows Media Player enables users to synchronize digital media content with portable devices.</span></span> <span data-ttu-id="bbacb-114">Dies kann Musikinhalte enthalten, die in einem Online Store erworben oder gemietet wurden.</span><span class="sxs-lookup"><span data-stu-id="bbacb-114">This can include music content purchased or rented from an online store.</span></span> <span data-ttu-id="bbacb-115">Unter bestimmten Umständen möchten Online Store-Anbieter vielleicht Code schreiben, um auf einem verbundenen tragbaren Gerät als Teil der Verwaltung von Inhalten des Stores zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bbacb-115">Under some circumstances, online store providers might want to write code to work on a connected portable device as part of managing content provided by the store.</span></span> <span data-ttu-id="bbacb-116">Um dem Online Shop-Plug-in die Gelegenheit zu geben, mit einem verbundenen Gerät zu arbeiten, ruft Windows Media Player [iwmpcontentpartner:: updatedevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) auf und gibt den kanonischen Namen des portablen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="bbacb-116">To give the online store plug-in the opportunity to work with a connected device, Windows Media Player calls [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) and provides the canonical name of the portable device.</span></span> <span data-ttu-id="bbacb-117">Wenn der Plug-in-Code feststellt, dass die Arbeit mit dem verbundenen Gerät erledigt werden muss, muss er \_ vom **Update Device-Update** sofort den Wert OK zurückgeben, bevor die Arbeit fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bbacb-117">If the plug-in code determines that some work must be done with the connected device, it must immediately return S\_OK from the call to **UpdateDevice** before proceeding to do the work.</span></span> <span data-ttu-id="bbacb-118">Wenn keine Arbeit durchzuführen ist, sollte das Plug-in einen Fehlercode zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bbacb-118">If there is no work to do, the plug-in should return an error code.</span></span>

<span data-ttu-id="bbacb-119">Wenn das Plug-in die Verwendung des Geräts abgeschlossen hat, muss es [iwmpcontentpartnercallback:: updatedevicecomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) aufrufen, um Windows Media Player zu benachrichtigen, dass das Gerät verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="bbacb-119">When the plug-in has finished using the device, it must call [IWMPContentPartnerCallback::UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) to notify Windows Media Player that the device is available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbacb-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbacb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbacb-121">**Programmier Handbuch für den Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="bbacb-121">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




