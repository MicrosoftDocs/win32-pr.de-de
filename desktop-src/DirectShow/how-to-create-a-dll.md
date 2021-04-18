---
description: Erstellen einer DirectShow-Filter-dll
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Erstellen einer DirectShow-Filter-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344771"
---
# <a name="how-to-create-a-directshow-filter-dll"></a><span data-ttu-id="c20fe-103">Erstellen einer DirectShow-Filter-dll</span><span class="sxs-lookup"><span data-stu-id="c20fe-103">How to Create a DirectShow Filter DLL</span></span>

<span data-ttu-id="c20fe-104">In diesem Artikel wird beschrieben, wie eine Komponente in Microsoft DirectShow als Dynamic Link Library (dll) implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="c20fe-104">This article describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span> <span data-ttu-id="c20fe-105">Dieser Artikel ist eine Fortsetzung der [Implementierung von IUnknown](how-to-implement-iunknown.md), in der beschrieben wird, wie Sie die **IUnknown** -Schnittstelle implementieren, indem Sie die Komponente von der [**cunknown**](cunknown.md) -Basisklasse ableiten.</span><span class="sxs-lookup"><span data-stu-id="c20fe-105">This article is a continuation from [How to Implement IUnknown](how-to-implement-iunknown.md), which describes how to implement the **IUnknown** interface by deriving your component from the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="c20fe-106">Dieser Artikel enthält folgende Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="c20fe-106">This article contains the following sections.</span></span>

-   [<span data-ttu-id="c20fe-107">Klassen-und factoryvorlagen</span><span class="sxs-lookup"><span data-stu-id="c20fe-107">Class Factories and Factory Templates</span></span>](class-factories-and-factory-templates.md)
-   [<span data-ttu-id="c20fe-108">Factory-Vorlagen Array</span><span class="sxs-lookup"><span data-stu-id="c20fe-108">Factory Template Array</span></span>](factory-template-array.md)
-   [<span data-ttu-id="c20fe-109">DLL-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c20fe-109">DLL Functions</span></span>](dll-functions.md)

<span data-ttu-id="c20fe-110">Das Registrieren eines DirectShow-Filters (im Gegensatz zu einem generischen com-Objekt) erfordert einige zusätzliche Schritte, die in diesem Artikel nicht behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c20fe-110">Registering a DirectShow filter (as opposed to a generic COM object) requires some additional steps that are not covered in this article.</span></span> <span data-ttu-id="c20fe-111">Weitere Informationen zum Registrieren von Filtern finden [Sie unter Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="c20fe-111">For information on registering filters, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c20fe-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c20fe-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c20fe-113">DirectShow und com</span><span class="sxs-lookup"><span data-stu-id="c20fe-113">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



