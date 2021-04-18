---
description: Die getdvdtextnumofstrings-Methode ruft die Anzahl von Text Zeichenfolgen ab, die für die angegebene Sprache verfügbar sind.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Getdvdtextnummeriofstrings-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341110"
---
# <a name="getdvdtextnumberofstrings-method"></a><span data-ttu-id="8141f-103">Getdvdtextnummeriofstrings-Methode</span><span class="sxs-lookup"><span data-stu-id="8141f-103">GetDVDTextNumberOfStrings Method</span></span>

> [!Note]  
> <span data-ttu-id="8141f-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8141f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8141f-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8141f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8141f-106">Die- `GetDVDTextNumberOfStrings` Methode ruft die Anzahl von Text Zeichenfolgen ab, die für die angegebene Sprache verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8141f-106">The `GetDVDTextNumberOfStrings` method retrieves the number of text strings available for the specified language.</span></span>

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="8141f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8141f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8141f-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*ilangindex*</span><span class="sxs-lookup"><span data-stu-id="8141f-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="8141f-109">Gibt die Sprache als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="8141f-109">Specifies the language as an Integer.</span></span> <span data-ttu-id="8141f-110">Der Wert muss zwischen 0 (null) und einem Wert liegen, der kleiner als der von [**getdvdtextnumoflanguages**](getdvdtextnumberoflanguages-method.md)zurückgegebene Wert ist.</span><span class="sxs-lookup"><span data-stu-id="8141f-110">The value must range from zero through one less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8141f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8141f-111">Return Value</span></span>

<span data-ttu-id="8141f-112">Gibt einen ganzzahligen Wert zurück, der angibt, wie viele Zeichen folgen die Diskette in der angegebenen Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="8141f-112">Returns an integer value specifying how many strings the disc contains in the specified language.</span></span>

## <a name="see-also"></a><span data-ttu-id="8141f-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8141f-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8141f-114">Mswebdvd-Objekt</span><span class="sxs-lookup"><span data-stu-id="8141f-114">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



