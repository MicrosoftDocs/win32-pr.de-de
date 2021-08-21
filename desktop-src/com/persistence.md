---
title: Persistenz
description: Persistenz
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c8600307bfe6c29f72fb9d29e633358062c4e8c1c61da8898173cf190f1d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500330"
---
# <a name="persistence"></a>Persistenz

Ein Steuerelement implementiert mindestens eine von mehreren Persistenzschnittstellen, um die Persistenz seines Zustands zu unterstützen. Die [**IPersistStreamInit-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) unterstützt beispielsweise die streambasierte Persistenz des Zustands des Steuerelements. **IPersistStreamInit** ist ein Ersatz für [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) und fügt die Initialisierungsmethode [**InitNew hinzu.**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew) Die anderen Methoden sind in beiden Schnittstellen identisch. **IPersistStreamInit** wird nicht von **IPersistStream** abgeleitet; Ein -Objekt unterstützt nur eine der beiden Schnittstellen, je danach, ob es die Möglichkeit erfordert, neue Instanzen von sich selbst zu initialisieren.

Andere Persistenzschnittstellen, die ein Steuerelement bieten kann, sind: [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistMemory,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)) [**IPersistPropertyBag,**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). Der Steuerelement-Implementierer muss entscheiden, welche Arten von Persistenz am wichtigsten sind, und die entsprechenden Persistenzschnittstellen implementieren. Die Steuerelement-Implementierung entscheidet auch, was gespeichert werden soll. Beispielsweise kann ein Steuerelement die aktuellen Werte seiner Eigenschaften oder seine Position und Größe in seinem Container speichern. Der Client entscheidet, welche Schnittstelle er bevorzugt verwendet.

Vor dem Laden eines Steuerelements aus seinem persistenten Zustand kann ein Client das OLEMISC \_ SETCLIENTSITEFIRST-Flag überprüfen, um zu ermitteln, ob das Steuerelement das Abrufen des Clientstandorts und der Umgebungseigenschaften vor dem Laden des persistenten Zustands unterstützt. Diese Optimierung kann Beim Instanziieren eines Steuerelements Zeit sparen, da das Steuerelement dann seine persistenten Werte ignorieren kann, anstatt sie nur zu laden, damit sie von umgebungseigenschaften überschrieben werden, die vom Client bereitgestellt werden.

Ein Steuerelement kann auch das Speichern und Wiederherstellen seines Zustands in einem OLE-Eigenschaftensatz, einem Satz von Bezeichnern und Werten in einem angegebenen Format unterstützen. Diese Funktion kann bei Containern wie Visual Basic nützlich sein, die ihre Programme in textueller Form speichern. Ein Steuerelement, das dieses Feature unterstützen möchte, implementiert [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) und [**IDataObject::SetData,**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) um dessen Eigenschaftswerte an bzw. aus dem Container zu übergeben. Es ist der Auftrag des Containers, diese Informationen in Text zu konvertieren und zu speichern. Die vom Steuerelement verwendeten Bezeichner entsprechen den Eigenschaftennamen des Steuerelements und den Werten. Die Definition dieses Eigenschaftensatzes finden Sie im OLE CDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 