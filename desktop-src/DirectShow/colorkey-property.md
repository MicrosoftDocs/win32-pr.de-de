---
description: Die Colorkey-Eigenschaft legt den in Untertiteln verwendeten Farbschlüssel fest oder ruft ihn ab.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Colorkey-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481179"
---
# <a name="colorkey-property"></a><span data-ttu-id="6cb94-103">Colorkey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6cb94-103">ColorKey Property</span></span>

> [!Note]  
> <span data-ttu-id="6cb94-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cb94-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6cb94-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6cb94-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6cb94-106">Die- `ColorKey` Eigenschaft legt den in Untertiteln verwendeten Farbschlüssel fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="6cb94-106">The `ColorKey` property sets or retrieves the color key used in closed captioning.</span></span>

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a><span data-ttu-id="6cb94-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cb94-107">Return Value</span></span>

<span data-ttu-id="6cb94-108">Gibt einen ganzzahligen Wert zurück, der die Farbe darstellt, die als transparenter Hintergrund für Closed-beschrifteten Text verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cb94-108">Returns an integer value representing the color to use as a transparent background for closed-captioned text.</span></span> <span data-ttu-id="6cb94-109">Der Standardwert in 256 Farben ist Magenta und Off-Black in jeder anderen Farbtiefe.</span><span class="sxs-lookup"><span data-stu-id="6cb94-109">The default value in 256 colors is magenta, and off-black in any other color depth.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb94-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cb94-110">Remarks</span></span>

<span data-ttu-id="6cb94-111">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6cb94-111">This property is read/write.</span></span> <span data-ttu-id="6cb94-112">Diese Eigenschaft gilt nur für geschlossene Untertitel, sofern vorhanden, nicht für den subbildstream.</span><span class="sxs-lookup"><span data-stu-id="6cb94-112">This property applies only to the closed-captions, if any exist, not to the subpicture stream.</span></span>

 

 



