---
description: Die selectdefaultaudiolanguage-Methode legt die aktuelle Standard Audiosprache im mswebdvd-Objekt fest.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Selectdefaultaudiolanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521275"
---
# <a name="selectdefaultaudiolanguage-method"></a><span data-ttu-id="5c048-103">Selectdefaultaudiolanguage-Methode</span><span class="sxs-lookup"><span data-stu-id="5c048-103">SelectDefaultAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="5c048-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c048-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5c048-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5c048-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5c048-106">Die `SelectDefaultAudioLanguage` -Methode legt die aktuelle Standard Audiosprache im mswebdvd-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="5c048-106">The `SelectDefaultAudioLanguage` method sets the current default audio language in the MSWebDVD object.</span></span>

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a><span data-ttu-id="5c048-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c048-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c048-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*ilang*</span><span class="sxs-lookup"><span data-stu-id="5c048-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="5c048-109">Gibt die Sprache als einen LCID-ganzzahligen Wert an.</span><span class="sxs-lookup"><span data-stu-id="5c048-109">Specifies the language as an Integer LCID value.</span></span>

</dd> <dt>

<span data-ttu-id="5c048-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iext*</span><span class="sxs-lookup"><span data-stu-id="5c048-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="5c048-111">Gibt die DVD-Audiosprach Erweiterung als ganzzahligen Wert an.</span><span class="sxs-lookup"><span data-stu-id="5c048-111">Specifies the DVD audio language extension as an integer value.</span></span>



| <span data-ttu-id="5c048-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5c048-112">Value</span></span> | <span data-ttu-id="5c048-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c048-113">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="5c048-114">0</span><span class="sxs-lookup"><span data-stu-id="5c048-114">0</span></span>     | <span data-ttu-id="5c048-115">NotSpecified</span><span class="sxs-lookup"><span data-stu-id="5c048-115">NotSpecified</span></span>      |
| <span data-ttu-id="5c048-116">1</span><span class="sxs-lookup"><span data-stu-id="5c048-116">1</span></span>     | <span data-ttu-id="5c048-117">Untertitel</span><span class="sxs-lookup"><span data-stu-id="5c048-117">Captions</span></span>          |
| <span data-ttu-id="5c048-118">2</span><span class="sxs-lookup"><span data-stu-id="5c048-118">2</span></span>     | <span data-ttu-id="5c048-119">Visualisierungen beeinträchtigt</span><span class="sxs-lookup"><span data-stu-id="5c048-119">VisuallyImpaired</span></span>  |
| <span data-ttu-id="5c048-120">3</span><span class="sxs-lookup"><span data-stu-id="5c048-120">3</span></span>     | <span data-ttu-id="5c048-121">DirectorComments1</span><span class="sxs-lookup"><span data-stu-id="5c048-121">DirectorComments1</span></span> |
| <span data-ttu-id="5c048-122">4</span><span class="sxs-lookup"><span data-stu-id="5c048-122">4</span></span>     | <span data-ttu-id="5c048-123">DirectorComments2</span><span class="sxs-lookup"><span data-stu-id="5c048-123">DirectorComments2</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c048-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c048-124">Return Value</span></span>

<span data-ttu-id="5c048-125">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="5c048-125">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c048-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c048-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c048-127">Mswebdvd-Objekt</span><span class="sxs-lookup"><span data-stu-id="5c048-127">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



