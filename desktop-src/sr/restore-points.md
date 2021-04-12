---
title: Wiederherstellungspunkte
description: Wiederherstellungspunkte werden erstellt, um Benutzern die Möglichkeit zu geben, die vorherigen Systemzustände auszuwählen. Jeder Wiederherstellungspunkt enthält die erforderlichen Informationen, die erforderlich sind, um das System im ausgewählten Zustand wiederherzustellen. Wiederherstellungspunkte werden erstellt, bevor wichtige Änderungen am System vorgenommen werden.
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 6ef1aba7d1cb018bb3fa4f32d868828ef2ac4d1b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316094"
---
# <a name="restore-points"></a>Wiederherstellungspunkte

Wiederherstellungspunkte werden erstellt, um Benutzern das Auswählen eines früheren Systemstatus zu ermöglichen. Jeder Wiederherstellungspunkt enthält die erforderlichen Informationen, um das System im ausgewählten Zustand wiederherzustellen. Wiederherstellungspunkte werden erstellt, bevor wichtige Änderungen am System vorgenommen werden.

Die System Wiederherstellung verwaltet automatisch den Speicherplatz, der für Wiederherstellungspunkte reserviert ist. Die ältesten Wiederherstellungspunkte werden bereinigt, um Platz für neue Wiederherstellungspunkte zu schaffen. Durch die System Wiederherstellung wird Speicherplatz basierend auf der Größe der Festplatte und der von dem Computer ausgeführten Windows-Version zugewiesen, wie in der folgenden Tabelle dargestellt.

|Windows-Version |Festplatten &nbsp; Größe |System Wiederherstellungs Bereich |
| --- | --- | --- |
|Windows 7 und höhere Versionen | > 64 GB |Bis zu fünf Prozent des gesamten Speicherplatzes oder maximal 10 GB, je nachdem, welcher Wert kleiner ist. |
|  | &le; 64 GB |Bis zu drei Prozent des gesamten Speicherplatzes |
|Windows Vista |  |Bis zu 15 Prozent des gesamten Speicherplatzes oder maximal 30 Prozent des verfügbaren Speicherplatzes, je nachdem, welcher Wert kleiner ist. |
|Windows XP | >4 GB |Bis zu 12 Prozent des gesamten Speicherplatzes<br /><br />Verwenden Sie das System Element in der **System** Steuerung, um die maximale Speicherbeschränkung in Windows XP zu ändern. |
|  | \< 4 GB |Bis zu 400 MB |

## <a name="event-triggered-restore-points"></a>Ereignisgesteuerte Wiederherstellungspunkte

Die System Wiederherstellung erstellt automatisch einen Wiederherstellungspunkt, bevor eines der folgenden Ereignisse auftritt:

- **Anwendungs Installation** (gilt nur für Anwendungen, die einen System Wiederherstellungs kompatiblen Installer verwenden). Wenn die Anwendungs Installation System Probleme verursacht, kann der Benutzer das System in einen Zustand versetzen, der der Installation vorausgeht.
- **Windows Update-oder AutoUpdate-Installation**. Mit Windows Update (früher als "AutoUpdate" bezeichnet) werden Windows-Updates automatisch heruntergeladen und installiert. Außerdem bietet es Benutzern eine einfache Möglichkeit, Updates manuell herunterzuladen und zu installieren. Bei der System Wiederherstellung wird vor der Installation eines Updates ein Wiederherstellungspunkt erstellt, ob automatisch oder manuell.
- **System Wiederherstellungs Vorgang**. Die System Wiederherstellung erstellt automatisch einen Wiederherstellungspunkt als Sicherung, bevor ein Wiederherstellungs Vorgang gestartet wird. Nehmen Sie beispielsweise an, dass ein Benutzer versehentlich Windows an einem falschen Wiederherstellungspunkt wiederherstellt. Um diese Wiederherstellung rückgängig zu machen, kann der Benutzer Windows auf einem Wiederherstellungspunkt wiederherstellen, der dem ersten Wiederherstellungspunkt vorangestellt ist. Nachdem Windows in seinem ursprünglichen Zustand wieder hergestellt wurde, kann der Benutzer den Vorgang wiederholen, indem er den richtigen Wiederherstellungspunkt ausgewählt hat.

## <a name="scheduled-restore-points"></a>Geplante Wiederherstellungspunkte

Benutzer können die System Wiederherstellung zum Erstellen von Wiederherstellungs Punkten in regelmäßigen Abständen konfigurieren. Benutzer können einen Wiederherstellungspunkt auch jederzeit manuell von der Benutzeroberfläche der System Wiederherstellung aus erstellen und benennen. Diese Wiederherstellungspunkte werden gespeichert und komprimiert und sind in der Liste der Wiederherstellungspunkte verfügbar.

In Windows 7 und höheren Versionen erstellt die System Wiederherstellung nur dann einen geplanten Wiederherstellungspunkt, wenn in den letzten sieben Tagen keine weiteren Wiederherstellungspunkte erstellt wurden. In Windows Vista erstellt die System Wiederherstellung alle 24 Stunden einen Prüfpunkt, wenn an diesem Tag keine weiteren Wiederherstellungspunkte erstellt wurden. In Windows XP erstellt die System Wiederherstellung einen Prüfpunkt alle 24 Stunden, unabhängig von anderen Vorgängen.

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a>Bekanntes Problem: nach der Installation eines Windows 10-Updates kann das System nicht wieder hergestellt werden.

