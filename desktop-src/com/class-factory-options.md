---
title: Class Factory-Optionen
description: Class Factory-Optionen
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730432"
---
# <a name="class-factory-options"></a><span data-ttu-id="70bc4-103">Class Factory-Optionen</span><span class="sxs-lookup"><span data-stu-id="70bc4-103">Class Factory Options</span></span>

<span data-ttu-id="70bc4-104">Ein ActiveX-Steuerelement muss aufgrund eines COM-Objekts über zugeordneten Servercode verfügen, der das Erstellen von Steuerelementen über [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="70bc4-104">An ActiveX Control, by virtue of being a COM object, must have associated server code that supports control creation through [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) as a minimum.</span></span>

<span data-ttu-id="70bc4-105">Es ist optional, nicht erforderlich, dass dieses Klassenobjekt auch [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) für die Lizenzierungs Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="70bc4-105">It is optional, not required, that this class object also support [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) for licensing management.</span></span> <span data-ttu-id="70bc4-106">Nur die Hersteller, die sich mit der Lizenzierung beschäftigen, müssen den Lizenzierungs Mechanismus von com unterstützen.</span><span class="sxs-lookup"><span data-stu-id="70bc4-106">Only those vendors that are concerned about licensing need to support COM's licensing mechanism.</span></span> <span data-ttu-id="70bc4-107">Anders ausgedrückt: da **IClassFactory2** die einzige Möglichkeit ist, eine Lizenzierung auf com-Ebene zu erreichen, ist diese Schnittstelle für das Klassenobjekt für die Steuerelemente, die lizenziert werden sollen, erforderlich.</span><span class="sxs-lookup"><span data-stu-id="70bc4-107">In other words, because **IClassFactory2** is the only way to achieve COM-level licensing, this interface is required on the class object for those controls that want to be licensed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70bc4-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70bc4-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70bc4-109">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="70bc4-109">Controls</span></span>](controls.md)
</dt> </dl>

 

 