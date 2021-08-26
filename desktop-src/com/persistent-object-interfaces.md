---
title: Persistente Objektschnittstellen (COM)
description: Ein persistentes -Objekt implementiert eine oder mehrere persistente Objektschnittstellen.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ee1062c80a5c40d139965e0e3bebf96cbda534062322e218e2f5a7da586ff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120410"
---
# <a name="persistent-object-interfaces"></a>Persistente Objektschnittstellen

Ein persistentes -Objekt implementiert eine oder mehrere *persistente Objektschnittstellen.* Clients verwenden persistente Objektschnittstellen, um diesen Objekten mitzuteilen, wann und wo ihr Zustand gespeichert werden soll. Alle permanenten Objektschnittstellen werden von [**IPersist**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist)abgeleitet, sodass jedes Objekt, das eine persistente Objektschnittstelle implementiert, auch **IPersist** implementiert.

Die folgenden persistenten Objektschnittstellen sind derzeit definiert:

-   [**Ipersiststream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**Ipersistfile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Implementierer wählen aus, welche permanenten Objektschnittstellen ein Objekt unterstützt, je nachdem, wie das Objekt verwendet werden soll. Da keine permanenten Objektschnittstellen unterstützt werden, sagt der Implementierer effektiv: "Der Zustand dieses Objekts kann nicht dauerhaft gespeichert werden." Durch die Unterstützung einer oder mehrerer persistenter Objektschnittstellen sagt der Implementierer effektiv: "Der Zustand dieses Objekts kann dauerhaft in einem oder mehreren Datenspeichermedien gespeichert werden."

In der folgenden Tabelle sind beispielsweise mehrere Objekttypen aufgeführt, die Unterstützung für verschiedene persistente Objektschnittstellen ermöglichen.



| Kategorie                            | Persistente Objektschnittstellen werden in der Regel unterstützt.                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Moniker<br/>                 | [**Ipersiststream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| OLE-einbettbare Objekte<br/>   | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| ActiveX-Steuerelemente<br/>         | [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)IPersistMemory, IPersistPropertyBag, [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| ActiveX Dokumentobjekte<br/> | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Client-Implementierer können auch auswählen, welche permanenten Objektschnittstellen der Client verwenden kann. Die Schnittstellen, die ein Client verwendet, werden in der Regel durch den Ort bestimmt, an dem der Client seine eigenen Daten speichern kann. Ein Client, der seine Daten nur in einer Flatfile speichern kann, verwendet wahrscheinlich nur [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))und IPersistPropertyBag. (**IPersistStreamInit** kann [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) in den meisten Anwendungen ersetzen, da es diese Definition enthält und eine Initialisierungsmethode hinzufügt.) Ein Client, der seine Daten in einer strukturierten Speicherdatei speichern kann, verwendet zusätzlich [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Initialisieren persistenter Objekte](initializing-persistent-objects.md)
</dt> </dl>

 

