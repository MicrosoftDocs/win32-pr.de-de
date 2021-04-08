---
description: Die selectdefaultsubpicturelanguage-Methode legt die aktuelle Standardsprache des unter Bilds im mswebdvd-Objekt fest.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Selectdefaultsubpicturelanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746248"
---
# <a name="selectdefaultsubpicturelanguage-method"></a><span data-ttu-id="7df7d-103">Selectdefaultsubpicturelanguage-Methode</span><span class="sxs-lookup"><span data-stu-id="7df7d-103">SelectDefaultSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="7df7d-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7df7d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7df7d-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7df7d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7df7d-106">Die- `SelectDefaultSubpictureLanguage` Methode legt die aktuelle Standardsprache des unter Bilds im **mswebdvd** -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="7df7d-106">The `SelectDefaultSubpictureLanguage` method sets the current default subpicture language in the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a><span data-ttu-id="7df7d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7df7d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df7d-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*ilang*</span><span class="sxs-lookup"><span data-stu-id="7df7d-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="7df7d-109">Gibt die Sprache als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="7df7d-109">Specifies the language as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="7df7d-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iext*</span><span class="sxs-lookup"><span data-stu-id="7df7d-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="7df7d-111">Gibt die unter Bild Spracherweiterung als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="7df7d-111">Specifies the subpicture language extension as an Integer.</span></span>



| <span data-ttu-id="7df7d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="7df7d-112">Value</span></span> | <span data-ttu-id="7df7d-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7df7d-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="7df7d-114">0</span><span class="sxs-lookup"><span data-stu-id="7df7d-114">0</span></span>     | <span data-ttu-id="7df7d-115">Erweiterung nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="7df7d-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="7df7d-116">1</span><span class="sxs-lookup"><span data-stu-id="7df7d-116">1</span></span>     | <span data-ttu-id="7df7d-117">Normale Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="7df7d-117">Normal Captions</span></span>                |
| <span data-ttu-id="7df7d-118">2</span><span class="sxs-lookup"><span data-stu-id="7df7d-118">2</span></span>     | <span data-ttu-id="7df7d-119">Große Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="7df7d-119">Big Captions</span></span>                   |
| <span data-ttu-id="7df7d-120">3</span><span class="sxs-lookup"><span data-stu-id="7df7d-120">3</span></span>     | <span data-ttu-id="7df7d-121">Untergeordnete Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="7df7d-121">Children's Captions</span></span>            |
| <span data-ttu-id="7df7d-122">5</span><span class="sxs-lookup"><span data-stu-id="7df7d-122">5</span></span>     | <span data-ttu-id="7df7d-123">Normale Untertitel</span><span class="sxs-lookup"><span data-stu-id="7df7d-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="7df7d-124">6</span><span class="sxs-lookup"><span data-stu-id="7df7d-124">6</span></span>     | <span data-ttu-id="7df7d-125">Big Closed-Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="7df7d-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="7df7d-126">7</span><span class="sxs-lookup"><span data-stu-id="7df7d-126">7</span></span>     | <span data-ttu-id="7df7d-127">Untertitel der untergeordneten Elemente</span><span class="sxs-lookup"><span data-stu-id="7df7d-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="7df7d-128">9</span><span class="sxs-lookup"><span data-stu-id="7df7d-128">9</span></span>     | <span data-ttu-id="7df7d-129">Erzwungen</span><span class="sxs-lookup"><span data-stu-id="7df7d-129">Forced</span></span>                         |
| <span data-ttu-id="7df7d-130">13</span><span class="sxs-lookup"><span data-stu-id="7df7d-130">13</span></span>    | <span data-ttu-id="7df7d-131">Kommentare des normalen Direktors</span><span class="sxs-lookup"><span data-stu-id="7df7d-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="7df7d-132">14</span><span class="sxs-lookup"><span data-stu-id="7df7d-132">14</span></span>    | <span data-ttu-id="7df7d-133">Kommentare zu Big Director</span><span class="sxs-lookup"><span data-stu-id="7df7d-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="7df7d-134">15</span><span class="sxs-lookup"><span data-stu-id="7df7d-134">15</span></span>    | <span data-ttu-id="7df7d-135">Die Kommentare der untergeordneten Elemente</span><span class="sxs-lookup"><span data-stu-id="7df7d-135">Children's Director's Comments</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df7d-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7df7d-136">Return Value</span></span>

<span data-ttu-id="7df7d-137">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="7df7d-137">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df7d-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7df7d-138">Remarks</span></span>

<span data-ttu-id="7df7d-139">Die unter Bilder-Spracherweiterung bietet weitere Informationen über das untergeordnete Bild.</span><span class="sxs-lookup"><span data-stu-id="7df7d-139">The subpicture language extension provides further information about the subpicture.</span></span>

 

 



