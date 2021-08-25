---
description: Verzögerte Befehle werden durch Aufrufe von Methoden auf der IQueueCommand-Schnittstelle in die Warteschlange gestellt und vom Filterdiagramm-Manager und von einigen Filtern verfügbar gemacht.
ms.assetid: b2b177c6-af2b-4585-914f-001a6355a298
title: CDeferredCommand-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3413deb3c606177c937aef72a8437769dc2a97acdcbee97200880c96f36f9fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910044"
---
# <a name="cdeferredcommand-class"></a>CDeferredCommand-Klasse

![cdeferredcommand-Klassenhierarchie](images/cutil13.png)

Verzögerte Befehle werden durch Aufrufe von Methoden auf der [**IQueueCommand-Schnittstelle**](/windows/desktop/api/Control/nn-control-iqueuecommand) in die Warteschlange gestellt und vom Filterdiagramm-Manager und von einigen Filtern verfügbar gemacht. Ein erfolgreicher Aufruf einer dieser Methoden gibt eine [**IDeferredCommand-Schnittstelle**](/windows/desktop/api/Control/nn-control-ideferredcommand) zurück, die den Befehl in der Warteschlange darstellt.

Ein -Objekt stellt einen einzelnen verzögerten Befehl dar und macht die `CDeferredCommand` [**IDeferredCommand-Schnittstelle**](/windows/desktop/api/Control/nn-control-ideferredcommand) sowie andere Methoden verfügbar, die Zeitüberprüfungen und die tatsächliche Ausführung zulassen. Ein `CDeferredCommand` -Objekt enthält einen Verweis auf das [**CCmdQueue-Objekt,**](ccmdqueue.md) für das es in die Warteschlange gestellt wird.

Verweisanzahlen steuern die Lebensdauer der `CDeferredCommand` Klasse. Beim Aufrufen der [**CDeferredCommand::Invoke-Memberfunktion**](cdeferredcommand-invoke.md) ruft die aufrufende Anwendung einen Schnittstellenzeiger ab, der mit Verweiszählungen gezählt wird, und das [**CCmdQueue-Objekt**](ccmdqueue.md) enthält auch eine Verweisanzahl für den verzögerten Befehl. Durch aufrufen [**der Memberfunktion IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) wird der verzögerte Befehl aus der Befehlswarteschlange entfernt und die Verweisanzahl um eins reduziert. Nachdem die Warteschlange entfernt wurde, kann der Befehl nicht mehr in die Warteschlange aufgenommen werden.



| Geschützte Datenmember                                        | BESCHREIBUNG                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| m \_ bStream                                                    | Flag für [**Die Streamzeit oder**](stream-time.md) Präsentationszeit. , die an die aufgerufene Methode übergeben werden soll.                   |
| m \_ Dispatch                                                   | Greifen Sie auf die **ITypeInfo-Schnittstelle** zu.                                                                                   |
| m \_ dispidMethod                                               | Methode für die schnittstelle, die ausgeführt werden soll.                                                                                         |
| m \_ DispParams                                                 | [**CDispParams-Objekt**](cdispparams.md) mit der **DISPPARAMS-Parameterliste**                                  |
| m \_ hrResult                                                   | Speichert den zurückgegebenen **HRESULT-Wert.**                                                                                  |
| m \_ iid                                                        | Global eindeutiger Bezeichner **(GUID)** der Schnittstelle.                                                                 |
| m \_ pQueue                                                     | Zeiger auf das [**CCmdQueue-Objekt,**](ccmdqueue.md) das die [**IQueueCommand-Schnittstelle verfügbar**](/windows/desktop/api/Control/nn-control-iqueuecommand) macht. |
| m \_ pUnk                                                       | **IUnknown-Zeiger** auf die Schnittstelle, auf der der Befehl ausgeführt wird.                                                 |
| m \_ pvarResult                                                 | Die resultierenden Informationen, falls dies der Fall ist, aus der aufgerufenen Methode.                                                                 |
| m \_ Zeit                                                       | Zeitpunkt, zu dem der Befehl ausgeführt wird.                                                                                  |
| m \_ wFlags                                                     | Flags, die den Kontext des Aufrufs angeben.                                                                         |
| Elementfunktionen                                              | BESCHREIBUNG                                                                                                             |
| [**CDeferredCommand**](cdeferredcommand-cdeferredcommand.md) | Erstellt ein **CDeferredCommand-Objekt.**                                                                               |
| [**GetFlags**](cdeferredcommand-getflags.md)                 | Ruft die Kontextflags ab, die dem verzögerten Befehl zugeordnet sind.                                                       |
| [**GetIID**](cdeferredcommand-getiid.md)                     | Ruft den Schnittstellenbezeichner (IID) der Schnittstelle ab, auf der die Methode ausgeführt wird.                              |
| [**GetMethod**](cdeferredcommand-getmethod.md)               | Ruft den Dispatchbezeichner der methode ab, die ausgeführt werden soll.                                                              |
| [**GetParams**](cdeferredcommand-getparams.md)               | Ruft die **DISPPARAMS-Argumentliste** für die -Methode ab.                                                               |
| [**GetResult**](cdeferredcommand-getresult.md)               | Ruft die resultierende Argumentliste ab, sofern vorhanden.                                                                   |
| [**Gettime**](cdeferredcommand-gettime.md)                   | Ruft den Zeitpunkt ab, zu dem die Methode ausgeführt wird.                                                                         |
| [**Invoke**](cdeferredcommand-invoke.md)                     | Ermöglicht den Zugriff auf Methoden und Eigenschaften, die von einem -Objekt verfügbar gemacht werden.                                                         |
| [**IsStreamTime**](cdeferredcommand-isstreamtime.md)         | Gibt an, ob der Befehl zur Streamzeit oder zur Präsentationszeit ausgeführt werden soll.                                         |
| IDeferredCommand-Methoden                                      | BESCHREIBUNG                                                                                                             |
| [**Abbrechen**](cdeferredcommand-cancel.md)                     | Bricht eine zuvor in der Warteschlange [**gespeicherte CDeferredCommand::Invoke-Anforderung**](cdeferredcommand-invoke.md) ab.                        |
| [**Confidence**](cdeferredcommand-confidence.md)             | Derzeit nicht implementiert.                                                                                              |
| [**Verschieben**](cdeferredcommand-postpone.md)                 | Gibt eine neue Präsentationszeit für einen Befehl in der Warteschlange an.                                                      |
| [**GetHResult**](cdeferredcommand-gethresult.md)             | Ruft den **HRESULT-Wert** der aufgerufenen Methode ab.                                                                  |



 

 

 