Nehmen Sie das folgende Szenario als Beispiel:

1. Sie installieren Windows 10 auf einem sauberen Computer.
1. Aktivieren Sie den Systemschutz, und erstellen Sie dann einen Systemwiederherstellungspunkt mit dem Namen "R1".
1. Sie installieren mindestens ein Windows 10-Update.
1. Nachdem die Installation der Updates abgeschlossen ist, stellen Sie das System auf dem Wiederherstellungspunkt "R1" wieder her.

In diesem Szenario wird das System nicht am Wiederherstellungspunkt "R1" wieder hergestellt. Stattdessen hat der Computer einen Fehler beim Abbrechen (0xC000021A). Der Computer wird neu gestartet, aber das System kann nicht zum Windows-Desktop zurückkehren.

### <a name="cause"></a>Ursache

Dies ist ein bekanntes Problem in Windows 10.

Während der Systemwiederherstellung wird die Wiederherstellung von Dateien, die gerade verwendet werden, von Windows vorübergehend durchlaufen. Anschließend werden die Informationen in der Registrierung gespeichert. Wenn der Computer neu gestartet wird, wird der gestaffelte Vorgang abgeschlossen.

In diesem Fall stellt Windows die Katalogdateien wieder her und stellt die Treiberdateien (sys) bereit, die wieder hergestellt werden sollen, wenn der Computer neu gestartet wird. Wenn der Computer jedoch neu gestartet wird, werden die vorhandenen Treiber von Windows geladen, bevor die späteren Treiberversionen wieder hergestellt werden. Da die Treiberversionen nicht mit den Versionen der wiederhergestellten Katalogdateien identisch sind, wird der Neustart Vorgang beendet.

### <a name="workaround"></a>Problemumgehung

**So stellen Sie einen fehlerhaften Neustart her und setzen den Wiederherstellungsprozess fort**

Nachdem der Fehler aufgetreten ist, starten Sie den Computer neu, bis er in die Windows-Wiederherstellungs Umgebung (WinRE) wechselt. Zu diesem Zweck müssen Sie möglicherweise einen Neustart des Hardware-Neustarts verwenden, und Sie müssen möglicherweise mehrmals neu starten.

In der Windows-Wiederherstellungs Umgebung:

1. Wählen **Sie Problem** Behandlung  >  **Erweiterte Optionen**  >  **weitere Wiederherstellungsoptionen**  >  **Start Einstellungen** aus, und klicken Sie dann auf **jetzt neu starten**.
1. Wählen Sie in der Liste der Start Einstellungen die Option **Durchsetzung der Treiber Signatur deaktivieren** aus.
   > [!NOTE]  
   > Sie müssen möglicherweise die Taste F7 verwenden, um diese Einstellung auszuwählen.
1. Lassen Sie den Startvorgang fortsetzen. Wenn Windows neu gestartet wird, sollte der System Wiederherstellungs Vorgang fortgesetzt und abgeschlossen werden.

Mit diesen Schritten wird der Computer wieder in den Zustand "R1" versetzt.

**So stellen Sie einen fehlerhaften Neustart wieder her**

Führen Sie die folgenden Schritte aus, um die Wiederherstellung nach dem fehlgeschlagenen Neustart auszuführen

1. Starten Sie den Computer neu, und geben Sie dann WinRE ein, wie im vorherigen Verfahren beschrieben.  
1. **Wählen Sie** in der Windows-Wiederherstellungs Umgebung Problembehandlung  >  **Erweiterte Optionen**  >  **Systemwiederherstellung**, und wählen Sie dann **Systemwiederherstellung rückgängig machen** aus.

Mit diesen Schritten wird der Computer wieder in den Zustand versetzt, in dem er sich vor Beginn des Wiederherstellungs Vorgangs befand.

**So stellen Sie Windows mithilfe von WinRE an einem Wiederherstellungspunkt wieder her**

Verwenden Sie WinRE anstelle des Dialog Felds **Einstellungen** , um den Systemwiederherstellungs-Assistenten auf einem betroffenen Computer zu starten. Gehen Sie hierzu folgendermaßen vor:

1. Wählen Sie **Start**  >  **Einstellungen**  >  **Aktualisieren & Sicherheits**  >  **Wiederherstellung** aus.
1. Wählen Sie unter **Erweiterte Optionen die Option** **jetzt neu starten** aus.
1. **Wählen Sie** nach dem Start von WinRE Problembehandlung  >  **Erweiterte Optionen**  >  **System Wiederherstellung** aus.
1. Geben Sie Ihren Wiederherstellungs Schlüssel ein, wie er auf dem Bildschirm angezeigt wird, und befolgen Sie dann die Anweisungen im Systemwiederherstellungs-Assistenten.

### <a name="references"></a>References

Weitere Informationen zur Verwendung von WinRE finden Sie in den folgenden Artikeln:

- [Windows-Wiederherstellungsumgebung (Windows RE)](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [Starten des Computers im abgesicherten Modus in Windows 10](https://support.microsoft.com/help/12376) 