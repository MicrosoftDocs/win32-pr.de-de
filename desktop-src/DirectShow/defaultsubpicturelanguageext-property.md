---
description: Die defaultsubpicturelanguageext-Eigenschaft ruft die standardmäßige DVD-unter Bild Spracherweiterung ab.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Defaultsubpicturelanguageext (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520747"
---
# <a name="defaultsubpicturelanguageext-property"></a><span data-ttu-id="6f490-103">Defaultsubpicturelanguageext (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6f490-103">DefaultSubpictureLanguageExt Property</span></span>

> [!Note]  
> <span data-ttu-id="6f490-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f490-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6f490-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6f490-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6f490-106">Die- `DefaultSubpictureLanguageExt` Eigenschaft ruft die standardmäßige DVD-unter Bild Spracherweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="6f490-106">The `DefaultSubpictureLanguageExt` property retrieves the default DVD subpicture language extension.</span></span>

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a><span data-ttu-id="6f490-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f490-107">Return Value</span></span>

<span data-ttu-id="6f490-108">Gibt einen ganzzahligen Wert zurück, der die standardmäßige DVD-unter Bild Spracherweiterung angibt</span><span class="sxs-lookup"><span data-stu-id="6f490-108">Returns an Integer value indicating the default DVD subpicture language extension.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f490-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f490-109">Remarks</span></span>

<span data-ttu-id="6f490-110">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="6f490-110">This property is read-only with no default value.</span></span> <span data-ttu-id="6f490-111">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f490-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="6f490-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6f490-112">Value</span></span> | <span data-ttu-id="6f490-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f490-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="6f490-114">0</span><span class="sxs-lookup"><span data-stu-id="6f490-114">0</span></span>     | <span data-ttu-id="6f490-115">Erweiterung nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="6f490-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="6f490-116">1</span><span class="sxs-lookup"><span data-stu-id="6f490-116">1</span></span>     | <span data-ttu-id="6f490-117">Normale Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="6f490-117">Normal Captions</span></span>                |
| <span data-ttu-id="6f490-118">2</span><span class="sxs-lookup"><span data-stu-id="6f490-118">2</span></span>     | <span data-ttu-id="6f490-119">Große Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="6f490-119">Big Captions</span></span>                   |
| <span data-ttu-id="6f490-120">3</span><span class="sxs-lookup"><span data-stu-id="6f490-120">3</span></span>     | <span data-ttu-id="6f490-121">Untergeordnete Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="6f490-121">Children's Captions</span></span>            |
| <span data-ttu-id="6f490-122">5</span><span class="sxs-lookup"><span data-stu-id="6f490-122">5</span></span>     | <span data-ttu-id="6f490-123">Normale Untertitel</span><span class="sxs-lookup"><span data-stu-id="6f490-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="6f490-124">6</span><span class="sxs-lookup"><span data-stu-id="6f490-124">6</span></span>     | <span data-ttu-id="6f490-125">Big Closed-Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="6f490-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="6f490-126">7</span><span class="sxs-lookup"><span data-stu-id="6f490-126">7</span></span>     | <span data-ttu-id="6f490-127">Untertitel der untergeordneten Elemente</span><span class="sxs-lookup"><span data-stu-id="6f490-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="6f490-128">9</span><span class="sxs-lookup"><span data-stu-id="6f490-128">9</span></span>     | <span data-ttu-id="6f490-129">Erzwungen</span><span class="sxs-lookup"><span data-stu-id="6f490-129">Forced</span></span>                         |
| <span data-ttu-id="6f490-130">13</span><span class="sxs-lookup"><span data-stu-id="6f490-130">13</span></span>    | <span data-ttu-id="6f490-131">Kommentare des normalen Direktors</span><span class="sxs-lookup"><span data-stu-id="6f490-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="6f490-132">14</span><span class="sxs-lookup"><span data-stu-id="6f490-132">14</span></span>    | <span data-ttu-id="6f490-133">Kommentare zu Big Director</span><span class="sxs-lookup"><span data-stu-id="6f490-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="6f490-134">15</span><span class="sxs-lookup"><span data-stu-id="6f490-134">15</span></span>    | <span data-ttu-id="6f490-135">Die Kommentare der untergeordneten Elemente</span><span class="sxs-lookup"><span data-stu-id="6f490-135">Children's Director's Comments</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="6f490-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f490-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f490-137">**Selectdefaultsubpicturelanguage**</span><span class="sxs-lookup"><span data-stu-id="6f490-137">**SelectDefaultSubpictureLanguage**</span></span>](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



