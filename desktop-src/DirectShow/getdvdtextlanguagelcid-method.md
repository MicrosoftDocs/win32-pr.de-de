---
description: Die getdvdtextlanguagelcid-Methode ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) für den angegebenen Textzeichen folgen Block ab.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Getdvdtextlanguagelcid-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520632"
---
# <a name="getdvdtextlanguagelcid-method"></a><span data-ttu-id="61a1f-103">Getdvdtextlanguagelcid-Methode</span><span class="sxs-lookup"><span data-stu-id="61a1f-103">GetDVDTextLanguageLCID Method</span></span>

> [!Note]  
> <span data-ttu-id="61a1f-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61a1f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="61a1f-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="61a1f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="61a1f-106">Die- `GetDVDTextLanguageLCID` Methode ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) für den angegebenen Textzeichen folgen Block ab.</span><span class="sxs-lookup"><span data-stu-id="61a1f-106">The `GetDVDTextLanguageLCID` method retrieves the locale identifier (LCID) for the specified text string block.</span></span>

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="61a1f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="61a1f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a1f-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*ilangindex*</span><span class="sxs-lookup"><span data-stu-id="61a1f-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="61a1f-109">Gibt den Text Sprach Block auf der Festplatte als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="61a1f-109">Specifies the text language block on the disc as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a1f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61a1f-110">Return Value</span></span>

<span data-ttu-id="61a1f-111">Gibt einen LCID-Wert zurück, der Informationen zur Angabe der Sprache enthält, in der die Zeichen folgen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="61a1f-111">Returns an LCID value that contains information specifying the language the strings are written in.</span></span>

## <a name="remarks"></a><span data-ttu-id="61a1f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61a1f-112">Remarks</span></span>

<span data-ttu-id="61a1f-113">Ergänzende Text Zeichenfolgen werden in zusammenhängenden Blöcken auf der Festplatte gespeichert. Jede Sprache verfügt über einen Block von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="61a1f-113">Supplemental text strings are stored in contiguous blocks on the disc. Each language has one block of strings.</span></span> <span data-ttu-id="61a1f-114">Eine Anwendung gibt diese Blöcke durch einen Index an, der kleiner als der von [**getdvdtextnumoflanguages**](getdvdtextnumberoflanguages-method.md)zurückgegebene Wert sein muss.</span><span class="sxs-lookup"><span data-stu-id="61a1f-114">An application specifies these blocks by an index, which must be less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="61a1f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61a1f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a1f-116">Mswebdvd-Objekt</span><span class="sxs-lookup"><span data-stu-id="61a1f-116">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> <dt>

[<span data-ttu-id="61a1f-117">**Getlangfromlangid**</span><span class="sxs-lookup"><span data-stu-id="61a1f-117">**GetLangFromLangID**</span></span>](getlangfromlangid-method.md)
</dt> </dl>

 

 



