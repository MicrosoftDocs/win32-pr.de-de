---
title: VML preferrelative-Attribut
description: VML preferrelative-Attribut
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039084"
---
# <a name="vml-preferrelative-attribute"></a><span data-ttu-id="3e660-103">VML preferrelative-Attribut</span><span class="sxs-lookup"><span data-stu-id="3e660-103">VML PreferRelative Attribute</span></span>

<span data-ttu-id="3e660-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3e660-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3e660-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3e660-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3e660-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3e660-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3e660-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3e660-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3e660-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3e660-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3e660-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3e660-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3e660-110">Bestimmt, ob die ursprüngliche Größe eines Objekts nach der Neuformatierung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="3e660-110">Determines whether the original size of an object is saved after reformatting.</span></span> <span data-ttu-id="3e660-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3e660-111">Read/write.</span></span> <span data-ttu-id="3e660-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="3e660-112">**VgTriState**.</span></span>

<span data-ttu-id="3e660-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3e660-113">**Applies To**</span></span>

[<span data-ttu-id="3e660-114">Form</span><span class="sxs-lookup"><span data-stu-id="3e660-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3e660-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3e660-115">**Tag Syntax**</span></span>

<span data-ttu-id="3e660-116"><v: *Element* o:preferrelative = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3e660-116"><v: *element* o:preferrelative=" *expression* "></span></span>

<span data-ttu-id="3e660-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3e660-117">**Remarks**</span></span>

<span data-ttu-id="3e660-118">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="3e660-118">The default is **False**.</span></span> <span data-ttu-id="3e660-119">Wenn der Wert **true** ist, wird die ursprüngliche Größe des Objekts gespeichert, und die Größenänderung basiert auf einem Prozentsatz der ursprünglichen Größe.</span><span class="sxs-lookup"><span data-stu-id="3e660-119">If **True**, the original size of the object will be stored and all resizing will be based on a percentage of that original size.</span></span> <span data-ttu-id="3e660-120">Andernfalls wird die Skalierung durch jede Größenänderung auf 100% zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3e660-120">Otherwise, each resizing will reset the scale to 100%.</span></span>

<span data-ttu-id="3e660-121">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="3e660-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="3e660-122">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3e660-122">**Example**</span></span>

<span data-ttu-id="3e660-123">Wenn die Größe der Form geändert wird, wird die ursprüngliche Größe nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3e660-123">If the shape is resized, the original size will not be stored.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 