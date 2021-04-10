---
description: Ein Writer kann aus vielen programmgesteuerten Gründen fehlschlagen.
ms.assetid: 50eced73-3917-4d7e-96cc-2d793b448738
title: Writer-Fehler und-Vetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c24c15ad10766fc6ec395ed058ab3cb72a689d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214614"
---
# <a name="writer-errors-and-vetoes"></a>Writer-Fehler und-Vetos

Ein Writer kann aus vielen programmgesteuerten Gründen fehlschlagen. Wenn dies der Fall ist, sollte Sie ein Veto für die laufende Sicherung, Wiederherstellung oder den Schatten Kopiervorgang durch Aufrufen der [**CVssWriter:: setwrite terfailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure) -Methode in einer ihrer Handlermethoden (z. b. [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) oder [**CVssWriter:: onprerestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) ausführen und **true** zurückgeben. Optional kann auch eine Fehlermeldungs Zeichenfolge als Reaktion auf eine Fehlerbedingung in bestimmten Handlermethoden mit dem [**ivsscomponentex-Wert festgelegt werden: setprepareforbackupfailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg), [**ivsscomponestex:: setpostsnapshotfailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg), [**IVssComponent:: setprerestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)und [**IVssComponent:: setpostrestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) -Methoden. Der Anforderer kann das Veto akzeptieren oder mit der Sicherung fortfahren, wobei das Veto ignoriert wird.

Ein Anforderer sollte den Writer-Status (mit [**IVssBackupComponents:: gatherbeschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents:: getschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)) nach jedem von ihm generierten Ereignis überprüfen.

In einigen Fällen können Fehlermeldungen von diesen Fehlern abgerufen werden (mithilfe von [**ivsscomponestex:: getprepareforbackupfailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg), [**IVssComponent:: getprerestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**ivsscomponentex:: getpostsnapshotfailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg)-und [**IVssComponent:: getpostrestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) -Methoden), oder ein Writer kann festlegen, dass Metadaten festgelegt werden (mithilfe von [**IVssComponent:: setrestoremetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata) und [**IVssComponent:: setbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) mit Fehler Zustandsinformationen). Beispielcode, der zeigt, wie Sie solche Fehlermeldungen anzeigen, finden Sie unter [**ivsscomponestex:: getprepareforbackupfailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).

Abhängig vom Fehlerzustand kann ein Anforderer oder der Operator die Sicherung und die Schatten Kopie mit ggf. notwendigen Änderungen am Status des Sicherungsauftrags oder-Systems neu starten.

Angenommen, [**getschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) hat Folgendes zurückgegeben:

-   **VSS \_ E \_ Write error \_ inkonsistentsnapshot** schlägt vor, dass ein Anforderer der Schatten Kopie zusätzliche Volumes hinzufügen kann.
-   **VSS \_ E \_ Schreibfehler \_ Retryable** gibt an, dass der Wiederholungsversuch ohne Neukonfiguration möglicherweise funktioniert. Wenn der Writer nach mehreren Wiederholungen weiterhin den Fehler zurückgibt, versuchen Sie, den Dienst neu zu starten, der den Writer hostet. Die folgenden Writer werden im VSS-Dienst gehostet: registrierungswriter, Datenbank-Writer der com+-Klassen Registrierung, Writer zur Optimierung der Schatten Kopie und ASR-Writer (Automated System Recovery). Wenn der Writer zu einer Anwendung gehört, die den Writer in einem eigenen Prozess hostet, versuchen Sie, die Anwendung neu zu starten.

    **Windows Server 2003 und Windows XP:** Die folgenden Writer werden im VSS-Dienst gehostet: registrierungswriter, Datenbank-Writer der com+-Klassen Registrierung, Anwendungs Ereignisprotokoll-Writer und Microsoft SQL Server 2000 Desktop Engine (MSDE) Writer.

-   VSS \_ E \_ Writer- \_ Status \_ nicht verfügbar gibt \_ an, dass ein Writer möglicherweise die maximale Anzahl von verfügbaren Sicherungs-und Wiederherstellungs Sitzungen erreicht hat und der Wiederholungsversuch möglicherweise funktioniert, wenn das System weniger ausgelastet ist.
-   **VSS \_ E \_ Schreibfehler \_ oudefresources** oder **VSS \_ E \_ schreibfehlertimeout \_** deutet möglicherweise darauf hin, dass die Systemlast vor dem erneuten Versuch reduziert wird.
-   **VSS \_ E \_ Schreibfehler nicht \_ wiederholbar** oder **VSS \_ E \_ Writer \_ \_ antwortet nicht** , würde wahrscheinlich auf einen Writer-Fehler hinweisen, der so schwer ist, dass versucht wird, die Daten mit VSS zu sichern.

Je nachdem, welcher Writer und welche Komponenten diese generieren, ist es nicht immer erforderlich, dass eine Sicherungs Anwendung nach einem Veto oder Fehler abgebrochen wird.

Beispielsweise kann eine anfordernde Person festlegen, dass die Absicht der Schatten Kopie darin besteht, Anwendung a zu sichern, und das Veto wurde vom Writer für die Sicherungs Anwendung B empfangen. In diesem Fall ist es durchaus akzeptabel, die Anwendung A zu sichern, während das Veto ignoriert wird.

Im folgenden finden Sie Beispiele für ein Writer-Veto:

-   Der Writer überprüft den Prozess der Schattenkopieerstellung, wenn er seine Aktivitäten während der Erstellung der Schatten Kopie nicht aussetzen konnte. Dies weist darauf hin, dass eine hohe Wahrscheinlichkeit besteht, dass die Schatten Kopie ungültig ist, da während des Fixierungs Zustands ein Schreibvorgang aufgetreten ist.
-   Eine Sicherungs Anwendung hat eine Schatten Kopie von Volume c: angefordert, und ein Writer bestimmt, dass eine Schatten Kopie von C: und D: zum Sichern der Daten dient. In diesem Fall wird der Writer in ein Veto schreiben. Die Sicherungs Anwendung kann die Metadaten untersuchen und bestimmen, ob der Writer ignoriert oder der Vorgang zum Erstellen von Schatten Kopien abgebrochen und später neu gestartet wird.

 

 



