---
description: Com+-Anwendungen bestehen aus einer oder mehreren COM-Komponenten.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Teile einer COM+-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483030"
---
# <a name="parts-of-a-com-application"></a><span data-ttu-id="68f32-103">Teile einer COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="68f32-103">Parts of a COM+ Application</span></span>

<span data-ttu-id="68f32-104">Com+-Anwendungen bestehen aus einer oder mehreren COM-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="68f32-104">COM+ applications consist of one or more COM components.</span></span>

<span data-ttu-id="68f32-105">Die folgenden Begriffe werden in der com+-Dokumentation verwendet:</span><span class="sxs-lookup"><span data-stu-id="68f32-105">The following terms are used throughout the COM+ documentation:</span></span>

<dl> <dt>

<span data-ttu-id="68f32-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM-Komponente*</span><span class="sxs-lookup"><span data-stu-id="68f32-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM component*</span></span>
</dt> <dd>

<span data-ttu-id="68f32-107">Eine binäre Einheit von Code, die COM-Objekte erstellt (einschließlich Paket Erstellung und Registrierungscode).</span><span class="sxs-lookup"><span data-stu-id="68f32-107">A binary unit of code that creates COM objects (includes packaging and registration code).</span></span>

</dd> <dt>

<span data-ttu-id="68f32-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM-Objekt*</span><span class="sxs-lookup"><span data-stu-id="68f32-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM object*</span></span>
</dt> <dd>

<span data-ttu-id="68f32-109">Eine Instanz einer com-Klasse.</span><span class="sxs-lookup"><span data-stu-id="68f32-109">An instance of a COM class.</span></span>

</dd> <dt>

<span data-ttu-id="68f32-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM-Klasse*</span><span class="sxs-lookup"><span data-stu-id="68f32-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM class*</span></span>
</dt> <dd>

<span data-ttu-id="68f32-111">Eine benannte, konkrete Implementierung von einer oder mehreren Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="68f32-111">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="68f32-112">Eine COM-Klasse wird durch eine CLSID identifiziert (manchmal auch durch eine ProgID).</span><span class="sxs-lookup"><span data-stu-id="68f32-112">A COM class is identified by a CLSID (sometimes by a ProgID also).</span></span>

</dd> <dt>

<span data-ttu-id="68f32-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM-Schnittstelle*</span><span class="sxs-lookup"><span data-stu-id="68f32-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM interface*</span></span>
</dt> <dd>

<span data-ttu-id="68f32-114">Eine Gruppe verwandter Methoden Funktionen, die von einer com-Klasse verfügbar gemacht werden, die einen Vertrag angibt.</span><span class="sxs-lookup"><span data-stu-id="68f32-114">A group of related method functions exposed by a COM class that specify a contract.</span></span> <span data-ttu-id="68f32-115">Dies schließt den Namen, die Schnittstellen Signatur, die Schnittstellen Semantik und das marshallingpufferformat ein.</span><span class="sxs-lookup"><span data-stu-id="68f32-115">This includes the name, interface signature, interface semantics, and marshaling buffer format.</span></span> <span data-ttu-id="68f32-116">Eine Schnittstelle wird durch eine IID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="68f32-116">An interface is identified by an IID.</span></span> <span data-ttu-id="68f32-117">Die Schnittstellen Syntax ist in IDL-und/oder Typbibliotheken definiert.</span><span class="sxs-lookup"><span data-stu-id="68f32-117">The interface syntax is defined in IDL and/or type libraries.</span></span> <span data-ttu-id="68f32-118">Die Schnittstellen einer com-Klasse sollten in verwaltbare, geschlossene Sätze von Methoden aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="68f32-118">The interfaces of a COM class should be divided into manageable, cohesive sets of methods.</span></span>

<span data-ttu-id="68f32-119">COM-Schnittstellen sind unveränderlich. der com-Vertrag besagt, dass Sie nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="68f32-119">COM interfaces are immutable; the COM contract states that they cannot be modified.</span></span> <span data-ttu-id="68f32-120">Jede Änderung (z. b. das Hinzufügen von Methoden) erfordert das Definieren einer neuen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="68f32-120">Any modification (such as adding methods) requires defining a new interface.</span></span>

