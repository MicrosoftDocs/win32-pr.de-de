---
description: Das calljekt wird erstellt, wenn ein-Rückruf vorhanden ist. Zugeordnete Schnittstellen abrufen und festlegen Informationen über den-Befehl.
ms.assetid: cff131c0-9f4a-418d-b486-155bd71e9316
title: Objekt Schnittstellen abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccb7fb9ed07fad8bd952aff806d39aa2db5e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959850"
---
# <a name="call-object-interfaces"></a>Objekt Schnittstellen abrufen

Das [calljekt](call-object.md) wird erstellt, wenn ein-Rückruf vorhanden ist. Zugeordnete Schnittstellen abrufen und festlegen Informationen über den-Befehl.

Enumerator-und Ereignis Schnittstellen werden nicht direkt für das callsobjekt verfügbar gemacht, sondern sind hier aufgeführt.

Die [**itcallnotificationevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)-, [**itcallinfochangeevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)-, [**itcallstateevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)-, [**itcallmediaevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)-und [**ienumterminalclass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) -Schnittstellen werden nicht direkt für das Aufruf Objekt verfügbar gemacht, sind jedoch eng damit verknüpft und werden hier zur Verfügung gestellt.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                               | Stellt Informationen zu einem calltobjekt bereit, z. b. den Aufrufstatus oder die verwendeten Terminals.                                       |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                             | Erweitert [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) durch Bereitstellen von Methoden zum Festlegen der Ereignis Filterung pro Aufruf.                    |
| [**Itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)               | Wird verwendet, um eine Verbindung herzustellen, diese zu beantworten und grundlegende telefonievorgänge für ein Anruf Objekt auszuführen.                                            |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)             | Erweitert [**itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) durch Bereitstellen von Methoden, um ein Terminal für einen-Befehl auszuwählen.              |
| [**Itcallnotificationevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)     | Benachrichtigungs Schnittstelle für [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                 |
| [**Itcallinfochangeevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)         | Benachrichtigungs Schnittstelle für Änderungen an den aufrufsinformationen.                                                                      |
| [**Itcallstateevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)                   | Ruft Informationen zu einem Ereignis des-Ereignisses ab.                                                                                    |
| [**Itcallmediaevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)                   | Ruft Informationen zu einem Ereignis zum Abrufen von Medien ab.                                                                              |
| [**Itcustomtone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                           | Stellt Methoden bereit, um die mit einigen Telefon Sätzen möglichen benutzerdefinierten Töne zu steuern.                                                  |
| [**Itdetecttone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                           | Stellt Methoden bereit, um die Töne und die Tonmerkmale anzugeben, die Tone-Ereignisse generieren.                                    |
| [**Itlegacycallmediacontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol)   | Unterstützt Legacy Anwendungen, die direkt mit einem Gerät kommunizieren müssen.                                                   |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2) | Erweitert [**itlegacycallmediacontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) durch Bereitstellen von Methoden für die Tone-Erkennung und-Generierung. |
| [**Ienumcall**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                 | Listet [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)auf.                                                                                 |



 

 

 



