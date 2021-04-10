---
description: Verzögerte Befehle werden von Aufrufen von Methoden in der iqueuecommand-Schnittstelle in die Warteschlange eingereiht und vom Filter Graph-Manager und einigen Filtern verfügbar gemacht.
ms.assetid: b2b177c6-af2b-4585-914f-001a6355a298
title: Cdeferredcommand-Klasse
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
ms.openlocfilehash: 8d3db3f35b5589a6cd17791d72aa9931124ccfbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125300"
---
# <a name="cdeferredcommand-class"></a>Cdeferredcommand-Klasse

![cdeferredcommand-Klassenhierarchie](images/cutil13.png)

Verzögerte Befehle werden von Aufrufen von Methoden in der [**iqueuecommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) -Schnittstelle in die Warteschlange eingereiht und vom Filter Graph-Manager und einigen Filtern verfügbar gemacht. Ein erfolgreicher Aufruf einer dieser Methoden gibt eine [**ideferredcommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) -Schnittstelle zurück, die den Befehl in der Warteschlange darstellt.

Ein `CDeferredCommand` -Objekt stellt einen einzelnen verzögerten Befehl dar und macht die [**ideferredcommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) -Schnittstelle sowie andere Methoden verfügbar, die Zeit Überprüfungen und tatsächliche Ausführung zulassen. Ein- `CDeferredCommand` Objekt enthält einen Verweis auf das [**ccmdqueue**](ccmdqueue.md) -Objekt, für das es in die Warteschlange eingereiht wird.

Verweis Zähler steuern die Lebensdauer der- `CDeferredCommand` Klasse. Beim Aufrufen der [**cdeferredcommand::**](cdeferredcommand-invoke.md) Call-Member-Funktion wird von der aufrufenden Anwendung ein Schnittstellen Zeiger mit Verweis Zählung abgerufen, und das [**ccmdqueue**](ccmdqueue.md) -Objekt enthält außerdem einen Verweis Zähler für den verzögerten Befehl. Durch Aufrufen der [**ideferredcommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) -Member-Funktion wird der verzögerte Befehl von der Befehls Warteschlange entfernt, wodurch der Verweis Zähler um 1 reduziert wird. Sobald der Befehl aus der Warteschlange entfernt wurde, kann er nicht wieder in der Warteschlange abgelegt werden.



| Geschützte Datenmember                                        | BESCHREIBUNG                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| m \_ bStream                                                    | Flag für die [**streamzeit**](stream-time.md) oder Präsentationszeit. , das an die aufgerufene Methode übermittelt werden soll.                   |
| Mio \_ . Verteilung                                                   | Greift auf die **itypeingefo** -Schnittstelle zu.                                                                                   |
| m \_ dispidmethod                                               | Methode für die zu testende Schnittstelle.                                                                                         |
| m- \_ dispparser                                                 | [**Cdispparameams**](cdispparams.md) -Objekt, das die **dispparameams** -Parameterliste enthält.                                  |
| m \_ hrresult                                                   | Speichert den zurückgegebenen **HRESULT** -Wert.                                                                                  |
| m \_ IID                                                        | **GUID**(Global Unique Identifier) der Schnittstelle.                                                                 |
| m \_ pqueue                                                     | Zeiger auf das [**ccmdqueue**](ccmdqueue.md) -Objekt, das die [**iqueuecommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) -Schnittstelle verfügbar macht. |
| m- \_ Punk                                                       | **IUnknown** -Zeiger auf die-Schnittstelle, für die der Befehl ausgeführt wird.                                                 |
| m \_ pVarResult                                                 | Resultierende Informationen, sofern vorhanden, aus der aufgerufenen Methode.                                                                 |
| m \_ Zeit                                                       | Der Zeitpunkt, zu dem der Befehl ausgeführt wird.                                                                                  |
| m- \_ wFlags                                                     | Flags, die den Kontext des aufaufruf angeben.                                                                         |
| Elementfunktionen                                              | BESCHREIBUNG                                                                                                             |
| [**Cdeferredcommand**](cdeferredcommand-cdeferredcommand.md) | Erstellt ein **cdeferredcommand** -Objekt.                                                                               |
| [**GetFlags**](cdeferredcommand-getflags.md)                 | Ruft die dem verzögerten Befehl zugeordneten kontexflags ab.                                                       |
| [**Getiid**](cdeferredcommand-getiid.md)                     | Ruft den Schnittstellen Bezeichner (IID) der Schnittstelle ab, auf der die Methode ausgeführt wird.                              |
| [**GetMethod**](cdeferredcommand-getmethod.md)               | Ruft den Dispatchbezeichner der Methode ab, die ausgeführt werden soll.                                                              |
| [**GetParams**](cdeferredcommand-getparams.md)               | Ruft die **DISPPARAMS** -Argumentliste an die-Methode ab.                                                               |
| [**GetResult**](cdeferredcommand-getresult.md)               | Ruft die resultierende Argumentliste ab, sofern eine vorhanden ist.                                                                   |
| [**GetTime**](cdeferredcommand-gettime.md)                   | Ruft den Zeitpunkt ab, zu dem die Methode ausgeführt wird.                                                                         |
| [**Invoke**](cdeferredcommand-invoke.md)                     | Bietet Zugriff auf Methoden und Eigenschaften, die von einem-Objekt verfügbar gemacht werden.                                                         |
| [**Isstreamtime**](cdeferredcommand-isstreamtime.md)         | Gibt an, ob der Befehl zur streamzeit oder Präsentationszeit ausgeführt werden soll.                                         |
| Ideferredcommand-Methoden                                      | BESCHREIBUNG                                                                                                             |
| [**Abbrechen**](cdeferredcommand-cancel.md)                     | Bricht eine zuvor in die Warteschlange eingereihte [**cdeferredcommand:: Aufrufen**](cdeferredcommand-invoke.md) -Anforderung ab.                        |
| [**Confidence**](cdeferredcommand-confidence.md)             | Derzeit nicht implementiert.                                                                                              |
| [**Verschieben**](cdeferredcommand-postpone.md)                 | Gibt eine neue Präsentationszeit für einen zuvor in die Warteschlange eingereihten Befehl an.                                                      |
| [**GetHResult**](cdeferredcommand-gethresult.md)             | Ruft den **HRESULT** -Wert der aufgerufenen Methode ab.                                                                  |



 

 

 