</dd> <dt>

<span data-ttu-id="68f32-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM-Methode*</span><span class="sxs-lookup"><span data-stu-id="68f32-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM method*</span></span>
</dt> <dd>

<span data-ttu-id="68f32-122">Einer von einer Reihe verwandter Funktionen, die von einer COM-Schnittstelle bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="68f32-122">One of a set of related functions provided by a COM interface.</span></span>

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a><span data-ttu-id="68f32-123">Konfigurierte und nicht konfigurierte Komponenten</span><span class="sxs-lookup"><span data-stu-id="68f32-123">Configured and Unconfigured Components</span></span>

<span data-ttu-id="68f32-124">Um die von com+-Anwendungen unterstützten Dienste nutzen zu können, erzwingt die com+-Umgebung bestimmte Anforderungen an COM-Komponenten, die für COM+-Anwendungen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="68f32-124">To take advantage of the services that COM+ applications support, the COM+ environment imposes specific requirements on COM components built for COM+ applications.</span></span> <span data-ttu-id="68f32-125">Wenn eine COM-Komponente zu einer COM+-Anwendung hinzugefügt wird, wird Sie als *konfigurierte Komponente* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="68f32-125">When added to a COM+ application, a COM component is known as a *configured component*.</span></span>

<span data-ttu-id="68f32-126">COM-Komponenten, die für COM+-Anwendungen erstellt wurden, sind Prozess interne Serverkomponenten.</span><span class="sxs-lookup"><span data-stu-id="68f32-126">COM components built for COM+ applications are in-process server components.</span></span> <span data-ttu-id="68f32-127">Die Komponente muss eine Typbibliothek (TLB-Datei) enthalten, um alle Klassen zu beschreiben, die in der Komponente implementiert sind, und die Schnittstellen für alle Klassen in der Komponente zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="68f32-127">The component must contain a type library (.tlb file) to describe all classes implemented in the component and declare the interfaces on all classes in the component.</span></span> <span data-ttu-id="68f32-128">Sie können diese Komponenten mit Microsoft Visual Basic, Microsoft Visual C++ oder einem beliebigen COM-kompatiblen Entwicklungs Tool erstellen und implementieren.</span><span class="sxs-lookup"><span data-stu-id="68f32-128">You can create and implement these components with Microsoft Visual Basic, Microsoft Visual C++, or any COM-compatible development tool.</span></span>

<span data-ttu-id="68f32-129">Eine *nicht konfigurierte Komponente* ist eine Komponente, die nicht in einer COM+-Anwendung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="68f32-129">An *unconfigured component* is a component that isn't installed in a COM+ application.</span></span> <span data-ttu-id="68f32-130">Sie können die meisten nicht konfigurierten Komponenten in konfigurierte Komponenten transformieren, indem Sie Sie einfach in eine COM+-Anwendung integrieren.</span><span class="sxs-lookup"><span data-stu-id="68f32-130">You can transform most unconfigured components into configured components simply by integrating them into a COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="68f32-131">Verwenden Sie nicht die gleiche AppID für eine COM+-Anwendung und in der Registrierung für eine nicht konfigurierte Komponente.</span><span class="sxs-lookup"><span data-stu-id="68f32-131">Do not use the same AppID for both a COM+ application and in the registry for an unconfigured component.</span></span> <span data-ttu-id="68f32-132">Wenn die nicht konfigurierte Komponente aktiviert ist, ruft die Aktivierung möglicherweise die com+-Anwendungsinformationen aus der Registrierung ab, die die für die COM-Aktivierung erforderlichen Informationen nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="68f32-132">When the unconfigured component is activated , as activation may retrieve the COM+ application information from the registry that does not contain the information required for COM activation.</span></span> <span data-ttu-id="68f32-133">Ähnliche Probleme können auftreten, wenn ein " [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) " von dllhost aufgerufen wird, der die com+-Server Anwendung hostet.</span><span class="sxs-lookup"><span data-stu-id="68f32-133">Similar problems could arise if a call is made to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) from DllHost that hosts COM+ Server application.</span></span>

 

 

 
