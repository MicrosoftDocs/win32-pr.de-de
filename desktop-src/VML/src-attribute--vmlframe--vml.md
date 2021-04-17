---
title: Src-Attribut (vmlframe) (VML)
description: Src-Attribut (vmlframe) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315494"
---
# <a name="src-attribute-vmlframevml"></a><span data-ttu-id="05ec0-103">Src-Attribut (vmlframe) (VML)</span><span class="sxs-lookup"><span data-stu-id="05ec0-103">Src Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="05ec0-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="05ec0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="05ec0-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="05ec0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="05ec0-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="05ec0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="05ec0-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="05ec0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="05ec0-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="05ec0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="05ec0-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="05ec0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="05ec0-110">Definiert die Datenquelle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="05ec0-110">Defines the source of data for the frame.</span></span> <span data-ttu-id="05ec0-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="05ec0-111">Read/write.</span></span> <span data-ttu-id="05ec0-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="05ec0-112">**String**.</span></span>

<span data-ttu-id="05ec0-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="05ec0-113">**Applies To**</span></span>

[<span data-ttu-id="05ec0-114">Vmlframe</span><span class="sxs-lookup"><span data-stu-id="05ec0-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="05ec0-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="05ec0-115">**Tag Syntax**</span></span>

<span data-ttu-id="05ec0-116"><v: *Element* src = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="05ec0-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="05ec0-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="05ec0-117">**Script Syntax**</span></span>

<span data-ttu-id="05ec0-118">*Element* . src = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="05ec0-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="05ec0-119">*Ausdruck* = *Element*. src</span><span class="sxs-lookup"><span data-stu-id="05ec0-119">*expression*=*element*.src</span></span>

<span data-ttu-id="05ec0-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="05ec0-120">**Remarks**</span></span>

<span data-ttu-id="05ec0-121">Das **src** -Attribut kann die folgenden Syntaxen einschließen:</span><span class="sxs-lookup"><span data-stu-id="05ec0-121">The **Src** attribute can involve the following syntaxes:</span></span>

-   <span data-ttu-id="05ec0-122">URL zu externer Datei.</span><span class="sxs-lookup"><span data-stu-id="05ec0-122">URL to external file.</span></span> <span data-ttu-id="05ec0-123">Die Datei muss eine XML-Datei mit folgendem Format sein:</span><span class="sxs-lookup"><span data-stu-id="05ec0-123">The file must be an XML file with the following format:</span></span>
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   <span data-ttu-id="05ec0-124">In der Datei müssen Sie über eine oder mehrere VML-Formen mit gültigen IDs verfügen, auf die mit der folgenden Syntax verwiesen werden kann:</span><span class="sxs-lookup"><span data-stu-id="05ec0-124">Inside the file you must have one or more VML shapes with valid IDs that can be referenced by using this syntax:</span></span>
    ```HTML
       filename#shapename
    ```

    

-   <span data-ttu-id="05ec0-125">In der folgenden Referenz haben externe Dateien die Erweiterung. VML, aber es kann eine beliebige Erweiterung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="05ec0-125">In the following reference, external files have the .vml extension, but any extension can be used:</span></span>
    ```HTML
       external.vml#image01
    ```

    

-   <span data-ttu-id="05ec0-126">Sie können auf eine Form innerhalb derselben Datei verweisen, indem Sie die folgende Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="05ec0-126">You can reference a shape within the same file by using the following syntax:</span></span>
    ```HTML
       #shapename
    ```

    

<span data-ttu-id="05ec0-127">Wenn **Clip** **false** ist, wird die Form so skaliert, dass Sie dem Frame entspricht.</span><span class="sxs-lookup"><span data-stu-id="05ec0-127">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="05ec0-128">**True** gibt an, dass Teile der Form, die sich außerhalb des Rahmens befinden, nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="05ec0-128">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="05ec0-129">Beachten Sie, dass [Origin](origin-attribute--vmlframe--vml.md) und [size](size-attribute--vmlframe.md) nicht verwendet werden, es sei denn, **Clip** ist **true**.</span><span class="sxs-lookup"><span data-stu-id="05ec0-129">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="05ec0-130">**VML-Standard Attribut**</span><span class="sxs-lookup"><span data-stu-id="05ec0-130">**VML Standard Attribute**</span></span>

<span data-ttu-id="05ec0-131">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="05ec0-131">**Example**</span></span>

<span data-ttu-id="05ec0-132">Das in der externen Datei definierte Bild wird abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="05ec0-132">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 