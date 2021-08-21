---
description: Wenn eine Anwendung über Besitzerberechtigungen für eine Kommunikationssitzung verfügt, kann die Anwendung den Besitz an eine andere Anwendung übertragen.
ms.assetid: d6d188c9-9cbd-45af-93f0-b78850374919
title: Übergaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60668fa5c0138de137e0dab81ba8159d00b7727f7eca699d207128615db5c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866136"
---
# <a name="handoffs"></a>Übergaben

Wenn eine Anwendung über [Besitzerberechtigungen für](privilege-ovr.md) eine Kommunikationssitzung verfügt, kann die Anwendung den Besitz an eine andere Anwendung übertragen. Der Übergabevorgang wird normalerweise verwendet, um das Ändern des Medientyps des Aufrufs zu ermöglichen. Die Anwendung mit der höchsten Priorität für den neuen Medientyp sollte den Aufruf übernehmen und verarbeiten. Die Änderung des Medientyps tritt in der Regel aus einem der folgenden Gründe auf.

**Benutzerbefehl:** Über eine Benutzeroberfläche oder über Fenstermeldungen lernt die Anwendung, dass der lokale Benutzer den Medientyp ändern möchte. Beispielsweise hat der Benutzer der neuen Zielanwendung (die noch kein Besitzer ist) mitgeteilt, einen vorhandenen Sprachanruf zum Übertragen von Daten zu erhalten. Die Zielanwendung muss nun die Kontrolle über den Aufruf übernehmen. In diesem Fall bemerkt der aktuelle Besitzer, dass die Anzahl der Besitzer steigt, und gibt dann seine Kontrolle über den Aufruf auf. Alternativ kann der Benutzer den aktuellen Besitzer des Aufrufs anweisen, ihn an eine Anwendung zu überweisen, die den neuen Medientyp verarbeiten kann.

**Medientypänderung:** Der Dienstanbieter kann eine Medientypänderung erkennen. Beispielsweise gibt die lokale Anwendung eine aufgezeichnete Sprachnachricht an den Anrufer ab. Während dieser Nachricht entscheidet sich der Aufrufer, einen Faxanrufton zu übertragen, und die lokale Anwendung kann entsprechend reagieren, indem er den Medientyp in ein Fax ändert und bei Bedarf den Anruf an eine Faxanwendung übergibt. Eine andere Möglichkeit besteht in der Aktivierung der Medientypüberwachung durch eine Überwachungsanwendung. Wenn der Medientyp, an dem sie interessiert ist, bei einem Aufruf erkannt wird, kann sie den Besitz des Aufrufs anfordern. Durch diesen Mechanismus ist es für jede Anwendung nicht erforderlich, jeden Aufruf für jeden Medientyp zu überwachen.

**Remotepartybefehl:** Die Remote-Partei kann während eines vorhandenen Aufrufs interaktiv auf eine Änderung der Medientypen hinweisen, z. B. ob die lokale Anwendung die EINGABEN des Remoteaufrufers überwacht. Durch diese Überwachung gibt der Aufrufer beispielsweise an, dass ein Fax gesendet werden soll. Andere Möglichkeiten, wie der Aufrufer lokale Anwendungen steuern kann, sind Befehle, die über andere Datenverbindungen und über ISDN-Benutzerinformationsmeldungen empfangen werden.

Eine Anruf-Übergabe hat eines der folgenden Ergebnisse:

-   Der Aufruf wird an eine andere Anwendung (SUCCESS) erfolgen.
-   Die Übergabeanwendung ist selbst das Ziel (TARGETSELF).
-   Die Übergabe schlägt fehl (TARGETNOTFOUND).

Wenn die Anwendung, die den übergebenen Aufruf empfängt, bereits über ein Anrufhand handle für den Aufruf verfügt, wird dieses alte Aufrufhand handle verwendet. Andernfalls wird ein neues Aufrufhand handle erstellt. In beiden Fällen hat die Anwendung besitzerrechte für den Aufruf. Wenn die Übergabeanwendung nicht mit der Zielanwendung identisch ist, wird das Ziel in einer Sitzungszustandsmeldung über die Übergabe informiert, als würde es einen neuen Aufruf empfangen.

