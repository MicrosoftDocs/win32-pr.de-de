---
title: Persistenzschnittstellen
description: Persistenzschnittstellen
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72ef5f7381c6d58b9025f983ecd852b83661030
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102451"
---
# <a name="persistence-interfaces"></a>Persistenzschnittstellen

Objekte mit einem permanenten Zustand einer beliebigen Art müssen mindestens eine ipersistent- \* Schnittstelle und vorzugsweise mehrere Schnittstellen implementieren, um dem Container die flexibelste Wahl zu bieten, wie der Zustand eines Steuer Elements gespeichert werden soll.

Wenn ein Steuerelement einen persistenten Zustand aufweist, muss es als Minimalwert entweder [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) oder [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) implementieren (beide schließen sich gegenseitig aus und sollten für den größten Teil nicht gemeinsam implementiert werden). Letzteres wird verwendet, wenn ein Steuerelement wissen möchte, wenn es neu erstellt wird, anstatt von einem vorhandenen persistenten Zustand neu geladen zu werden (**IPersistStream** verfügt nicht über die erstellte neue Funktion). Das vorhanden sein einer der beiden Schnittstellen gibt an, dass das Steuerelement seinen permanenten Zustand speichern und in einen Stream laden kann, d. h. eine Instanz von [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Über diese beiden streambasierten Schnittstellen hinaus \* können die in der folgenden Tabelle aufgeführten ipersistent-Schnittstellen optional bereitgestellt werden, um die Persistenz an anderen Speicherorten als einem erweiterbaren [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)zu unterstützen.

Eine Reihe von Komponenten Kategorien wird identifiziert, um die Unterstützung für Persistenz-Schnittstellen abzudecken. siehe [Komponenten Kategorien](component-categories.md).



| Schnittstelle                                                              | Verbrauch                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ipersistmemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | Das Objekt kann seinen Zustand speichern und in ein sequenzielles Bytearray mit fester Länge (im Arbeitsspeicher) laden.<br/>                                                                                                                                                                                                                                                    |
| [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | Das Objekt kann seinen Zustand speichern und in eine [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Instanz laden. Steuerelemente, die als "Insertable" markiert werden sollen, als andere Verbund Dokument Objekte (für Einfügevorgänge in Container ohne Kontrolle) müssen diese Schnittstelle unterstützen.<br/>                                                                                               |
| [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))<br/> | Das Objekt kann seinen Zustand als einzelne Eigenschaften speichern und laden, die in IPropertyBag geschrieben werden, die der Container implementiert. Diese wird für die Funktion "Speichern als Text" in einigen Containern verwendet.<br/>                                                                                                                                                          |
| [**Ipersistmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | Das Objekt kann seinen Zustand speichern und in einen Speicherort laden, der von einem Moniker benannt wird. Das Steuerelement ruft [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) auf, um die erforderliche Speicherschnittstelle abzurufen, z. b. [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/objidl/nn-objidl-ilockbytes), [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)usw.<br/> |



 

Die Unterstützung für [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) ist zwar optional, aber es wird dringend empfohlen, als Optimierung für Container mit Funktionen zum Speichern als Text zu empfehlen, wie z. b. Visual Basic.

Mit Ausnahme von [**IPersistStream:: GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax), [**IPersistStreamInit:: GetSizeMax**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)und [**ipersistmemory:: GetSizeMax**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85))müssen alle Methoden jeder Schnittstelle vollständig implementiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelemente](controls.md)
</dt> </dl>

 

