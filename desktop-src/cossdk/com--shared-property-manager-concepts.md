---
description: In com+ wird der freigegebene vorübergehende Zustand für-Objekte mithilfe des freigegebenen Eigenschaften-Managers (SPM) verwaltet. Der SPM ist ein Ressourcen Verteiler, den Sie verwenden können, um den Status von mehreren Objekten innerhalb eines Server Prozesses gemeinsam zu nutzen.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Gemeinsam genutzte com+-Eigenschaften-Manager Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343189"
---
# <a name="com-shared-property-manager-concepts"></a><span data-ttu-id="79eeb-104">Gemeinsam genutzte com+-Eigenschaften-Manager Konzepte</span><span class="sxs-lookup"><span data-stu-id="79eeb-104">COM+ Shared Property Manager Concepts</span></span>

<span data-ttu-id="79eeb-105">In com+ wird der freigegebene vorübergehende Zustand für-Objekte mithilfe des freigegebenen Eigenschaften-Managers (SPM) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="79eeb-105">In COM+, shared transient state for objects is managed by using the shared property manager (SPM).</span></span> <span data-ttu-id="79eeb-106">Der SPM ist ein Ressourcen Verteiler, den Sie verwenden können, um den Status von mehreren Objekten innerhalb eines Server Prozesses gemeinsam zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="79eeb-106">The SPM is a resource dispenser that you can use to share state among multiple objects within a server process.</span></span>

<span data-ttu-id="79eeb-107">Globale Variablen können nicht in einer verteilten Umgebung verwendet werden, da Probleme mit Parallelität und Namenskollisionen auftreten.</span><span class="sxs-lookup"><span data-stu-id="79eeb-107">You cannot use global variables in a distributed environment because of concurrency and name collision issues.</span></span> <span data-ttu-id="79eeb-108">Der freigegebene Eigenschaften-Manager entfernt Namenskonflikte durch Bereitstellen von freigegebenen Eigenschaften Gruppen, die eindeutige Namespaces für die freigegebenen Eigenschaften einrichten, die Sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="79eeb-108">The shared property manager eliminates name collisions by providing shared property groups, which establish unique namespaces for the shared properties they contain.</span></span> <span data-ttu-id="79eeb-109">Der SPM implementiert auch sperren und Semaphoren, um freigegebene Eigenschaften vor gleichzeitigem Zugriff zu schützen. Dies kann zu einem Verlust von Updates führen und die Eigenschaften in einem unvorhersehbaren Zustand hinterlassen.</span><span class="sxs-lookup"><span data-stu-id="79eeb-109">The SPM also implements locks and semaphores to help protect shared properties from simultaneous access, which could result in lost updates and leave properties in an unpredictable state.</span></span>

> [!Note]  
> <span data-ttu-id="79eeb-110">Ein frei gegebener vorübergehender Zustand ist Zustandsinformationen, die im Arbeitsspeicher beibehalten werden und Systemfehler nicht überstehen.</span><span class="sxs-lookup"><span data-stu-id="79eeb-110">Shared transient state is state information kept in memory that does not survive system failures.</span></span> <span data-ttu-id="79eeb-111">Die Informationen sind so konzipiert, dass Sie von mehreren-Objekten über transaktionsübergreifende (aber nicht prozessübergreifende) Grenzen hinweg verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79eeb-111">The information is designed to be shared by multiple objects across transaction (but not across process) boundaries.</span></span>

 

