---
description: Das Call-Objekt wird erstellt, wenn ein Aufruf existiert. Zugeordnete Schnittstellen rufen Informationen zum Aufruf ab und legen diese fest.
ms.assetid: cff131c0-9f4a-418d-b486-155bd71e9316
title: Aufrufen von Objektschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41d01c95ff2f387345eae570ef3cc67012e826a9ee104161d9c4a279118c121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947698"
---
# <a name="call-object-interfaces"></a>Aufrufen von Objektschnittstellen

Das [Call-Objekt](call-object.md) wird erstellt, wenn ein Aufruf existiert. Zugeordnete Schnittstellen rufen Informationen zum Aufruf ab und legen diese fest.

Enumerator- und Ereignisschnittstellen werden nicht direkt im Aufrufobjekt verfügbar gemacht, sondern sind hier zur Vereinfachung der Referenz aufgeführt.

Die [**Schnittstellen ITCallNotificationEvent,**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent) [**ITCallInfoChangeEvent,**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent) [**ITCallStateEvent,**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)und [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) werden nicht direkt im Call-Objekt verfügbar gemacht, sondern sind eng damit verknüpft und werden hier zur Referenzfreundlichkeit aufgeführt.



| Schnittstelle                                                      | Beschreibung                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                               | Stellt Informationen zu einem Call-Objekt bereit, z. B. den Aufrufzustand oder die in Gebrauchenen Terminals.                                       |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                             | Erweitert [**ITCallInfo,**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) indem Methoden zum Festlegen der Ereignisfilterung pro Aufruf zur Verfügung gestellt werden.                    |
| [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)               | Wird verwendet, um eine Verbindung herzustellen, antworten und grundlegende Telefonievorgänge für ein Anrufobjekt durchzuführen.                                            |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)             | Erweitert [**ITBasicCallControl,**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) indem Methoden zum Auswählen eines Terminals für einen Aufruf zur Verfügung stehen.              |
| [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)     | Benachrichtigungsschnittstelle für [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                 |
| [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)         | Benachrichtigungsschnittstelle für Änderungen in Anrufinformationen.                                                                      |
| [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)                   | Ruft Informationen zu einem Aufrufereignis ab.                                                                                    |
| [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)                   | Ruft Informationen zu einem Aufrufmedienereignis ab.                                                                              |
| [**ITCustomTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                           | Bietet Methoden zum Steuern der benutzerdefinierten Töne, die mit einigen Telefonsätzen möglich sind.                                                  |
| [**ITDetectTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                           | Stellt Methoden zum Angeben der Töne und Tonmerkmale zur Verfügung, die Tonereignisse generieren.                                    |
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol)   | Unterstützt Ältere Anwendungen, die direkt mit einem Gerät kommunizieren müssen.                                                   |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2) | Erweitert [**ITLegacyCallMediaControl durch die**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) Bereitstellung von Methoden für die Tonerkennung und -generierung. |
| [**IEnumCall**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                 | Enumeriert [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                                 |



 

 

 



