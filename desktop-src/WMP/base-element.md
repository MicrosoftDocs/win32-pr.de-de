---
title: Basis Element
description: Das Basiselement definiert eine URL-Zeichenfolge, die an den Anfang der an Windows Media Player gesendeten URLs angehängt ist.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Windows-Basis Element Media Player
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372651"
---
# <a name="base-element"></a><span data-ttu-id="e9f0f-104">Basis Element</span><span class="sxs-lookup"><span data-stu-id="e9f0f-104">BASE Element</span></span>

<span data-ttu-id="e9f0f-105">Das **Basis** Element definiert eine URL-Zeichenfolge, die an den Anfang der an Windows Media Player gesendeten URLs angehängt ist.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-105">The **BASE** element defines a URL string appended to the front of URLs sent to Windows Media Player.</span></span>

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="e9f0f-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="e9f0f-106">Attributes</span></span>

<span data-ttu-id="e9f0f-107">**Href** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="e9f0f-107">**HREF** (required)</span></span>

<span data-ttu-id="e9f0f-108">Die Zeichenfolge, die an den Anfang an die an Windows Media Player gesendeten URLs angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-108">The string appended to the front to URLs sent to Windows Media Player.</span></span> <span data-ttu-id="e9f0f-109">Der Standardwert ist die NULL-Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="e9f0f-109">The default value is the null string ("").</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="e9f0f-110">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="e9f0f-110">Parent/Child Elements</span></span>



| <span data-ttu-id="e9f0f-111">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e9f0f-111">Hierarchy</span></span>       | <span data-ttu-id="e9f0f-112">Elemente</span><span class="sxs-lookup"><span data-stu-id="e9f0f-112">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="e9f0f-113">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9f0f-113">Parent elements</span></span> | <span data-ttu-id="e9f0f-114">**ASX**, **Eintrag**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-114">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="e9f0f-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9f0f-115">Child elements</span></span>  | <span data-ttu-id="e9f0f-116">Keine</span><span class="sxs-lookup"><span data-stu-id="e9f0f-116">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="e9f0f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9f0f-117">Remarks</span></span>

<span data-ttu-id="e9f0f-118">Dieses Element definiert eine URL-Zeichenfolge, die an den Anfang der URL-Flip-URLs angehängt wird, die an Windows Media Player gesendet werden</span><span class="sxs-lookup"><span data-stu-id="e9f0f-118">This element defines a URL string appended to the front of URL-flip URLs sent to Windows Media Player.</span></span> <span data-ttu-id="e9f0f-119">Beim URL-Flipping handelt es sich um einen Skript Mechanismus, der bewirkt, dass Windows Media Player eine neue URL in einem Browser-oder Browser Rahmen öffnet, wenn ein Skript Befehl empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-119">URL-flipping is a scripting mechanism that causes Windows Media Player to open a new URL in a browser or browser frame when it receives a script command.</span></span>

<span data-ttu-id="e9f0f-120">Das **Basis** Element ähnelt einem Basisverzeichnis für relative Links.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-120">The **BASE** element is similar to a home directory for relative links.</span></span> <span data-ttu-id="e9f0f-121">Sie wirkt sich nur auf URLs aus, die mithilfe von Skript Befehlen als Teil des Inhaltsdaten Stroms gesendet werden, der in Windows Media Player abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-121">It only affects URLs sent using script commands as part of the content stream that is playing in Windows Media Player.</span></span>

<span data-ttu-id="e9f0f-122">Ein **Basis** Element, das als untergeordnetes Element eines **ASX** -Elements definiert ist, wird zum Standardwert für die gesamte Metadatendatei.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-122">A **BASE** element defined as the child of an **ASX** element becomes the default for the entire metafile.</span></span> <span data-ttu-id="e9f0f-123">Ein **Basis** Element, das in einem **Entry** -Element definiert ist, überschreibt jedes **Basis** Element im übergeordneten **ASX** -Element (nur für dieses **Eintrags** Element).</span><span class="sxs-lookup"><span data-stu-id="e9f0f-123">A **BASE** element defined in an **ENTRY** element overrides any **BASE** element in the parent **ASX** element (for that **ENTRY** element only).</span></span>

> [!Note]  
> <span data-ttu-id="e9f0f-124">Wenn das **href** -Attribut nicht mit einem/-Zeichen endet, fügt Windows Media Player ein an das Ende der Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-124">If the **HREF** attribute does not end with a / character, Windows Media Player appends one to the end of the string.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e9f0f-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9f0f-125">Examples</span></span>


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a><span data-ttu-id="e9f0f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9f0f-126">Requirements</span></span>



| <span data-ttu-id="e9f0f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9f0f-127">Requirement</span></span> | <span data-ttu-id="e9f0f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e9f0f-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e9f0f-129">Version</span><span class="sxs-lookup"><span data-stu-id="e9f0f-129">Version</span></span><br/> | <span data-ttu-id="e9f0f-130">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e9f0f-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9f0f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9f0f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f0f-132">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="e9f0f-133">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