Wenn die aktuelle Besitzeranwendung dazu aufgerufen wird, Medientypen zu ändern, wird der Aufruf an eine Anwendung, die für den Zielmedientyp verwendet wird, abgesendet. Die beiden Typen von Anrufhandoffs werden unter [Directed Handoffs](#directed-handoffs) und [Media type Handoffs (Handoffs des Medientyps) beschrieben.](#media-type-handoffs)

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2.x:** Siehe [**lineHandoff ,**](/windows/win32/api/tapi/nf-tapi-linehandoff)bei *dem lpszFileName* für eine direkte Übergabe auf den Anwendungsnamen oder *dwMediaMode* für eine indirekte Übergabe auf einen Medientyp festgelegt ist.

**TAPI 3.x:** Siehe [**ITBasicCallControl::HandoffDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffdirect), [**ITBasicCallControl::HandoffIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect).

## <a name="directed-handoffs"></a>Gerichtete Übergaben

Eine *gerichtete Übergabe erfolgt,* wenn die Zielanwendung der ursprünglichen Anwendung durch den Namen bekannt ist. Diese Situation tritt z. B. bei einer Gruppe von Anwendungen auf, die vom gleichen Anbieter geschrieben wurden. Der Benutzer kann in der Regel die Steuerung von gerichteten Übergaben konfigurieren. Bei einer solchen Übergabe wird der Aufruf an die angegebene Anwendung erteilt, wenn sie die Zeile geöffnet hat, in der der Aufruf vorhanden ist. Der Medientyp, der beim Öffnen der Zeile durch die Anwendung angegeben wurde, wird ignoriert. Ein häufiges Beispiel ist ein Sprachanruf, gefolgt von einer Faxübertragung im selben Anruf. Die gesteuerte Übergabe wird am häufigsten von Anwendungen desselben Entwicklers verwendet, die auch auf andere Weise verknüpft sind.

Die gesteuerte Übergabe kann auch in zukünftigen Versionen als Teil des Prozesses verwendet werden, bei dem mehrere Anwendungen auf eingehende Aufrufe desselben Medientyps warten, und die Auswahl der Anwendung für die Verarbeitung des Aufrufs basiert auf der Erkennung von Datenlinks oder Protokollen auf höherer Ebene anstelle des Medientyps. Ein Beispiel für die Verwendung ist eine eingehende Datenmodemverbindung mit Anwendungen wie Remoteübernahme, Bulletin Board, Remotenetzwerkzugriff und Remote-E-Mail-Zugriff, die alle gleichzeitig auf Aufrufe warten.

## <a name="media-type-handoffs"></a>Medientyphandoffs

Eine *Medientyp-Übergabe* findet statt, wenn ein neuer, gezielter Medientyp vorhanden ist, in der Regel, wenn die besitzende Anwendung feststellt, dass der für den Aufruf benötigte Medientyp nicht vorhanden ist oder sich ändern wird.

Der Prozess für eine medienabhängige Übergabe kann ein Probeprozess sein, wenn der Medientyp UNKNOWN bit ein on ist. Es liegt in der Verantwortung der zuständigen Anwendung, Medientypen zu durchzyklen, um die Anwendung mit der höchsten Priorität zu finden. TAPI durchfing dies nur beim ersten eingehenden Aufruf, um den ersten Besitzer zu finden. Dies wird für einen Übergabevorgang nicht durchgeführt. Andernfalls ist eine Übergabe praktisch identisch mit der ersten Zuweisung eines Aufrufs einer Anwendung. Der Unterschied besteht in der Tatsache, dass nur ein Medientyp für eine indirekte Übergabe (Medientyp) festgelegt werden kann.

Da nur ein einzelnes Medientypbit angegeben werden kann, wird der Aufruf an die Anwendung mit der höchsten Priorität für diesen Medientyp erteilt. Es ist jedoch möglich, dass mehrere Medientypen für die Übergabe berücksichtigt werden. In diesem Fall sollte die Übergabeanwendung die höchste Priorität der möglichen Medientypen als Parameter angeben.

Wenn eine Anwendung das UNKNOWN-Bit angibt, wenn eine Medientyp-Übergabe ausgeführt wird und die Übergabe fehlschlägt, bedeutet dies, dass eine unbekannte Anwendung, die die Medientypermittlung durchführen kann, derzeit nicht ausgeführt wird. Die Anwendung, die die Übergabe vor sich hat, sollte dann versuchen, den Aufruf an die Anwendung mit der höchsten Priorität zu überschreiben, die für den Medientyp mit der nächsten höheren Priorität registriert ist.

Die empfangende Anwendung ist jetzt für den Aufruf verantwortlich. Er prüft nun den tatsächlichen Medientyp des Aufrufs. Wenn die Anwendung den Medientyp des Aufrufs verarbeiten kann, muss sie sicherstellen, dass es sich um die Anwendung mit der höchsten Priorität handelt, die für diesen Medientyp registriert ist. Wenn dies der Regelfall ist, behält er den Aufruf bei und verarbeitet ihn normal. Wenn nicht, wird der Aufruf an eine andere Anwendung übertragen, die für diesen Medientyp registriert ist.

Wenn der Test für diesen Medientyp jedoch fehlschlägt, prüft die Anwendung erneut und versucht, die verbleibenden Medienmodusmöglichkeiten zu nutzen. Zuerst muss das aktuelle Medientypbit deaktiviert und dann eine weitere Übergabe mit einem anderen Typ versucht werden.

Dieser Prozess der Probe und Übergabe wird fortgesetzt, und die verbleibenden Medientypen werden nach und nach entfernt. Dabei kann eine der Anwendungen erkennen, dass sich der von ihr verarbeitete Medientyp im Aufruf befindet und die Übergabe erfolgreich ist.

Die Anwendung sollte dann den richtigen Medientyp festlegen und alle anderen Medientypbits löschen. Dadurch werden andere interessierten Anwendungen über den richtigen Medientyp informiert. Diese anderen Anwendungen erhalten eine Ereignisbenachrichtigung, die besagt, dass sich der Medientyp des Aufrufs geändert hat.

 

 
