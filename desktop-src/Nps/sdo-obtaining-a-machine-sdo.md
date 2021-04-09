---
title: Abrufen eines Computers SDO
description: Der erste Schritt bei der Verwendung der SDO-API ist das Erstellen eines SDO-Computer Objekts.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039241"
---
# <a name="obtaining-a-machine-sdo"></a><span data-ttu-id="69b4d-103">Abrufen eines Computers SDO</span><span class="sxs-lookup"><span data-stu-id="69b4d-103">Obtaining a Machine SDO</span></span>

<span data-ttu-id="69b4d-104">Der erste Schritt bei der Verwendung der SDO-API ist das Erstellen eines SDO-Computer Objekts.</span><span class="sxs-lookup"><span data-stu-id="69b4d-104">The first step in using the SDO API is to create an SDO machine object.</span></span>

<span data-ttu-id="69b4d-105">Verwenden Sie die [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) -Funktion, um den Klassen Bezeichner (CLSID) für das Objekt "SDO Machine" abzurufen.</span><span class="sxs-lookup"><span data-stu-id="69b4d-105">Use the [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) function to obtain the class identifier (CLSID) for the SDO machine object.</span></span> <span data-ttu-id="69b4d-106">Der programmatische Bezeichner (ProgID), der für das-Objekt verwendet werden soll, ist "IAS. Sdomachine ".</span><span class="sxs-lookup"><span data-stu-id="69b4d-106">The programmatic identifier (ProgID) to use for the object is "IAS.SdoMachine".</span></span>

<span data-ttu-id="69b4d-107">Wenn Sie die CLSID haben, müssen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dieser CLSID aufrufen.</span><span class="sxs-lookup"><span data-stu-id="69b4d-107">Once you have the CLSID, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with this CLSID.</span></span> <span data-ttu-id="69b4d-108">Geben Sie [**isdomachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) als Schnittstelle an, für die ein Zeiger zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="69b4d-108">Specify [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) as the interface for which to return a pointer.</span></span>

<span data-ttu-id="69b4d-109">Beispielcode zum Abrufen eines Computers SDO finden [Sie unter Anfügen an einen SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) .</span><span class="sxs-lookup"><span data-stu-id="69b4d-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to obtain a machine SDO.</span></span>

 

 