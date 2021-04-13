---
title: VML-Zeichen folgen Attribut
description: VML-Zeichen folgen Attribut
ms.assetid: 99609814-29c9-4349-9509-8c91f2aaeff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6c172b4ca1f5049a3e89528a2333378164f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390585"
---
# <a name="vml-string-attribute"></a><span data-ttu-id="a4e06-103">VML-Zeichen folgen Attribut</span><span class="sxs-lookup"><span data-stu-id="a4e06-103">VML String Attribute</span></span>

<span data-ttu-id="a4e06-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a4e06-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a4e06-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a4e06-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a4e06-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a4e06-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a4e06-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a4e06-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a4e06-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a4e06-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a4e06-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a4e06-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a4e06-110">Definiert den Text des Textpfads.</span><span class="sxs-lookup"><span data-stu-id="a4e06-110">Defines the text of the text path.</span></span> <span data-ttu-id="a4e06-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a4e06-111">Read/write.</span></span> <span data-ttu-id="a4e06-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="a4e06-112">**String**.</span></span>

<span data-ttu-id="a4e06-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a4e06-113">**Applies To**</span></span>

[<span data-ttu-id="a4e06-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="a4e06-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="a4e06-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a4e06-115">**Tag Syntax**</span></span>

<span data-ttu-id="a4e06-116"><v: *Element* String = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a4e06-116"><v: *element* string=" *expression* "></span></span>

<span data-ttu-id="a4e06-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="a4e06-117">**Script Syntax**</span></span>

<span data-ttu-id="a4e06-118">*Element* . String = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="a4e06-118">*element* .string="*expression*"</span></span>

<span data-ttu-id="a4e06-119">*Ausdruck* = *Element*. String</span><span class="sxs-lookup"><span data-stu-id="a4e06-119">*expression*=*element*.string</span></span>

<span data-ttu-id="a4e06-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a4e06-120">**Remarks**</span></span>

<span data-ttu-id="a4e06-121">Sie müssen eine Text Zeichenfolge zum Anzeigen von Text in einem Textpfad zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a4e06-121">You must assign a text string to display text on a text path.</span></span>

<span data-ttu-id="a4e06-122">VML-Standard Attribut</span><span class="sxs-lookup"><span data-stu-id="a4e06-122">VML Standard Attribute</span></span>

<span data-ttu-id="a4e06-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a4e06-123">**Example**</span></span>

<span data-ttu-id="a4e06-124">Die Zeichenfolge, die angezeigt wird, ist "VML-Text".</span><span class="sxs-lookup"><span data-stu-id="a4e06-124">The string that will be displayed is "VML Text".</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 