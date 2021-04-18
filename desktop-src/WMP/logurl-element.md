---
title: LogURL-Element
description: Das LogURL-Element weist Windows Media Player an, beliebige Protokolldaten an die angegebene URL zu senden.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Windows-Media Player für das LogURL-Element
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358394"
---
# <a name="logurl-element"></a><span data-ttu-id="dcdc8-104">LogURL-Element</span><span class="sxs-lookup"><span data-stu-id="dcdc8-104">LOGURL Element</span></span>

<span data-ttu-id="dcdc8-105">Das **LogURL** -Element weist Windows Media Player an, beliebige Protokolldaten an die angegebene URL zu senden.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-105">The **LOGURL** element instructs Windows Media Player to submit any log data to the specified URL.</span></span>

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="dcdc8-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="dcdc8-106">Attributes</span></span>

<span data-ttu-id="dcdc8-107">**Href** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="dcdc8-107">**HREF** (required)</span></span>

<span data-ttu-id="dcdc8-108">Die URL zu einem Host, der Protokollierungs Anforderungen verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-108">URL to a host that is able to process logging requests.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="dcdc8-109">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="dcdc8-109">Parent/Child Elements</span></span>



| <span data-ttu-id="dcdc8-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="dcdc8-110">Hierarchy</span></span>       | <span data-ttu-id="dcdc8-111">Elemente</span><span class="sxs-lookup"><span data-stu-id="dcdc8-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="dcdc8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dcdc8-112">Parent elements</span></span> | <span data-ttu-id="dcdc8-113">**ASX**, **Eintrag**</span><span class="sxs-lookup"><span data-stu-id="dcdc8-113">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="dcdc8-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dcdc8-114">Child elements</span></span>  | <span data-ttu-id="dcdc8-115">Keine</span><span class="sxs-lookup"><span data-stu-id="dcdc8-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="dcdc8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcdc8-116">Remarks</span></span>

<span data-ttu-id="dcdc8-117">Das **LogURL** -Element ermöglicht es einer clientmetadatendatei-Wiedergabeliste, zusätzliche Protokollierungs Informationen an bestimmte Server zu senden.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-117">The **LOGURL** element enables a client metafile playlist to send additional logging information to specified servers.</span></span> <span data-ttu-id="dcdc8-118">Protokollierungs Informationen werden automatisch an den Ursprungsserver einer Wiedergabeliste gesendet, wenn Sie geöffnet wird, sowie an jede **LogURL** , die für das Element " **ASX** " angegeben ist (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="dcdc8-118">Logging information is automatically sent to the origin server of a playlist when it is opened and to each **LOGURL** specified for the **ASX** element, if any are present.</span></span> <span data-ttu-id="dcdc8-119">Protokollierungs Informationen werden auch an jede **LogURL** gesendet, die für ein **Entry** -Element angegeben ist, wenn dieser Eintrag erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-119">Logging information is also sent to each **LOGURL** specified for an **ENTRY** element when that entry is reached.</span></span> <span data-ttu-id="dcdc8-120">Die URL, die im **href** -Attribut eines **LogURL** -Elements angegeben ist, muss die Adresse eines Hosts sein, der Protokollierungs Anforderungen verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-120">The URL specified in the **HREF** attribute of a **LOGURL** element must be the address of a host that is able to process logging requests.</span></span> <span data-ttu-id="dcdc8-121">Die URL kann eine beliebige gültige HTTP-URL sein.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-121">The URL can be any valid HTTP URL.</span></span> <span data-ttu-id="dcdc8-122">Die URL kann auch den Speicherort eines CGI-Skripts angeben.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-122">The URL can also indicate the location of a CGI script.</span></span>

<span data-ttu-id="dcdc8-123">Die einzigen gültigen Protokolle für ein **LogURL** -Element sind http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-123">The only valid protocols for a **LOGURL** element are HTTP and HTTPS.</span></span>

<span data-ttu-id="dcdc8-124">Ein **LogURL** -Element innerhalb des Gültigkeits Bereichs eines **ASX** -Elements ist nur auf die Metadatendatei anwendbar, in der es sich befindet, unabhängig davon, ob auf diese Metadatendatei von einer anderen Metadatei verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-124">A **LOGURL** element within the scope of an **ASX** element is applicable only to the metafile in which it resides, regardless of whether that metafile is referenced from another metafile.</span></span> <span data-ttu-id="dcdc8-125">Ein **LogURL** -Element erzwingt die Übermittlung von Protokolldaten für alle Inhalte, die aus dem definierten Bereich gestreamt werden, und nur für Inhalte, die aus dem definierten Bereich gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-125">A **LOGURL** element forces the submission of log data for all content streamed from within its defined scope and only for content streamed from within its defined scope.</span></span> <span data-ttu-id="dcdc8-126">Protokolldaten werden an den Ursprungsserver und an alle URLs übermittelt, die in jedem **LogURL** -Element im Gültigkeitsbereich aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-126">Log data will be submitted to the origin server and to all URLs listed in every **LOGURL** element in scope.</span></span> <span data-ttu-id="dcdc8-127">Protokolldaten werden nur einmal an jede aufgelistete URL übermittelt, auch wenn die gleiche URL mehrmals in einem bestimmten Bereich aufgelistet ist.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-127">Log data will be submitted only once to each listed URL, even if the same URL is listed more than once in a given scope.</span></span> <span data-ttu-id="dcdc8-128">Eine Wiederholung eines **Eintrags** führt zu einer weiteren Übermittlung an die aufgelisteten URLs.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-128">A repeat of an **ENTRY** would result in another submission to the listed URLs.</span></span>

<span data-ttu-id="dcdc8-129">Es gibt keine Beschränkung für die Anzahl der **LogURL** -Elemente in einer Metadatei-Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-129">There is no limit to the number of **LOGURL** elements in a metafile playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="dcdc8-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dcdc8-130">Examples</span></span>


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



<span data-ttu-id="dcdc8-131">Im folgenden finden Sie Beispiele für gültige URLs.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-131">The following are examples of valid URLs.</span></span>

<span data-ttu-id="dcdc8-132">URL einer ISAPI-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="dcdc8-132">URL of an ISAPI application:</span></span>


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



<span data-ttu-id="dcdc8-133">URL eines CGI-Skripts:</span><span class="sxs-lookup"><span data-stu-id="dcdc8-133">URL of a CGI script:</span></span>


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



<span data-ttu-id="dcdc8-134">Eine gültige HTTP-URL:</span><span class="sxs-lookup"><span data-stu-id="dcdc8-134">A valid HTTP URL:</span></span>


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a><span data-ttu-id="dcdc8-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcdc8-135">Requirements</span></span>



| <span data-ttu-id="dcdc8-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcdc8-136">Requirement</span></span> | <span data-ttu-id="dcdc8-137">Wert</span><span class="sxs-lookup"><span data-stu-id="dcdc8-137">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="dcdc8-138">Version</span><span class="sxs-lookup"><span data-stu-id="dcdc8-138">Version</span></span><br/> | <span data-ttu-id="dcdc8-139">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="dcdc8-139">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dcdc8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcdc8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcdc8-141">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="dcdc8-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="dcdc8-142">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="dcdc8-142">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





