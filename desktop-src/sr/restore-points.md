---
title: Wiederherstellungspunkte
description: Wiederherstellungspunkte werden erstellt, um Benutzern die Auswahl vorheriger Systemzustände zu ermöglichen. Jeder Wiederherstellungspunkt enthält die erforderlichen Informationen, um den ausgewählten Zustand des Systems wiederherzustellen. Wiederherstellungspunkte werden erstellt, bevor wichtige Änderungen am System vorgenommen werden.
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 56cc7035f2e5a152ad90205257fb86ddaef8bf565f8459cb5067874280946db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968039"
---
# <a name="restore-points"></a>Wiederherstellungspunkte

Wiederherstellungspunkte werden erstellt, damit Benutzer einen vorherigen Systemstatus auswählen können. Jeder Wiederherstellungspunkt enthält die erforderlichen Informationen, um den ausgewählten Zustand des Systems wiederherzustellen. Wiederherstellungspunkte werden erstellt, bevor wichtige Änderungen am System vorgenommen werden.

Die Systemwiederherstellung verwaltet automatisch den Speicherplatz, der wiederhergestellten Punkten zugeordnet ist. Die ältesten Wiederherstellungspunkte werden gelöscht, um Platz für neue wiederherzustellen. Bei der Systemwiederherstellung wird Speicherplatz basierend auf der Größe der Festplatte und der Version der Windows, die auf dem Computer ausgeführt wird, wie in der folgenden Tabelle gezeigt.

|Windows-Version |&nbsp;Festplattengröße |Systemwiederherstellungsspeicherplatz |
| --- | --- | --- |
|Windows 7 und höher | > 64 GB |Bis zu fünf Prozent des gesamten Speicherplatzes auf dem Datenträger oder maximal 10 GB, was weniger ist |
|  | &le; 64 GB |Bis zu drei Prozent des gesamten Speicherplatzes auf dem Datenträger |
|Windows Vista |  |Bis zu 15 Prozent des gesamten Speicherplatzes auf dem Datenträger oder maximal 30 Prozent des verfügbaren Speicherplatzes, unabhängig davon, welcher Speicherplatz geringer ist |
|Windows XP | >4 GB |Bis zu 12 Prozent des gesamten Speicherplatzes auf dem Datenträger<br /><br />Verwenden Sie zum Ändern des maximalen Speicherlimits in Windows XP das **Element System** in Systemsteuerung. |
|  | \< 4 GB |Bis zu 400 MB |

## <a name="event-triggered-restore-points"></a>Ereignisauslöser für Wiederherstellungspunkte

Die Systemwiederherstellung erstellt automatisch einen Wiederherstellungspunkt, bevor eines der folgenden Ereignisse eintritt:

- **Anwendungsinstallation** (gilt nur für Anwendungen, die ein systemwiederherstellungskonformes Installationsprogramm verwenden). Wenn die Anwendungsinstallation Systemprobleme verursacht, kann der Benutzer das System in einem Zustand vor der Installation wiederherstellen.
- **Windows Update- oder AutoUpdate-Installation.** Windows Update (früher als AutoUpdate bezeichnet) lädt automatisch Windows herunter und installiert sie. Darüber hinaus bietet es Benutzern eine einfache Möglichkeit, Updates manuell herunterzuladen und zu installieren. Bei der Systemwiederherstellung wird ein Wiederherstellungspunkt erstellt, bevor ein Update automatisch oder manuell installiert wird.
- **Systemwiederherstellungsvorgang**. Die Systemwiederherstellung erstellt automatisch einen Wiederherstellungspunkt als Sicherung, bevor ein Wiederherstellungsvorgang gestartet wird. Angenommen, ein Benutzer stellt versehentlich eine wiederhergestellte Windows fehlerhaften Wiederherstellungspunkt wieder. Um diese Wiederherstellung rückgängig zu machen, kann der Benutzer Windows auf einen Wiederherstellungspunkt wiederherstellen, der vor dem ersten Wiederherstellungspunkt liegt. Nachdem Windows wiederhergestellt wurde, kann der Benutzer den Vorgang wiederholen und dieses Mal den richtigen Wiederherstellungspunkt auswählen.

## <a name="scheduled-restore-points"></a>Geplante Wiederherstellungspunkte

Benutzer können die Systemwiederherstellung so konfigurieren, dass in regelmäßigen Abständen Wiederherstellungspunkte erstellt werden. Benutzer können einen Wiederherstellungspunkt auch jederzeit manuell über die Benutzeroberfläche für die Systemwiederherstellung erstellen und benennen. Diese Wiederherstellungspunkte werden gespeichert und komprimiert und sind in der Liste der Wiederherstellungspunkte verfügbar.

In Windows 7 und höher erstellt die Systemwiederherstellung nur dann einen geplanten Wiederherstellungspunkt, wenn in den letzten sieben Tagen keine anderen Wiederherstellungspunkte erstellt wurden. In Windows Vista erstellt die Systemwiederherstellung alle 24 Stunden einen Prüfpunkt, wenn an diesem Tag keine anderen Wiederherstellungspunkte erstellt wurden. In Windows XP erstellt die Systemwiederherstellung alle 24 Stunden einen Prüfpunkt, unabhängig von anderen Vorgängen.

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a>Bekanntes Problem: Sie können das System nicht auf einem Wiederherstellungspunkt wiederherstellen, nachdem Sie ein Windows 10 installiert haben.

