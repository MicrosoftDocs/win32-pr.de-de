---
description: Ein Writer kann aus zahlreichen programmgesteuerten Gründen fehlschlagen.
ms.assetid: 50eced73-3917-4d7e-96cc-2d793b448738
title: Schreibfehler und -fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0835775aec21da9aa69e81b4f7af63f98d765b5c72763cb52af706c4e7a720e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124460"
---
# <a name="writer-errors-and-vetoes"></a>Schreibfehler und -fehler

Ein Writer kann aus zahlreichen programmgesteuerten Gründen fehlschlagen. In diesem Fall sollte der laufende Sicherungs-, Wiederherstellungs- oder Schattenkopievorgang durch Aufrufen der [**CVssWriter::SetWriterFailure-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure) in einer seiner Handlermethoden (z. B. [**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) oder [**CVssWriter::OnPreRestore)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)blockiert und **TRUE zurückgeben.** Optional kann eine Fehlermeldungszeichenfolge auch als Reaktion auf eine Fehlerbedingung in bestimmten Handlermethoden mit den Methoden [**IVssComponentEx::SetPrepareForBackupFailureMsg,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg) [**IVssComponentEx::SetPostSnapshotFailureMsg,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg) [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)und [**IVssComponent::SetPostRestoreFailureMsg festgelegt**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) werden. Der Anfordernde kann die Sicherung akzeptieren oder mit der Sicherung fortfahren und dabei die Sicherung ignorieren.

Eine Anfordernde sollte den Writerstatus (mithilfe von [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents::GetWriterStatus)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)nach jedem generierten Ereignis überprüfen.

In einigen Fällen Fehlermeldungen können aus diesen Fehlern abgerufen werden (mithilfe von [**IVssComponentEx::GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg), [**IVssComponent::GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**IVssComponentEx::GetPostSnapshotFailureMsg-**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg)und [**IVssComponent::GetPostRestoreFailureMsg-Methoden**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) oder ein Writer können Metadaten festlegen (mithilfe von [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata) und [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) mit Fehlerzustandsinformationen). Beispielcode zum Anzeigen solcher Fehlermeldungen finden Sie unter [**IVssComponentEx::GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).

Je nach Fehlerstatus kann ein An anfordernde Oder dessen Operator die Sicherung und Schattenkopie mit jeder erforderlichen Änderung des Zustands des Sicherungsauftrags oder -systems neu starten.

Angenommen, [**GetWriterStatus hat**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) Folgendes zurückgegeben:

-   **VSS \_ E \_ WRITERERROR \_ INKONSISTENTSNAPSHOT** schlägt vor, dass ein Anfordernde der Schattenkopie möglicherweise zusätzliche Volumes hinzufüge
-   **VSS \_ E \_ WRITERERROR \_ RETRYABLE gibt** an, dass ein Wiederholungsversuch ohne Neukonfiguration möglicherweise funktioniert. Wenn der Writer den Fehler nach mehreren Versuchen weiterhin zurücksendet, versuchen Sie, den Dienst neu zu starten, der den Writer hostet. Die folgenden Writer werden im VSS-Dienst gehostet: Registrierungswriter, DATENBANK-Writer für COM+-Klassenregistrierung, Schattenkopieoptimierungs-Writer und ASR-Writer (Automated System Recovery). Wenn der Writer zu einer Anwendung gehört, die den Writer in seinem eigenen Prozess hostet, versuchen Sie, die Anwendung neu zu starten.

    **Windows Server 2003 und Windows XP:** Die folgenden Writer werden im VSS-Dienst gehostet: Registrierungswriter, DATENBANK-Writer für COM+-Klassenregistrierung, Anwendungsereignisprotokoll-Writer und Microsoft SQL Server 2000 Desktop Engine-Writer (MSDE).

-   VSS E WRITER STATUS NOT AVAILABLE gibt an, dass ein Writer möglicherweise die maximale Anzahl verfügbarer Sicherungs- und Wiederherstellungssitzungen erreicht hat, und wiederholungsversuche funktionieren möglicherweise, wenn das System weniger \_ \_ \_ \_ \_ ausgelastet ist.
-   **VSS \_ E \_ WRITERERROR \_ OUTOFRESOURCES** oder **VSS \_ E \_ WRITERERROR \_ TIMEOUT** schlagen möglicherweise vor, dass die Systemlast vor dem Erneuten Versuchen reduziert wird.
-   **VSS \_ E \_ WRITERERROR \_ NONRETRYABLE** oder **VSS \_ E WRITER NOT \_ \_ \_ RESPONDING** deutet wahrscheinlich auf einen Writerfehler hin, der so schwerwiegend ist, dass nicht versucht wird, seine Daten mit VSS zu sichern.

Je nachdem, welcher Writer und welche Komponenten sie generieren, ist es nicht immer erforderlich, dass eine Sicherungsanwendung nach einem Fehler oder Fehler abgebrochen wird.

Beispielsweise kann ein Anfordernde entscheiden, dass die Schattenkopie die Sicherung von Anwendung A und die Sicherungsanwendung B vom Writer erhalten hat. In diesem Fall ist es durchaus akzeptabel, Anwendung A weiterhin zu sichern und dabei die N-Unglange zu ignorieren.

Im Folgenden finden Sie Beispiele für einen Writer:

-   Der Writer blockiert den Erstellungsprozess für Schattenkopien, wenn seine Aktivitäten während der Erstellung der Schattenkopie nicht angehalten werden konnten. Dies weist darauf hin, dass die Wahrscheinlichkeit hoch ist, dass die Schattenkopie ungültig ist, da während des Freeze-Zustands ein Schreibvorgang aufgetreten ist.
-   Eine Sicherungsanwendung hat nur eine Schattenkopie von Volume C: angefordert, und ein Writer bestimmt, dass eine Schattenkopie von C: und D: die Daten sichern soll. In diesem Fall wird der Writer als Schreiber bezeichnet. Die Sicherungsanwendung kann die Metadaten überprüfen und bestimmen, ob der Writer ignoriert wird oder der Erstellungsprozess für Schattenkopien abgebrochen und später neu gestartet wird.

 

 



