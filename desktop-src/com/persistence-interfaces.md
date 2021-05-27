---
title: Persistenzschnittstellen
description: Persistenzschnittstellen
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e1acbd1074fd5fa4e87e571a1e21ab48d5d075
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550505"
---
# <a name="persistence-interfaces"></a>Persistenzschnittstellen

Objekte mit einem permanenten Zustand jeder Art müssen mindestens eine IPersist-Schnittstelle \* und vorzugsweise mehrere Schnittstellen implementieren, um dem Container die flexibelste Wahl zu bieten, wie er den Zustand eines Steuerelements speichern möchte.

Wenn ein Steuerelement einen dauerhaften Zustand aufwies, muss es mindestens [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) oder [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) implementieren (die beiden schließen sich gegenseitig aus und sollten größtenteils nicht zusammen implementiert werden). Letzteres wird verwendet, wenn ein Steuerelement wissen möchte, wann es neu erstellt wird, anstatt es aus einem vorhandenen persistenten Zustand neu zu laden (**IPersistStream** verfügt nicht über die erstellte neue Funktion). Das Vorhandensein einer der Schnittstellen gibt an, dass das Steuerelement seinen persistenten Zustand speichern und in einen Stream laden kann, d. h. eine Instanz von [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream)

Über diese beiden streambasierten Schnittstellen hinaus können die in der folgenden Tabelle aufgeführten IPersist-Schnittstellen \* optional bereitgestellt werden, um Persistenz an anderen Speicherorten als einem erweiterbaren [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)zu unterstützen.

Eine Reihe von Komponentenkategorien wird identifiziert, um die Unterstützung für Persistenzschnittstellen zu decken. Weitere Informationen finden Sie unter [Komponentenkategorien.](component-categories.md)



| Schnittstelle                                                              | Verwendung                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | Das Objekt kann seinen Zustand speichern und in ein sequenzielles Bytearray mit fester Länge (im Arbeitsspeicher) laden.<br/>                                                                                                                                                                                                                                                    |
| [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | Das Objekt kann seinen Zustand speichern und in eine [**IStorage-Instanz**](/windows/desktop/api/objidl/nn-objidl-istorage) laden. Steuerelemente, die als Insertable (Einfügebar) als andere zusammengesetzte Dokumentobjekte (zum Einfügen in nicht steuerelementfähige Container) markiert werden sollen, müssen diese Schnittstelle unterstützen.<br/>                                                                                               |
| [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)<br/> | Das Objekt kann seinen Zustand als einzelne Eigenschaften speichern und laden, die in IPropertyBag geschrieben werden, die der Container implementiert. Dies wird für die Funktion Speichern unter Text in einigen Containern verwendet.<br/>                                                                                                                                                          |
| [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | Das -Objekt kann seinen Zustand speichern und an einen Speicherort laden, der durch einen Moniker benannt wird. Das Steuerelement ruft [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) auf, um die benötigten Speicherschnittstellen abzurufen, z. B. [**IStorage,**](/windows/desktop/api/objidl/nn-objidl-istorage) [**IStream,**](/windows/desktop/api/objidl/nn-objidl-istream) [**ILockBytes,**](/windows/desktop/api/objidl/nn-objidl-ilockbytes) [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)usw.<br/> |



 

Die Unterstützung für [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) ist zwar optional, wird jedoch dringend als Optimierung für Container mit Funktionen zum Speichern unter Text empfohlen, z. B. Visual Basic.

Mit Ausnahme von [**IPersistStream::GetSizeMax,**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax) [**IPersistStreamInit::GetSizeMax**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)und [**IPersistMemory::GetSizeMax**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85))müssen alle Methoden jeder Schnittstelle vollständig implementiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelemente](controls.md)
</dt> </dl>

 