Nehmen Sie das folgende Szenario als Beispiel:

1. Sie installieren Windows 10 auf einem bereinigten Computer.
1. Sie aktivieren den Systemschutz und erstellen dann einen Systemwiederherstellungspunkt mit dem Namen "R1".
1. Sie installieren mindestens ein Windows 10 Updates.
1. Nachdem die Installation der Updates abgeschlossen ist, stellen Sie das System auf den Wiederherstellungspunkt "R1" wieder auf.

In diesem Szenario wird das System nicht auf den Wiederherstellungspunkt "R1" wiederhergestellt. Stattdessen tritt auf dem Computer ein Stop-Fehler (0xc000021a) auf. Sie starten den Computer neu, aber das System kann nicht zum Desktop Windows werden.

### <a name="cause"></a>Ursache

Dies ist ein bekanntes Problem in Windows 10.

Während des Systemwiederherstellungsprozesses wird Windows die Wiederherstellung von dateien, die verwendet werden, vorübergehend gephasen. Anschließend werden die Informationen in der Registrierung gespeichert. Wenn der Computer neu gestartet wird, schließt er den gestufigen Vorgang ab.

In diesem Fall stellt Windows die Katalogdateien wieder auf und stellt die Treiberdateien (.sys) für die Wiederherstellung beim Neustart des Computers zur Wiederherstellung auf. Wenn der Computer jedoch neu gestartet wird, Windows die vorhandenen Treiber geladen, bevor die neueren Versionen der Treiber wiederhergestellt werden. Da die Treiberversionen nicht mit den Versionen der wiederhergestellten Katalogdateien übereinstimmen, wird der Neustartvorgang beendet.

### <a name="workaround"></a>Problemumgehung

**So stellen Sie die Wiederherstellung nach dem fehlgeschlagenen Neustart wieder auf und setzen den Wiederherstellungsvorgang fort**

Starten Sie den Computer nach dem Auftreten des Fehlers neu, bis er in die Windows Recovery Environment (WinRE) gelangt. Hierzu müssen Sie möglicherweise einen Hardwareneustartschalter verwenden, und Sie müssen möglicherweise mehrmals neu starten.

In der Windows Recovery Environment:

1. Wählen **Sie**  >  **Problembehandlung Erweiterte Optionen** Weitere  >  **Wiederherstellungsoptionen**  >  **Starteinstellungen** und dann Neu starten **aus.**
1. Wählen Sie in der Liste der Starteinstellungen **Treibersignaturerzwingung deaktivieren aus.**
   > [!NOTE]  
   > Möglicherweise müssen Sie die Taste F7 verwenden, um diese Einstellung auszuwählen.
1. Lassen Sie den Startprozess fortsetzen. Wenn Windows neu gestartet wird, sollte der Prozess der Systemwiederherstellung fortgesetzt und abgeschlossen werden.

Mit diesen Schritten wird der Computer in seinen Zustand "R1" wiederhergestellt.

**So stellen Sie nach dem fehlgeschlagenen Neustart wieder eine Wiederherstellung**

Führen Sie die folgenden Schritte aus, um die Wiederherstellung nach dem fehlgeschlagenen Neustart und dem Wiederherstellungsvorgang wiederherzustellen:

1. Starten Sie wie im vorherigen Verfahren beschrieben den Computer neu, und geben Sie dann WinRE ein.  
1. Wählen Sie Windows Wiederherstellungsumgebung die **Option** Problembehandlung Erweiterte Optionen Systemwiederherstellung aus, und wählen Sie dann  >    >   **Systemwiederherstellung rückgängig machen aus.**

Diese Schritte geben den Computer in den Zustand zurück, in dem er sich vor dem Starten des Wiederherstellungsvorgangs aufwies.

**So stellen Sie Windows wiederhergestellten Wiederherstellungspunkt mithilfe von WinRE wieder**

Um den Assistenten für die Systemwiederherstellung auf einem betroffenen Computer zu starten, verwenden Sie WinRE anstelle Einstellungen **Dialogfelds** . Gehen Sie hierzu folgendermaßen vor:

1. Wählen **Sie Start**  >  **Einstellungen** Update &  >  **Security** Recovery  >  **aus.**
1. Wählen **Sie unter Erweiterte Optionen** die Option Jetzt neu starten **aus.**
1. Nachdem WinRE gestartet wurde, wählen Sie **Problembehandlung**  >  **Erweiterte Optionen**  >  **Systemwiederherstellung aus.**
1. Geben Sie Ihren Wiederherstellungsschlüssel ein, wie er auf dem Bildschirm angezeigt wird, und befolgen Sie dann die Anweisungen im Assistenten für die Systemwiederherstellung.

### <a name="references"></a>Referenzen

Weitere Informationen zur Verwendung von WinRE finden Sie in den folgenden Artikeln:

- [Windows-Wiederherstellungsumgebung (Windows RE)](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [Starten Sie Ihren PC im abgesicherten Modus in Windows 10](https://support.microsoft.com/help/12376) 