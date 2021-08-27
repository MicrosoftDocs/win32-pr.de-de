---
title: Persistenzschnittstellen
description: Persistenzschnittstellen
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4894ccb1cc5d17747739e78918da9a5b48e2cca13a9f36078d752fceeaef011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120420"
---
# <a name="persistence-interfaces"></a>Persistenzschnittstellen

Objekte mit einem persistenten Zustand jeder Art müssen mindestens eine IPersist-Schnittstelle und vorzugsweise mehrere Schnittstellen implementieren, um dem Container die flexibelste Auswahl zu bieten, wie er den Zustand eines Steuerelements speichern \* möchte.

Wenn ein Steuerelement einen dauerhaften Zustand hat, muss es mindestens [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) oder [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) implementieren (die beiden schließen sich gegenseitig aus und sollten zum größten Teil nicht zusammen implementiert werden). Letzteres wird verwendet, wenn ein Steuerelement wissen möchte, wann es neu erstellt wird, anstatt aus einem vorhandenen persistenten Zustand neu geladen zu werden (**IPersistStream** verfügt nicht über die erstellte neue Funktion). The existence of either interface indicates that the control can save and load its persistent state into a stream, that is, an instance of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Über diese beiden streambasierten Schnittstellen hinaus können die in der folgenden Tabelle aufgeführten IPersist-Schnittstellen optional bereitgestellt werden, um Persistenz an anderen Speicherorten als einem erweiterbaren IStream zu \* [**unterstützen.**](/windows/desktop/api/objidl/nn-objidl-istream)

Ein Satz von Komponentenkategorien wird identifiziert, um die Unterstützung für Persistenzschnittstellen zu decken. Weitere Informationen finden Sie unter [Komponentenkategorien.](component-categories.md)



| Schnittstelle                                                              | Verbrauch                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | Das Objekt kann seinen Zustand speichern und in ein sequenzielles Bytearray mit fester Länge (im Arbeitsspeicher) laden.<br/>                                                                                                                                                                                                                                                    |
| [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | Das Objekt kann seinen Zustand speichern und in eine [**IStorage-Instanz**](/windows/desktop/api/objidl/nn-objidl-istorage) laden. Steuerelemente, die als Insertable als andere zusammengesetzte Dokumentobjekte (zum Einfügen in nicht steuerelementfähige Container) markiert werden sollen, müssen diese Schnittstelle unterstützen.<br/>                                                                                               |
| [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)<br/> | Das Objekt kann seinen Zustand als einzelne Eigenschaften speichern und laden, die in den vom Container implementierten IPropertyBag geschrieben werden. Dies wird für die Funktion "Als Text speichern" in einigen Containern verwendet.<br/>                                                                                                                                                          |
| [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | Das Objekt kann seinen Zustand speichern und an einen Speicherort laden, der von einem Moniker benannt wird. Das Steuerelement ruft [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) auf, um die benötigten Speicherschnittstellen abzurufen, z. B. [**IStorage,**](/windows/desktop/api/objidl/nn-objidl-istorage) [**IStream,**](/windows/desktop/api/objidl/nn-objidl-istream) [**ILockBytes,**](/windows/desktop/api/objidl/nn-objidl-ilockbytes) [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)usw.<br/> |



 

Die Unterstützung für [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) ist zwar optional, wird jedoch dringend als Optimierung für Container mit Funktionen zum Speichern unter Text empfohlen, z. B. Visual Basic.

Mit Ausnahme von [**IPersistStream::GetSizeMax,**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax) [**IPersistStreamInit::GetSizeMax**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)und [**IPersistMemory::GetSizeMax**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85))müssen alle Methoden jeder Schnittstelle vollständig implementiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelemente](controls.md)
</dt> </dl>

 

