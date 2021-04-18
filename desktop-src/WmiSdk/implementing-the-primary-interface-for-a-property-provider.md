---
description: Ein Eigenschaften Anbieter verwendet die IWbemPropertyProvider-Methoden als primäre Schnittstelle zu WMI. Mit IWbemPropertyProvider können Sie den Code implementieren, um Klassen-und Instanzeigenschaften abzurufen und zu ändern.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implementieren der primären Schnittstelle für einen Eigenschaften Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351807"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a><span data-ttu-id="ac066-104">Implementieren der primären Schnittstelle für einen Eigenschaften Anbieter</span><span class="sxs-lookup"><span data-stu-id="ac066-104">Implementing the Primary Interface for a Property Provider</span></span>

<span data-ttu-id="ac066-105">Ein Eigenschaften Anbieter verwendet die [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Methoden als primäre Schnittstelle zu WMI.</span><span class="sxs-lookup"><span data-stu-id="ac066-105">A property provider uses the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods as the primary interface to WMI.</span></span> <span data-ttu-id="ac066-106">Mit **IWbemPropertyProvider** können Sie den Code implementieren, um Klassen-und Instanzeigenschaften abzurufen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ac066-106">With **IWbemPropertyProvider**, you can implement the code to retrieve and modify class and instance properties.</span></span>

<span data-ttu-id="ac066-107">In der folgenden Tabelle sind die [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Methoden aufgelistet, die Sie für einen Eigenschaften Anbieter implementieren können.</span><span class="sxs-lookup"><span data-stu-id="ac066-107">The following table lists the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods that you can implement for a property provider.</span></span>



| <span data-ttu-id="ac066-108">Methode</span><span class="sxs-lookup"><span data-stu-id="ac066-108">Method</span></span>                                                   | <span data-ttu-id="ac066-109">Funktion</span><span class="sxs-lookup"><span data-stu-id="ac066-109">Feature</span></span>      |
|----------------------------------------------------------|--------------|
| [<span data-ttu-id="ac066-110">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="ac066-110">**GetProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | <span data-ttu-id="ac066-111">Auslagerung</span><span class="sxs-lookup"><span data-stu-id="ac066-111">Retrieval</span></span>    |
| [<span data-ttu-id="ac066-112">**PutProperty**</span><span class="sxs-lookup"><span data-stu-id="ac066-112">**PutProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | <span data-ttu-id="ac066-113">Modifikation (Modification)</span><span class="sxs-lookup"><span data-stu-id="ac066-113">Modification</span></span> |



 

> [!Note]  
> <span data-ttu-id="ac066-114">Sie müssen einen Eigenschaften Anbieter als in-Process-Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="ac066-114">You must implement a property provider as an in-process provider.</span></span> <span data-ttu-id="ac066-115">WMI initialisiert Eigenschaften Anbieter, die als Dienste oder ausführbare Dateien geschrieben werden, aber nie Ihre [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) -und [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) -Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ac066-115">WMI will initialize property providers written as services or executable files but will never call their [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) methods.</span></span>

 

<span data-ttu-id="ac066-116">Wenn Sie eine dieser Methoden nicht unterstützen, kann der Anbieter eine Stubimplementierung bereitstellen, die den **WBEM \_ E- \_ Anbieter \_ nicht \_** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac066-116">If you choose not to support one of these methods, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span>

<span data-ttu-id="ac066-117">Ein Eigenschaften Anbieter identifiziert eine verwaltete Klasse oder Instanz durch einen Satz von drei Qualifizierern: **propertycontext**, **InstanceContext** und **ClassContext**.</span><span class="sxs-lookup"><span data-stu-id="ac066-117">A property provider identifies a managed class or instance by a set of three qualifiers: **PropertyContext**, **InstanceContext**, and **ClassContext**.</span></span> <span data-ttu-id="ac066-118">WMI übergibt Zeichen folgen Konstanten, die diese drei Qualifizierer für ihren Eigenschaften Anbieter beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ac066-118">WMI will pass in string constants describing these three qualifiers to your property provider.</span></span>

<span data-ttu-id="ac066-119">Der Eigenschaften Anbieter muss darauf vorbereitet sein, die folgenden Typen von Kontext Qualifizierern zu verarbeiten:</span><span class="sxs-lookup"><span data-stu-id="ac066-119">Your property provider must be prepared to handle the following types of context qualifiers:</span></span>

-   <span data-ttu-id="ac066-120">Der **InstanceContext** -Qualifizierer ist an eine-Instanz angefügt und enthält Informationen, die für jede Eigenschaft in der Instanz gelten.</span><span class="sxs-lookup"><span data-stu-id="ac066-120">The **InstanceContext** qualifier is attached to an instance and contains information that applies to every property in the instance.</span></span>
-   <span data-ttu-id="ac066-121">Der **ClassContext** -Qualifizierer ist an eine Klasse angefügt und enthält Informationen, die für jede Instanz in der Klasse gelten.</span><span class="sxs-lookup"><span data-stu-id="ac066-121">The **ClassContext** qualifier is attached to a class and contains information that applies to every instance in the class.</span></span> <span data-ttu-id="ac066-122">In einer Klasse, die zum Speichern von Daten verwendet wird, die vom Registrierungs Anbieter bereitgestellt werden, kann **ClassContext** z. b. der Pfad zum Registrierungsschlüssel sein, der die zu gemeldeten Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="ac066-122">For example, in a class used to store data supplied by the Registry provider, **ClassContext** can be the path to the registry key that contains the properties to be reported.</span></span>
-   <span data-ttu-id="ac066-123">Der **propertycontext** -Qualifizierer gibt kontextspezifische Informationen an, die sich auf die-Eigenschaft beziehen.</span><span class="sxs-lookup"><span data-stu-id="ac066-123">The **PropertyContext** qualifier specifies context-specific information that pertains to the property.</span></span> <span data-ttu-id="ac066-124">In einer Klasse zum Speichern von Daten, die vom Registrierungs Anbieter bereitgestellt werden, gibt **propertycontext** z. b. den Namen des Registrierungs Werts an, der von der-Eigenschaft gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac066-124">For example, in a class used to store data supplied by the Registry provider, **PropertyContext** specifies the name of the registry value to be stored by the property.</span></span>

<span data-ttu-id="ac066-125">Diese Qualifizierer können zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ac066-125">These qualifiers can work together.</span></span> <span data-ttu-id="ac066-126">Sie können sowohl einen **InstanceContext** -als auch einen **propertycontext** -Wert festlegen, um dem Anbieter mitzuteilen, wie bestimmte Typen von Instanzen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ac066-126">You can designate both an **InstanceContext** and **PropertyContext** value to tell the provider how to treat particular types of instances.</span></span> <span data-ttu-id="ac066-127">Beispielsweise können Sie Instanzen markieren, die der Anbieter als lesbar erkennt, aber nur eine beschreibbare Eigenschaft besitzt.</span><span class="sxs-lookup"><span data-stu-id="ac066-127">For example, you might want to mark instances the provider will recognize as readable but having only one writeable property.</span></span>

<span data-ttu-id="ac066-128">Der am häufigsten verwendete Qualifizierer ist **propertycontext**.</span><span class="sxs-lookup"><span data-stu-id="ac066-128">The most common qualifier used is **PropertyContext**.</span></span> <span data-ttu-id="ac066-129">Daher stellt WMI den **dyn-** Eigenschaften Qualifizierer als Verknüpfung bereit.</span><span class="sxs-lookup"><span data-stu-id="ac066-129">Therefore, WMI provides the **DynProps** qualifier as a shortcut.</span></span> <span data-ttu-id="ac066-130">WMI betrachtet jede Eigenschaft in einer Instanz, die mit **dyn-** Eigenschaften gekennzeichnet ist, auch über die Qualifizierer " **Dynamic**", " [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)" und " **propertycontext**</span><span class="sxs-lookup"><span data-stu-id="ac066-130">WMI considers each property in an instance marked with **DynProps** to also have the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** qualifiers.</span></span>

 

 



