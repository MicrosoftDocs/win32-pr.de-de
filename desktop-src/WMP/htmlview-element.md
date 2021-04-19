---
title: HtmlView-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das HtmlView-Element gibt die Basis-URL einer HtmlView-Webseite an.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- HtmlView-Element, Windows-Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372374"
---
# <a name="htmlview-element"></a><span data-ttu-id="9e462-106">HtmlView-Element</span><span class="sxs-lookup"><span data-stu-id="9e462-106">HTMLView Element</span></span>

> [!Note]  
> <span data-ttu-id="9e462-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="9e462-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9e462-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e462-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9e462-109">Das **HtmlView** -Element gibt die Basis-URL einer HtmlView-Webseite an.</span><span class="sxs-lookup"><span data-stu-id="9e462-109">The **HTMLView** element specifies the base URL of an HTMLView webpage.</span></span>

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="9e462-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="9e462-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="9e462-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**Baseurl** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9e462-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="9e462-112">Basis-URL für die von Windows Media Player angezeigte HtmlView-Webseite.</span><span class="sxs-lookup"><span data-stu-id="9e462-112">Base URL for the HTMLView webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="9e462-113">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="9e462-113">Parent/Child Elements</span></span>



| <span data-ttu-id="9e462-114">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="9e462-114">Hierarchy</span></span>       | <span data-ttu-id="9e462-115">Element</span><span class="sxs-lookup"><span data-stu-id="9e462-115">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="9e462-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e462-116">Parent elements</span></span> | <span data-ttu-id="9e462-117">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9e462-117">**ServiceInfo**</span></span> |
| <span data-ttu-id="9e462-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e462-118">Child elements</span></span>  | <span data-ttu-id="9e462-119">Keine</span><span class="sxs-lookup"><span data-stu-id="9e462-119">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="9e462-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e462-120">Remarks</span></span>

<span data-ttu-id="9e462-121">Sie können dieses Element verwenden, um die HtmlView-Funktion in Ihren Online Store zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="9e462-121">You can use this element to integrate the HTMLView feature with your online store.</span></span> <span data-ttu-id="9e462-122">Wenn die Domäne der URL, die im aktuellen Onlinespeicher angegeben ist, mit der Domäne der HtmlView-Webseite übereinstimmt, erfolgt die wieder **Gabe jetzt** ohne Benutzereingriff, und der HtmlView-Inhalt wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e462-122">If the domain of the URL specified by the current online store matches the one for the HTMLView webpage, the switch to **Now Playing** happens without user intervention and the HTMLView content is displayed.</span></span> <span data-ttu-id="9e462-123">Andernfalls fordert Windows Media Player den Benutzer zur Eingabe der Berechtigung auf, den HtmlView-Inhalt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9e462-123">Otherwise, Windows Media Player prompts the user for permission to show the HTMLView content.</span></span>

<span data-ttu-id="9e462-124">Wenn beispielsweise die URL für die HtmlView-Webseite lautet https://www.proseware.com/html/HTMLView.htm und die URL für das **baseurl** -Attribut als angegeben wird https://www.proseware.com , wird die HtmlView-Webseite angezeigt, ohne den Benutzer aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="9e462-124">For example, if the URL for the HTMLView webpage is https://www.proseware.com/html/HTMLView.htm and the URL for the **BaseURL** attribute is specified as https://www.proseware.com, the HTMLView webpage displays without prompting the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e462-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e462-125">Requirements</span></span>



| <span data-ttu-id="9e462-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e462-126">Requirement</span></span> | <span data-ttu-id="9e462-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9e462-127">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="9e462-128">Version</span><span class="sxs-lookup"><span data-stu-id="9e462-128">Version</span></span><br/> | <span data-ttu-id="9e462-129">Windows Media Player 10 oder höher</span><span class="sxs-lookup"><span data-stu-id="9e462-129">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e462-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e462-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e462-131">**Anzeigen von Webseiten in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="9e462-131">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="9e462-132">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="9e462-132">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="9e462-133">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="9e462-133">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="9e462-134">**Param-Element**</span><span class="sxs-lookup"><span data-stu-id="9e462-134">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="9e462-135">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="9e462-135">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





