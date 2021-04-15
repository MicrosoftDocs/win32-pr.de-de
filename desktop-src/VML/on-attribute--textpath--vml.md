---
title: On-Attribut (TextPath) (VML)
description: On-Attribut (TextPath) (VML)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ae791b1144046a1c29e92d11663cd15d696bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517090"
---
# <a name="on-attribute-textpathvml"></a><span data-ttu-id="18a49-103">On-Attribut (TextPath) (VML)</span><span class="sxs-lookup"><span data-stu-id="18a49-103">On Attribute (TextPath)(VML)</span></span>

<span data-ttu-id="18a49-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="18a49-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="18a49-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="18a49-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="18a49-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="18a49-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="18a49-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="18a49-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="18a49-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="18a49-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="18a49-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="18a49-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="18a49-110">Definiert, ob der Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="18a49-110">Defines whether the text is displayed.</span></span> <span data-ttu-id="18a49-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="18a49-111">Read/write.</span></span> <span data-ttu-id="18a49-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="18a49-112">**VgTriState**.</span></span>

<span data-ttu-id="18a49-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="18a49-113">**Applies To**</span></span>

[<span data-ttu-id="18a49-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="18a49-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="18a49-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="18a49-115">**Tag Syntax**</span></span>

<span data-ttu-id="18a49-116"><v: *Element* on = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="18a49-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="18a49-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="18a49-117">**Script Syntax**</span></span>

<span data-ttu-id="18a49-118">*Element* . on = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="18a49-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="18a49-119">*Ausdruck* = *Element*. on</span><span class="sxs-lookup"><span data-stu-id="18a49-119">*expression*=*element*.on</span></span>

<span data-ttu-id="18a49-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="18a49-120">**Remarks**</span></span>

<span data-ttu-id="18a49-121">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="18a49-121">Default is **False**.</span></span> <span data-ttu-id="18a49-122">Dieser Wert muss auf **true** festgelegt werden, um Text in einem Textpfad anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="18a49-122">This value must be set to **True** to display text on a text path.</span></span>

<span data-ttu-id="18a49-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="18a49-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="18a49-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="18a49-124">**Example**</span></span>

<span data-ttu-id="18a49-125">Der Text im Textpfad wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18a49-125">The text on the text path will be displayed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 