---
title: ActiveX-Steuerelemente
description: ActiveX-Steuerelemente
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391040"
---
# <a name="activex-controls"></a><span data-ttu-id="7a4ad-103">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7a4ad-103">ActiveX Controls</span></span>

<span data-ttu-id="7a4ad-104">ActiveX-Steuerungstechnologien sind auf einer Grundlage von com, Verbindungs fähigen Objekten, Verbund Dokumenten, Eigenschaften Seiten, OLE-Automatisierung, Objekt Persistenz und vom System bereitgestellten Schriftart-und Bild Objekten enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-104">ActiveX controls technology rests on a foundation consisting of COM, connectable objects, compound documents, property pages, OLE automation, object persistence, and system-provided font and picture objects.</span></span> <span data-ttu-id="7a4ad-105">Wie unten zusammengefasst, spielt jede dieser Kerntechnologien eine Rolle in den Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-105">As summarized below, each of these core technologies plays a role in controls.</span></span>

<dl> <dt>

<span data-ttu-id="7a4ad-106"><span id="COM"></span><span id="com"></span>KOM</span><span class="sxs-lookup"><span data-stu-id="7a4ad-106"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="7a4ad-107">Ein Steuerelement ist im Grunde ein COM-Objekt, das die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle verfügbar macht, über die Clients Zeiger auf Ihre anderen Schnittstellen abrufen können.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-107">A control is essentially a COM object that exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces.</span></span> <span data-ttu-id="7a4ad-108">Steuerelemente können die Lizenzierung über [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) und Selbstregistrierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-108">Controls can support licensing through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) and self-registration.</span></span> <span data-ttu-id="7a4ad-109">Weitere Informationen zu com, Lizenzierung und Selbstregistrierung finden Sie in [der Component Object Model](the-component-object-model.md) .</span><span class="sxs-lookup"><span data-stu-id="7a4ad-109">See [The Component Object Model](the-component-object-model.md) for more information on COM, licensing, and self-registration.</span></span>

</dd> <dt>

<span data-ttu-id="7a4ad-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Verbindungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="7a4ad-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Connectable objects</span></span>
</dt> <dd>

