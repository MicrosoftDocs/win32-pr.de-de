---
title: Persistenz
description: Persistenz
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6cffab1c9a0f2746e57e356a90698caf9903deb
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549285"
---
# <a name="persistence"></a>Persistenz

Ein Steuerelement implementiert eine oder mehrere von mehreren Persistenzschnittstellen, um die Persistenz des Zustands zu unterstützen. Die [**IPersistStreamInit-Schnittstelle unterstützt**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) beispielsweise die streambasierte Persistenz des Zustands des Steuerelements. **IPersistStreamInit ist** ein Ersatz für [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) und fügt die Initialisierungsmethode [**InitNew hinzu.**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew) Die anderen Methoden sind in beiden Schnittstellen identisch. **IPersistStreamInit** wird nicht von **IPersistStream abgeleitet.** Ein -Objekt unterstützt nur eine der beiden Schnittstellen, je darauf, ob es die Möglichkeit erfordert, neue Instanzen von sich selbst zu initialisieren.

Weitere Persistenzschnittstellen, die ein Steuerelement bieten kann, sind: [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). Der Implementer des Steuerelements muss entscheiden, welche Arten von Persistenz am wichtigsten sind, und die entsprechenden Persistenzschnittstellen implementieren. Der Implementer des Steuerelements entscheidet auch, was zu speichern ist. Beispielsweise kann ein Steuerelement die aktuellen Werte seiner Eigenschaften oder seine Position und Größe in seinem Container speichern. Der Client entscheidet, welche Schnittstelle er bevorzugt.

Vor dem Laden eines Steuerelements aus seinem persistenten Zustand kann ein Client das OLEMISC SETCLIENTSITEFIRST-Flag überprüfen, um zu ermitteln, ob das Steuerelement das Abrufen seiner Clientstandort- und Umgebungseigenschaften unterstützt, bevor der persistente Zustand geladen \_ wird. Diese Optimierung kann beim Instanziieren eines Steuerelements Zeit sparen, da das Steuerelement dann seine persistenten Werte ignorieren kann, anstatt sie nur zu laden, damit sie von umgebungseigenschaften überschrieben werden, die vom Client bereitgestellt werden.

Ein Steuerelement kann auch das Speichern und Wiederherstellen seines Zustands in einem OLE-Eigenschaftensatz, einem Satz von Bezeichnern und Werten in einem angegebenen Format, unterstützen. Dieses Feature kann bei Containern wie Visual Basic nützlich sein, die seine Programme in Textform speichern. Ein Steuerelement, das dieses Feature unterstützen möchte, implementiert [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) und [**IDataObject::SetData,**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) um dessen Eigenschaftswerte an bzw. aus dem Container zu übergeben. Es ist aufgabe des Containers, diese Informationen in Text zu konvertieren und zu speichern. Die vom Steuerelement verwendeten Bezeichner entsprechen den Eigenschaftennamen des Steuerelements und den Werten. Die Definition dieses Eigenschaftensatzes finden Sie im OLE CDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 