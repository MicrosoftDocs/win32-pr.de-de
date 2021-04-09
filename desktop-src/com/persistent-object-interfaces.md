---
title: Persistente Objekt Schnittstellen (com)
description: Ein persistentes Objekt implementiert eine oder mehrere persistente Objekt Schnittstellen.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df8920f1242d077044654d1090adcc0e3f3f05c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949172"
---
# <a name="persistent-object-interfaces"></a>Persistente Objekt Schnittstellen

Ein persistentes Objekt implementiert eine oder mehrere *persistente Objekt Schnittstellen*. Clients verwenden persistente Objekt Schnittstellen, um diese Objekte zu informieren, wann und wo ihr Zustand gespeichert werden soll. Alle persistenten Objekt Schnittstellen werden von [**ipersistent**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist)abgeleitet, sodass jedes Objekt, das eine persistente Objektschnittstelle implementiert, auch **ipersistent** implementiert.

Die folgenden permanenten Objekt Schnittstellen sind aktuell definiert:

-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**Ipersistmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [Ipersistmemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Implementierer wählen Sie aus, welche persistenten Objekt Schnittstellen ein Objekt unterstützt, je nachdem, wie das Objekt verwendet werden soll. Wenn keine permanenten Objekt Schnittstellen unterstützt werden, sagt der Implementierer tatsächlich, dass der Zustand dieses Objekts nicht dauerhaft gespeichert werden kann. Durch die Unterstützung einer oder mehrerer persistenter Objekt Schnittstellen besagt der Implementierer, dass der Zustand dieses Objekts dauerhaft in einem oder mehreren Datenspeichermedien gespeichert werden kann.

In der folgenden Tabelle sind z. b. mehrere Objekttypen aufgeführt, die Unterstützung für unterschiedliche persistente Objekt Schnittstellen ermöglichen.



| Category                            | Persistente Objekt Schnittstellen unterstützt                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Moniker<br/>                 | [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| OLE-einbettbare Objekte<br/>   | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| ActiveX-Steuerelemente<br/>         | [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), ipersistmemory, IPersistPropertyBag, [**ipersistmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| ActiveX-Dokument Objekte<br/> | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Client Implementierungen können auch auswählen, welche permanenten Objekt Schnittstellen vom Client verwendet werden können. Die von einem Client verwendeten Schnittstellen werden in der Regel durch den Ort bestimmt, an dem der Client seine eigenen Daten speichern kann Ein Client, der seine Daten nur in einer Flatfile speichern kann, verwendet wahrscheinlich nur [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**ipersistmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))und IPersistPropertyBag. (**IPersistStreamInit** kann [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) in den meisten Anwendungen ersetzen, da es diese Definition enthält und eine Initialisierungs Methode hinzufügt.) Ein Client, der seine Daten in einer strukturierten Speicherdatei speichern kann, verwendet zusätzlich [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Initialisieren von persistenten Objekten](initializing-persistent-objects.md)
</dt> </dl>

 