<span data-ttu-id="7a4ad-111">Steuerelemente können ausgehende Schnittstellen durch Verbindungs fähige Objekte unterstützen, sodass das Steuerelement mit dem Client kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-111">Controls can support outgoing interfaces through connectable objects so that the control can communicate with its client.</span></span> <span data-ttu-id="7a4ad-112">Beispielsweise kann eine ausgehende Schnittstelle eine Aktion im Client auslöst, den Client über Änderungen im Steuerelement benachrichtigen oder eine Berechtigung vom Client anfordern, bevor das Steuerelement Aktionen annimmt.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-112">For example, an outgoing interface can trigger an action in the client, can notify the client of some change in the control, or can request permission from the client before the control takes some action.</span></span> <span data-ttu-id="7a4ad-113">Weitere Informationen zur Funktionsweise von Verbindungs fähigen Objekten finden Sie unter [Ereignisse in com und Verbindungs fähigen Objekten](events-in-com-and-connectable-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="7a4ad-113">See [Events in COM and Connectable Objects](events-in-com-and-connectable-objects.md) for more information on how connectable objects work.</span></span>

</dd> <dt>

<span data-ttu-id="7a4ad-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Einheitliche Datenübertragung</span><span class="sxs-lookup"><span data-stu-id="7a4ad-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform data transfer</span></span>
</dt> <dd>

<span data-ttu-id="7a4ad-115">Steuerelemente können das ziehen und Ablegen in einem Container mithilfe von Hilfe aus dem Container unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-115">Controls can support being dragged and dropped within a container with help from their container.</span></span> <span data-ttu-id="7a4ad-116">Weitere Informationen zum Ziehen und ablegen finden Sie unter [**IOleInPlaceObjectWindowless:: getdroptarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="7a4ad-116">See [**IOleInPlaceObjectWindowless::GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) for more information on drag and drop.</span></span>

</dd> <dt>

<span data-ttu-id="7a4ad-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Verbund Dokumente</span><span class="sxs-lookup"><span data-stu-id="7a4ad-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Compound documents</span></span>
</dt> <dd>

<span data-ttu-id="7a4ad-118">Bei einem Steuerelement kann es sich um ein direktes aktives Objekt handeln, das in einen enthaltenden Client eingebettet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-118">A control can be an in-place active object that can be embedded in a containing client.</span></span> <span data-ttu-id="7a4ad-119">Ein Endbenutzer aktiviert das-Steuerelement, um eine Aktion in der Containeranwendung zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-119">An end-user activates the control to initiate an action in the container application.</span></span> <span data-ttu-id="7a4ad-120">Weitere Informationen zur direkten Aktivierung und zu anderen Verbund Dokument Schnittstellen finden Sie unter zusammen [gesetzte Dokumente](compound-documents.md) .</span><span class="sxs-lookup"><span data-stu-id="7a4ad-120">See [Compound Documents](compound-documents.md) for more information on in-place activation and other compound document interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="7a4ad-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="7a4ad-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Property pages</span></span>
</dt> <dd>

<span data-ttu-id="7a4ad-122">Steuerelemente können Eigenschaften Seiten bereitstellen, damit Endbenutzer die Eigenschaften des Steuer Elements anzeigen und ändern können.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-122">Controls can provide property pages so end users can view and change the control's properties.</span></span> <span data-ttu-id="7a4ad-123">Weitere Informationen zur Funktionsweise von Eigenschaften Seiten finden Sie unter [Eigenschaften Seiten und Eigenschaften Blätter](property-pages-and-property-sheets.md) .</span><span class="sxs-lookup"><span data-stu-id="7a4ad-123">See [Property Pages and Property Sheets](property-pages-and-property-sheets.md) for more information on how property pages work.</span></span>

</dd> <dt>

<span data-ttu-id="7a4ad-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE-Automatisierung</span><span class="sxs-lookup"><span data-stu-id="7a4ad-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE automation</span></span>
</dt> <dd>

<span data-ttu-id="7a4ad-125">Steuerelemente können mithilfe der OLE-Automatisierung Programmierbarkeit bereitstellen, sodass Clients die Funktionen des Steuer Elements über eine vom Client bereitgestellte Programmiersprache nutzen können.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-125">Controls can provide programmability through OLE automation so clients can take advantage of the control's features through a programming language supplied by the client.</span></span> <span data-ttu-id="7a4ad-126">Weitere Informationen zur OLE-Automatisierung finden Sie im Abschnitt OLE-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-126">See the OLE Automation section for more information on OLE automation.</span></span>

</dd> <dt>

<span data-ttu-id="7a4ad-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Persistenter Speicher</span><span class="sxs-lookup"><span data-stu-id="7a4ad-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Persistent storage</span></span>
</dt> <dd>

<span data-ttu-id="7a4ad-128">Ein Steuerelement kann eine oder mehrere der persistenzschnittstellen implementieren, um die Persistenz seines Zustands zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-128">A control can implement one or more of several persistence interfaces to support persistence of its state.</span></span> <span data-ttu-id="7a4ad-129">Die Implementierung des Steuer Elements muss entscheiden, welche Arten von Persistenz am wichtigsten sind, und die entsprechenden persistenzschnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-129">The control implementer must decide what kinds of persistence are most important and implement the appropriate persistence interfaces.</span></span> <span data-ttu-id="7a4ad-130">Der Client entscheidet, welche Schnittstelle er bevorzugt verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-130">The client decides which interface it prefers to use.</span></span> <span data-ttu-id="7a4ad-131">Weitere Informationen zu allen persistenzschnittstellen finden Sie in [der Component Object Model](the-component-object-model.md) .</span><span class="sxs-lookup"><span data-stu-id="7a4ad-131">See [The Component Object Model](the-component-object-model.md) for more information on all the persistence interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="7a4ad-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Schriftart-und Bildobjekte</span><span class="sxs-lookup"><span data-stu-id="7a4ad-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Font and picture objects</span></span>
</dt> <dd>

<span data-ttu-id="7a4ad-133">Steuerelemente können diese vom System bereitgestellten Objekte verwenden, um eine visuelle Darstellung von sich selbst innerhalb des Clients bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-133">Controls can use these system provided objects to provide a visual representation of themselves within the client.</span></span> <span data-ttu-id="7a4ad-134">Das Schriftart Objekt implementiert mehrere Schnittstellen, einschließlich [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) und [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span><span class="sxs-lookup"><span data-stu-id="7a4ad-134">The font object implements several interfaces, including [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) and [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span></span> <span data-ttu-id="7a4ad-135">Ein Schriftart Objekt kann mit [**olecreatefontindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-135">A font object can be created with [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span></span> <span data-ttu-id="7a4ad-136">Das Bild Objekt implementiert auch mehrere Schnittstellen, einschließlich [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) und [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span><span class="sxs-lookup"><span data-stu-id="7a4ad-136">The picture object also implements several interfaces, including [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span></span> <span data-ttu-id="7a4ad-137">Ein Bild Objekt kann mithilfe von [**olecreatepictureindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) erstellt werden und kann aus einem Stream mit [**oleloadpicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)geladen werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-137">A picture object can be created using [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) and can loaded from a stream with [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span></span>

</dd> </dl>

<span data-ttu-id="7a4ad-138">Es ist wichtig zu verstehen, dass diese Features in beliebigen OLE-Objekten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-138">It is important to understand that these features can be used in any OLE object.</span></span> <span data-ttu-id="7a4ad-139">Ein Steuerelement muss nicht implementiert werden, damit diese Features verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-139">One does not need to implement a control in order to use these features.</span></span> <span data-ttu-id="7a4ad-140">Außerdem ist die einzige erforderliche Schnittstelle für ein Steuerelement IUnknown.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-140">Also, the only required interface on a control is IUnknown.</span></span> <span data-ttu-id="7a4ad-141">Das-Steuerelement unterstützt optional andere Schnittstellen, je nachdem, dass die zugehörigen Funktionen unterstützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-141">The control optionally supports other interfaces based on the need to support the related features.</span></span>

<span data-ttu-id="7a4ad-142">Zusätzlich zu diesen Features sind die folgenden Schnittstellen und Funktionen spezifisch für die Steuerelemente Technologie: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)und [**oletranslatecolor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span><span class="sxs-lookup"><span data-stu-id="7a4ad-142">In addition to these features, the following interfaces and functions are specific to controls technology: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span></span> <span data-ttu-id="7a4ad-143">Auch Steuerelemente sind ein Satz von Standards für Eigenschaften und Methoden, die ein Steuerelement oder ein Steuerelement Container unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-143">Also specific to controls are a set of standards for properties and methods that a control or a control container can support.</span></span>

> [!Note]  
> <span data-ttu-id="7a4ad-144">Die Systembibliothek OleAut32.dll enthält Implementierungen der Funktionen ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**olecreatepropertyframeindirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**olecreatefontindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**olecreatepictureindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**oleloadpicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)und [**oletranslatecolor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span><span class="sxs-lookup"><span data-stu-id="7a4ad-144">The system library OleAut32.dll contains implementations of the functions ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span></span> <span data-ttu-id="7a4ad-145">Darüber hinaus enthält OleAut32.dll die Implementierungen der standardmäßigen Schriftart-und Bildobjekte sowie eine Typbibliothek für alle Schnittstellen, die mit Steuerelementen verwendet werden, sowie die zusätzlichen Datenstrukturen und Datentypen.</span><span class="sxs-lookup"><span data-stu-id="7a4ad-145">In addition, OleAut32.dll contains the implementations of the standard font and picture objects, as well as a type library for all the interfaces used with controls as well as the additional data structures and data types.</span></span>

 

<span data-ttu-id="7a4ad-146">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="7a4ad-146">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="7a4ad-147">ActiveX-Steuerelement Architektur</span><span class="sxs-lookup"><span data-stu-id="7a4ad-147">ActiveX Controls Architecture</span></span>](activex-controls-architecture.md)
-   [<span data-ttu-id="7a4ad-148">ActiveX-Steuerelement Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7a4ad-148">ActiveX Controls Interfaces</span></span>](activex-controls-interfaces.md)
-   [<span data-ttu-id="7a4ad-149">Eigenschaften und Methoden</span><span class="sxs-lookup"><span data-stu-id="7a4ad-149">Properties and Methods</span></span>](properties-and-methods.md)
-   [<span data-ttu-id="7a4ad-150">Steuerelementereignisse</span><span class="sxs-lookup"><span data-stu-id="7a4ad-150">Control Events</span></span>](control-events.md)
-   [<span data-ttu-id="7a4ad-151">Visuelle Darstellung</span><span class="sxs-lookup"><span data-stu-id="7a4ad-151">Visual Representation</span></span>](visual-representation.md)
-   [<span data-ttu-id="7a4ad-152">Tastatur Behandlung für Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7a4ad-152">Keyboard Handling for Controls</span></span>](keyboard-handling-for-controls.md)
-   [<span data-ttu-id="7a4ad-153">Persistenz</span><span class="sxs-lookup"><span data-stu-id="7a4ad-153">Persistence</span></span>](persistence.md)
-   [<span data-ttu-id="7a4ad-154">Registrierung und Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="7a4ad-154">Registration and Licensing</span></span>](registration-and-licensing.md)

## <a name="related-topics"></a><span data-ttu-id="7a4ad-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a4ad-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a4ad-156">ActiveX-Steuerelement-und Steuerelement Container</span><span class="sxs-lookup"><span data-stu-id="7a4ad-156">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 