<span data-ttu-id="79eeb-112">Freigegebene Eigenschaften, die im SPM gespeichert sind, sind nur für Objekte verfügbar, die im selben Prozess ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="79eeb-112">Shared properties stored in the SPM are available only to objects running in the same process.</span></span> <span data-ttu-id="79eeb-113">Dies bedeutet, dass die Objekte, die den SPM zum Speichern von Werten verwenden und auf diese Werte zugreifen müssen, als Teil der gleichen com+-Anwendung installiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="79eeb-113">This means that the objects that will use the SPM for storing values and that will need to have access to these values must be installed as part of the same COM+ application.</span></span> <span data-ttu-id="79eeb-114">Es ist möglich, dass Systemadministratoren com+-Klassen nach der Bereitstellung der com+-Anwendung von einem Paket in ein anderes verschieben.</span><span class="sxs-lookup"><span data-stu-id="79eeb-114">It is possible for system administrators to move COM+ classes from one package to another after your COM+ application has been deployed.</span></span> <span data-ttu-id="79eeb-115">Wenn Sie von mehreren Objekten abhängen, die Eigenschaften über das SPM freigeben, sollten Sie klar dokumentieren, dass Sie in der gleichen com+-Anwendung installiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="79eeb-115">If you rely on several objects sharing properties through the SPM, you should clearly document that they must be installed in the same COM+ application.</span></span>

<span data-ttu-id="79eeb-116">Es ist auch wichtig, dass Komponenten, die Eigenschaften gemeinsam nutzen, über das gleiche Aktivierungs Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="79eeb-116">It's also important for components sharing properties to have the same activation attribute.</span></span> <span data-ttu-id="79eeb-117">Wenn zwei Komponenten im gleichen Paket über unterschiedliche Aktivierungs Attribute verfügen, können diese Eigenschaften in der Regel nicht gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="79eeb-117">If two components in the same package have different activation attributes, they generally won't be able to share properties.</span></span> <span data-ttu-id="79eeb-118">Wenn z. b. eine Komponente so konfiguriert ist, dass Sie in einem Client Prozess ausgeführt wird und die andere für die Durchführung in einem Server Prozess konfiguriert ist, werden die Objekte in der Regel in unterschiedlichen Prozessen ausgeführt, auch wenn Sie sich im gleichen Paket befinden.</span><span class="sxs-lookup"><span data-stu-id="79eeb-118">For example, if one component is configured to run in a client process and the other is configured to run in a server process, their objects will usually run in different processes even though they're in the same package.</span></span>

<span data-ttu-id="79eeb-119">Sie sollten immer die Objekte [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)und [**SharedProperty**](sharedproperty.md) von COM+-Komponenten anstelle eines Basis Clients instanziieren.</span><span class="sxs-lookup"><span data-stu-id="79eeb-119">You should always instantiate the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md), and [**SharedProperty**](sharedproperty.md) objects from COM+ components rather than from a base client.</span></span> <span data-ttu-id="79eeb-120">Wenn ein Basis Client freigegebene Eigenschaften Gruppen und Eigenschaften erstellt, befinden sich die freigegebenen Eigenschaften innerhalb des Basis Client Prozesses und nicht in einem Server Prozess.</span><span class="sxs-lookup"><span data-stu-id="79eeb-120">If a base client creates shared property groups and properties, the shared properties are inside the base-client process, not in a server process.</span></span> <span data-ttu-id="79eeb-121">Dies bedeutet, dass die COM+-Objekte die Eigenschaften nicht gemeinsam nutzen können, es sei denn, die Objekte werden ebenfalls im Client Prozess ausgeführt (was in der Regel keine gute Idee ist).</span><span class="sxs-lookup"><span data-stu-id="79eeb-121">This means the COM+ objects cannot share the properties unless the objects are also running in the client process (which is generally not a good idea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79eeb-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79eeb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79eeb-123">Gemeinsam genutztes com+-Eigenschaften-Manager</span><span class="sxs-lookup"><span data-stu-id="79eeb-123">COM+ Shared Property Manager</span></span>](com--shared-property-manager.md)
</dt> <dt>

[<span data-ttu-id="79eeb-124">Freigegebene Eigenschaften Gruppen</span><span class="sxs-lookup"><span data-stu-id="79eeb-124">Shared Property Groups</span></span>](shared-property-groups.md)
</dt> </dl>

 

 



