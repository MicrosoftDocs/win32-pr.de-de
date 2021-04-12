---
title: Die IOleContainer-Methode
description: Die IOleContainer-Methode
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206345"
---
# <a name="the-iolecontainerenumobjects-method"></a><span data-ttu-id="d1d87-103">IOleContainer:: erumubjects-Methode</span><span class="sxs-lookup"><span data-stu-id="d1d87-103">The IOleContainer::EnumObjects Method</span></span>

<span data-ttu-id="d1d87-104">Diese Methode wird verwendet, um alle OLE-Objekte aufzuzählen, die in einem Dokument oder Formular enthalten sind, und gibt einen Schnittstellen Zeiger für jedes OLE-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d1d87-104">This method is used to enumerate over all the OLE objects contained in a document or form, returning an interface pointer for each OLE object.</span></span> <span data-ttu-id="d1d87-105">Der Container muss Zeiger auf jedes OLE-Objekt zurückgeben, das denselben Container gemeinsam nutzt.</span><span class="sxs-lookup"><span data-stu-id="d1d87-105">The container must return pointers to each OLE object that shares the same container.</span></span> <span data-ttu-id="d1d87-106">Es müssen auch in Form von Form-oder-Steuerelementen aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="d1d87-106">Nested forms or nested controls must also be enumerated.</span></span>

<span data-ttu-id="d1d87-107">Einige Container implementieren Extender-Steuerelemente, die nicht-ActiveX-Steuerelemente umschließen und dann Zeiger auf diese Extendersteuerelemente zurückgeben, wenn ein Formular aufgelistet ist.</span><span class="sxs-lookup"><span data-stu-id="d1d87-107">Some containers implement extender controls, which wrap non-ActiveX controls, and then return pointers to these extender controls as a form is enumerated.</span></span> <span data-ttu-id="d1d87-108">Durch dieses Verhalten können ActiveX-Steuerelemente und ActiveX-Steuerelement Container gut in nicht-ActiveX-Steuerelemente integriert werden. Daher wird empfohlen, ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1d87-108">This behavior enables ActiveX controls and ActiveX control containers to integrate well with non-ActiveX controls, and is thus recommended, but not required.</span></span>

 

 




