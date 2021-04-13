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
# <a name="activex-controls"></a>ActiveX-Steuerelemente

ActiveX-Steuerungstechnologien sind auf einer Grundlage von com, Verbindungs fähigen Objekten, Verbund Dokumenten, Eigenschaften Seiten, OLE-Automatisierung, Objekt Persistenz und vom System bereitgestellten Schriftart-und Bild Objekten enthalten. Wie unten zusammengefasst, spielt jede dieser Kerntechnologien eine Rolle in den Steuerelementen.

<dl> <dt>

<span id="COM"></span><span id="com"></span>KOM
</dt> <dd>

Ein Steuerelement ist im Grunde ein COM-Objekt, das die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle verfügbar macht, über die Clients Zeiger auf Ihre anderen Schnittstellen abrufen können. Steuerelemente können die Lizenzierung über [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) und Selbstregistrierung unterstützen. Weitere Informationen zu com, Lizenzierung und Selbstregistrierung finden Sie in [der Component Object Model](the-component-object-model.md) .

</dd> <dt>

<span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Verbindungs fähige Objekte
</dt> <dd>

Steuerelemente können ausgehende Schnittstellen durch Verbindungs fähige Objekte unterstützen, sodass das Steuerelement mit dem Client kommunizieren kann. Beispielsweise kann eine ausgehende Schnittstelle eine Aktion im Client auslöst, den Client über Änderungen im Steuerelement benachrichtigen oder eine Berechtigung vom Client anfordern, bevor das Steuerelement Aktionen annimmt. Weitere Informationen zur Funktionsweise von Verbindungs fähigen Objekten finden Sie unter [Ereignisse in com und Verbindungs fähigen Objekten](events-in-com-and-connectable-objects.md) .

</dd> <dt>

<span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Einheitliche Datenübertragung
</dt> <dd>

Steuerelemente können das ziehen und Ablegen in einem Container mithilfe von Hilfe aus dem Container unterstützen. Weitere Informationen zum Ziehen und ablegen finden Sie unter [**IOleInPlaceObjectWindowless:: getdroptarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) .

</dd> <dt>

<span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Verbund Dokumente
</dt> <dd>

Bei einem Steuerelement kann es sich um ein direktes aktives Objekt handeln, das in einen enthaltenden Client eingebettet werden kann. Ein Endbenutzer aktiviert das-Steuerelement, um eine Aktion in der Containeranwendung zu initiieren. Weitere Informationen zur direkten Aktivierung und zu anderen Verbund Dokument Schnittstellen finden Sie unter zusammen [gesetzte Dokumente](compound-documents.md) .

</dd> <dt>

<span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Eigenschaften Seiten
</dt> <dd>

Steuerelemente können Eigenschaften Seiten bereitstellen, damit Endbenutzer die Eigenschaften des Steuer Elements anzeigen und ändern können. Weitere Informationen zur Funktionsweise von Eigenschaften Seiten finden Sie unter [Eigenschaften Seiten und Eigenschaften Blätter](property-pages-and-property-sheets.md) .

</dd> <dt>

<span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE-Automatisierung
</dt> <dd>

Steuerelemente können mithilfe der OLE-Automatisierung Programmierbarkeit bereitstellen, sodass Clients die Funktionen des Steuer Elements über eine vom Client bereitgestellte Programmiersprache nutzen können. Weitere Informationen zur OLE-Automatisierung finden Sie im Abschnitt OLE-Automatisierung.

</dd> <dt>

<span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Persistenter Speicher
</dt> <dd>

Ein Steuerelement kann eine oder mehrere der persistenzschnittstellen implementieren, um die Persistenz seines Zustands zu unterstützen. Die Implementierung des Steuer Elements muss entscheiden, welche Arten von Persistenz am wichtigsten sind, und die entsprechenden persistenzschnittstellen implementieren. Der Client entscheidet, welche Schnittstelle er bevorzugt verwenden soll. Weitere Informationen zu allen persistenzschnittstellen finden Sie in [der Component Object Model](the-component-object-model.md) .

</dd> <dt>

<span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Schriftart-und Bildobjekte
</dt> <dd>

Steuerelemente können diese vom System bereitgestellten Objekte verwenden, um eine visuelle Darstellung von sich selbst innerhalb des Clients bereitzustellen. Das Schriftart Objekt implementiert mehrere Schnittstellen, einschließlich [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) und [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp). Ein Schriftart Objekt kann mit [**olecreatefontindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect)erstellt werden. Das Bild Objekt implementiert auch mehrere Schnittstellen, einschließlich [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) und [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp). Ein Bild Objekt kann mithilfe von [**olecreatepictureindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) erstellt werden und kann aus einem Stream mit [**oleloadpicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)geladen werden.

</dd> </dl>

Es ist wichtig zu verstehen, dass diese Features in beliebigen OLE-Objekten verwendet werden können. Ein Steuerelement muss nicht implementiert werden, damit diese Features verwendet werden können. Außerdem ist die einzige erforderliche Schnittstelle für ein Steuerelement IUnknown. Das-Steuerelement unterstützt optional andere Schnittstellen, je nachdem, dass die zugehörigen Funktionen unterstützt werden müssen.

Zusätzlich zu diesen Features sind die folgenden Schnittstellen und Funktionen spezifisch für die Steuerelemente Technologie: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)und [**oletranslatecolor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor). Auch Steuerelemente sind ein Satz von Standards für Eigenschaften und Methoden, die ein Steuerelement oder ein Steuerelement Container unterstützen kann.

> [!Note]  
> Die Systembibliothek OleAut32.dll enthält Implementierungen der Funktionen ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**olecreatepropertyframeindirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**olecreatefontindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**olecreatepictureindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**oleloadpicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)und [**oletranslatecolor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)). Darüber hinaus enthält OleAut32.dll die Implementierungen der standardmäßigen Schriftart-und Bildobjekte sowie eine Typbibliothek für alle Schnittstellen, die mit Steuerelementen verwendet werden, sowie die zusätzlichen Datenstrukturen und Datentypen.

 

Weitere Informationen finden Sie unter den folgenden Themen:

-   [ActiveX-Steuerelement Architektur](activex-controls-architecture.md)
-   [ActiveX-Steuerelement Schnittstellen](activex-controls-interfaces.md)
-   [Eigenschaften und Methoden](properties-and-methods.md)
-   [Steuerelementereignisse](control-events.md)
-   [Visuelle Darstellung](visual-representation.md)
-   [Tastatur Behandlung für Steuerelemente](keyboard-handling-for-controls.md)
-   [Persistenz](persistence.md)
-   [Registrierung und Lizenzierung](registration-and-licensing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelement-und Steuerelement Container](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 