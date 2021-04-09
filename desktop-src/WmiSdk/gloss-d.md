---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042366"
---
# <a name="d-wmi"></a><span data-ttu-id="9d50a-103">D (WMI)</span><span class="sxs-lookup"><span data-stu-id="9d50a-103">D (WMI)</span></span>

<span data-ttu-id="9d50a-104">[a](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="9d50a-104">[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="9d50a-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**DateTime**</span><span class="sxs-lookup"><span data-stu-id="9d50a-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**datetime**</span></span>
</dt> <dd>

<span data-ttu-id="9d50a-106">Weitere Informationen finden Sie unter [*CIM DateTime*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="9d50a-106">See [*CIM datetime*](gloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d50a-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**entkoppelter Anbieter**</span><span class="sxs-lookup"><span data-stu-id="9d50a-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**decoupled provider**</span></span>
</dt> <dd>

<span data-ttu-id="9d50a-108">Ein Anbieter, der in einem anderen Prozess als WMI-Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d50a-108">A provider hosted in a separate process from WMI.</span></span> <span data-ttu-id="9d50a-109">Entkoppelte Anbieter sind die empfohlene Methode zum Instrumentieren einer Anwendung, da der Anbieter seine eigene Lebensdauer steuern kann, anstatt jedes Mal gestartet zu werden, wenn ein Benutzer über WMI auf den Anbieter zugreift.</span><span class="sxs-lookup"><span data-stu-id="9d50a-109">Decoupled providers are the recommended way to instrument an application, because the provider can control its own lifetime instead of being started each time a user accesses the provider through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="9d50a-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**direkter Zugriff**</span><span class="sxs-lookup"><span data-stu-id="9d50a-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**direct access**</span></span>
</dt> <dd>

<span data-ttu-id="9d50a-111">Eine Möglichkeit, auf Eigenschaften und Methoden zuzugreifen, die von WMI in einem Skript bereitgestellt werden, als ob es sich um Automatisierungs Eigenschaften und-Methoden von " [**errbemubject**](swbemobject.md)" handelt</span><span class="sxs-lookup"><span data-stu-id="9d50a-111">A way to access properties and methods supplied by WMI in a script as if they were automation properties and methods of [**SWbemObject**](swbemobject.md).</span></span>

<span data-ttu-id="9d50a-112">Nicht direkter Zugriff: `VolumeName = MyDisk.Properties_("VolumeName")`</span><span class="sxs-lookup"><span data-stu-id="9d50a-112">Nondirect access: `VolumeName = MyDisk.Properties_("VolumeName")`</span></span>

<span data-ttu-id="9d50a-113">Direkter Zugriff: `VolumeName = MyDisk.VolumeName`</span><span class="sxs-lookup"><span data-stu-id="9d50a-113">Direct access: `VolumeName = MyDisk.VolumeName`</span></span>

</dd> <dt>

<span data-ttu-id="9d50a-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Task Force für verteilte Verwaltung (DMTF)**</span><span class="sxs-lookup"><span data-stu-id="9d50a-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="9d50a-115">Eine internationale Standard Organisation, die mit wichtigen Technologieanbietern wie Microsoft zusammenarbeitet, um die Entwicklung, Übernahme und Vereinheitlichung von Verwaltungsstandards und-Initiativen für Desktop-, Unternehmens-und Internet Umgebungen zu unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9d50a-115">An international standards organization that works with key technology vendors, including Microsoft, to lead the development, adoption, and unification of management standards and initiatives for desktop, enterprise, and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="9d50a-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span><span class="sxs-lookup"><span data-stu-id="9d50a-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="9d50a-117">Siehe *verteilte Verwaltung Task Force (DMTF)*.</span><span class="sxs-lookup"><span data-stu-id="9d50a-117">See *Distributed Management Task Force (DMTF)*.</span></span>

</dd> <dt>

<span data-ttu-id="9d50a-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**dynamische Klasse**</span><span class="sxs-lookup"><span data-stu-id="9d50a-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**dynamic class**</span></span>
</dt> <dd>

<span data-ttu-id="9d50a-119">Eine CIM-Klasse, deren Definition bei Bedarf von einem [*Anbieter*](gloss-p.md) zur Laufzeit bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9d50a-119">A CIM class whose definition is supplied by a [*provider*](gloss-p.md) at run time, as required.</span></span> <span data-ttu-id="9d50a-120">Dynamische Klassen stellen anbieterspezifische [*verwaltete Objekte*](gloss-m.md) dar und werden nicht im CIM- [*Repository*](gloss-c.md)gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9d50a-120">Dynamic classes represent provider-specific [*managed objects*](gloss-m.md) and are not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="9d50a-121">Dynamische Klassen unterstützen nur *dynamische Instanzen*.</span><span class="sxs-lookup"><span data-stu-id="9d50a-121">Dynamic classes support only *dynamic instances*.</span></span>

</dd> <dt>

<span data-ttu-id="9d50a-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**dynamische Instanz**</span><span class="sxs-lookup"><span data-stu-id="9d50a-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**dynamic instance**</span></span>
</dt> <dd>

<span data-ttu-id="9d50a-123">Eine Instanz einer CIM-Klasse, die von einem [*Anbieter*](gloss-p.md) bei Bedarf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9d50a-123">An instance of a CIM class that is supplied by a [*provider*](gloss-p.md) when required.</span></span> <span data-ttu-id="9d50a-124">Sie wird nicht im CIM- [*Repository*](gloss-c.md)gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9d50a-124">It is not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="9d50a-125">Dynamische Instanzen können für statische oder dynamische Klassen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9d50a-125">Dynamic instances can be provided for either static or dynamic classes.</span></span> <span data-ttu-id="9d50a-126">Durch die dynamische Unterstützung von Instanzen einer Klasse kann ein Anbieter bis zu Minuten [*Eigenschafts*](gloss-p.md) Werte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9d50a-126">Dynamically supporting instances of a class enables a provider to supply up-to-the-minute [*property*](gloss-p.md) values.</span></span>

</dd> </dl>

 

 



