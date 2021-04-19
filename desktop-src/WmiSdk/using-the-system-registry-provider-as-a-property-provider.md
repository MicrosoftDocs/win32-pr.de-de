---
description: Sie können den System Registrierungs Anbieter entweder als Instanz oder als Eigenschaften Anbieter verwenden.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Verwenden des System Registrierungs Anbieters als Eigenschaften Anbieter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360693"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a><span data-ttu-id="e2d00-103">Verwenden des System Registrierungs Anbieters als Eigenschaften Anbieter</span><span class="sxs-lookup"><span data-stu-id="e2d00-103">Use the System Registry Provider as a Property Provider</span></span>

<span data-ttu-id="e2d00-104">Sie können den [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) entweder als Instanz oder als Eigenschaften Anbieter verwenden.</span><span class="sxs-lookup"><span data-stu-id="e2d00-104">You can use the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) as either an instance or a property provider.</span></span>

<span data-ttu-id="e2d00-105">Wenn Sie sich für den Zugriff auf die Eigenschaften Anbieter Schnittstellen entscheiden, müssen Sie die WMI-Klassen markieren, um ihre Absicht anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e2d00-105">If you choose to access the property provider interfaces, you must mark your WMI classes to indicate your intention.</span></span>

<span data-ttu-id="e2d00-106">**So verwenden Sie den System Registrierungs Anbieter als Eigenschaften Anbieter**</span><span class="sxs-lookup"><span data-stu-id="e2d00-106">**To use the system registry provider as a property provider**</span></span>

-   <span data-ttu-id="e2d00-107">Definieren Sie die WMI-Klasse mit den Standard Qualifizierern **dynproper,** [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)und **propertycontext** .</span><span class="sxs-lookup"><span data-stu-id="e2d00-107">Define your WMI class with the **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** standard qualifiers.</span></span>

    <span data-ttu-id="e2d00-108">Der **dynproperties** -Qualifizierer identifiziert eine Klasse als Eigenschaften, die von dem vom [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider) Qualifizierer identifizierten Eigenschaften Anbieter verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e2d00-108">The **DynProps** qualifier identifies a class as having properties that are maintained by the property provider identified by the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span> <span data-ttu-id="e2d00-109">Der **propertycontext** -Qualifizierer gibt den Namen des Registrierungs Werts an, der von der-Eigenschaft gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2d00-109">The **PropertyContext** qualifier specifies the name of the registry value to be stored by the property.</span></span> <span data-ttu-id="e2d00-110">Das Format des **propertycontext** -Qualifizierers ist mit dem Format des **ClassContext** -Qualifizierers mit zusätzlichen *valueName* -und *Expression* -Werten identisch.</span><span class="sxs-lookup"><span data-stu-id="e2d00-110">The format of the **PropertyContext** qualifier is the same as the format of the **ClassContext** qualifier with additional *valuename* and *expression* values.</span></span>

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    <span data-ttu-id="e2d00-111">" *ValueName* " und " *Expression* " sind optional.</span><span class="sxs-lookup"><span data-stu-id="e2d00-111">Both *valuename* and *expression* are optional.</span></span> <span data-ttu-id="e2d00-112">Die *valueName* -Einstellung wird nur verwendet, wenn der Registrierungs Wert einen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="e2d00-112">The *valuename* setting is only used if the registry value has a name.</span></span> <span data-ttu-id="e2d00-113">Der *Ausdruck* ist auch optional und wird für Ressourcen deskriptordaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2d00-113">The *expression* is also optional and is used for resource descriptor data.</span></span> <span data-ttu-id="e2d00-114">Weitere Informationen finden Sie unter [beschreiben einer Ressource für die Registrierung](describing-a-resource-for-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="e2d00-114">For more information, see [Describing a Resource for the Registry](describing-a-resource-for-the-registry.md).</span></span>

    <span data-ttu-id="e2d00-115">Im folgenden Codebeispiel wird veranschaulicht, wie die-Klasse den System Registrierungs Anbieter als Eigenschaften Anbieter verwendet, um seine nicht Schlüsseleigenschaften beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="e2d00-115">The following code example shows how the class uses the System Registry provider as a property provider to maintain its nonkey properties.</span></span>

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 
