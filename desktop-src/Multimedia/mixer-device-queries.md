---
title: Geräte Abfragen im Mixer
description: Geräte Abfragen im Mixer
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- Multimedia-Audiodaten, Mixer-Geräte Abfragen
- Audiodaten, Mixer-Geräte Abfragen
- Audiomixer, Geräte Abfragen
- Mixer, Geräte Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038929"
---
# <a name="mixer-device-queries"></a><span data-ttu-id="66712-107">Geräte Abfragen im Mixer</span><span class="sxs-lookup"><span data-stu-id="66712-107">Mixer Device Queries</span></span>

<span data-ttu-id="66712-108">Die Mixer-Dienste bieten Funktionen zum Bestimmen der Anzahl der im System vorhandenen mischunggeräte und der Funktionen der Geräte.</span><span class="sxs-lookup"><span data-stu-id="66712-108">The mixer services provide functions for determining the number of mixer devices present in the system and the capabilities of the devices.</span></span> <span data-ttu-id="66712-109">Sie können auch eine Funktion "Mixer Dienste" verwenden, um den Geräte Bezeichner für ein Mischgerät zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="66712-109">You can also use a mixer services function to determine the device identifier for a mixer device.</span></span>

<span data-ttu-id="66712-110">Sie können die Funktion " [**mixergetnumdecovs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) " verwenden, um zu bestimmen, wie viele Mixergeräte im System vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="66712-110">You can use the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function to determine how many mixer devices are present in the system.</span></span> <span data-ttu-id="66712-111">Mixergeräte werden anhand eines Geräte Bezeichners identifiziert.</span><span class="sxs-lookup"><span data-stu-id="66712-111">Mixer devices are identified by a device identifier.</span></span> <span data-ttu-id="66712-112">Geräte Bezeichner werden implizit von der Anzahl der Geräte, die in einem bestimmten System vorhanden sind, bestimmt.</span><span class="sxs-lookup"><span data-stu-id="66712-112">Device identifiers are determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="66712-113">Sie reichen von 0 (null) bis zu der Anzahl der vorhandenen Geräte.</span><span class="sxs-lookup"><span data-stu-id="66712-113">They range from zero through one less than the number of devices present.</span></span>

<span data-ttu-id="66712-114">Vor der Verwendung eines Mixer-Geräts müssen Sie seine Funktionen bestimmen.</span><span class="sxs-lookup"><span data-stu-id="66712-114">Before using a mixer device, you must determine its capabilities.</span></span> <span data-ttu-id="66712-115">Die Audiofunktionen können von einem Multimedia-Computer zu einem anderen unterschiedlich sein, sodass Anwendungen mit einer Vielzahl von Audiohardware arbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="66712-115">Audio capabilities can vary from one multimedia computer to another, so applications need to work with a variety of audio hardware.</span></span>

<span data-ttu-id="66712-116">Sie können die Funktion " [**mixergetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) " verwenden, um die Funktionen von mischergeräten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="66712-116">You can use the [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) function to determine the capabilities of mixer devices.</span></span> <span data-ttu-id="66712-117">Diese Funktion füllt eine [**mixercaps**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) -Struktur mit Informationen zu den Funktionen eines angegebenen Geräts.</span><span class="sxs-lookup"><span data-stu-id="66712-117">This function fills a [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) structure with information about the capabilities of a specified device.</span></span>

<span data-ttu-id="66712-118">Die [**mixergetid**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) -Funktion Ruft den dem angegebenen Geräte handle zugeordneten audiomischgeräterbezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="66712-118">The [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) function retrieves the audio mixer device identifier associated with a specified device handle.</span></span> <span data-ttu-id="66712-119">Beispielsweise können Sie mit dieser Funktion den Geräte Bezeichner für einen Audiomixer abrufen und dann mithilfe des Geräte Bezeichners das Volume anpassen oder ein anderes Steuerelement anzeigen.</span><span class="sxs-lookup"><span data-stu-id="66712-119">For example, you could use this function to retrieve the device identifier for an audio mixer and then use the device identifier to adjust the volume or to display another control.</span></span>

 

 