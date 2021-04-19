---
description: 'VSS ermöglicht, dass viele Schatten Kopien gleichzeitig vorhanden sind, aber nur die Erstellung eines schattenkopiespeichersets zwischen dem Befehl IVssBackupComponents:: startnapshotset und der Rückgabe des Aufrufes von IVssBackupComponents::D osnapshotset.'
ms.assetid: 26657fc2-180f-4ebb-820c-2159e7fe7584
title: Fehlerbehandlung bei schattenkopieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5f040526f63a0fe57fc5a49ac903e8b60b76646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359557"
---
# <a name="error-handling-in-shadow-copy-providers"></a>Fehlerbehandlung bei schattenkopieanbietern

VSS ermöglicht, dass viele Schatten Kopien gleichzeitig vorhanden sind, aber nur die Erstellung eines schattenkopiespeichersets zwischen dem Befehl [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) und der Rückgabe des Aufrufes von [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).

## <a name="no-partial-commit"></a>Kein teilcommit

Wenn ein Anbieter eine Schatten Kopie auf einem Volume oder einer LUN im Schattenkopiesatz nicht erstellt, schlägt die Erstellung des gesamten schattenkopiesatzes fehl. Dies ist beabsichtigt. Dieser Entwurf vereinfacht die Verhaltensprobleme, die bei der Semantik des partiellen Fehlers auftreten, und behält einen konsistenten Zeitpunkt über alle Schatten Kopien in der Menge hinweg bei.

## <a name="reporting-fault-conditions"></a>Melden von Fehlerbedingungen

Wenn ein Anbieter Fehler oder eine Fehlerbedingung auftritt, muss der Anbieter einen Fehler im Anwendungs Ereignisprotokoll protokollieren. Dies umfasst auch anbieterspezifische Fehler beim Erstellen oder Importieren eines schattenkopiesatzes oder einen Fehler bei der Ressourcen Zuordnung für die Kopier-/schreibschattenkopie nach der Erstellung. Diese Protokollierung darf nicht durchgeführt werden, wenn sich die Volumes im Schattenkopiesatz in einem fixierten Zustand befinden.

## <a name="valid-provider-return-values"></a>Gültige Anbieter Rückgabewerte

In der folgenden Tabelle werden die gültigen Rückgabecodes für Anbieter Methoden und deren Bedeutungen aufgelistet.



| Wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span>S \_ OK<br/>                                                                                                                     | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                  |
| <span id="E_OUTOFMEMORY"></span><span id="e_outofmemory"></span>E \_ outo-Memory<br/>                                                                                          | Der Anbieter verfügt nicht über genügend Arbeitsspeicher oder andere Systemressourcen.<br/>                                                                                                                                                                                    |
| <span id="E_INVALIDARG"></span><span id="e_invalidarg"></span>E \_ invalidArg<br/>                                                                                             | Einer der Parameterwerte ist ungültig.<br/>                                                                                                                                                                                                   |
| <span id="E_ACCESSDENIED"></span><span id="e_accessdenied"></span>E \_ AccessDenied<br/>                                                                                       | Ein nicht privilegierter Client hat versucht, den Anbieter aufzurufen.<br/>                                                                                                                                                                                |
| <span id="VSS_E_BAD_STATE"></span><span id="vss_e_bad_state"></span>VSS \_ E ungültiger \_ \_ Status<br/>                                                                                  | Entweder wird der angeforderte Vorgang von keinem Anbieter unterstützt, oder der Vorgang kann nicht für das Objekt ausgeführt werden, da sich das Objekt nicht im richtigen Zustand befindet.<br/>                                                                                     |
| <span id="VSS_E_OBJECT_NOT_FOUND"></span><span id="vss_e_object_not_found"></span>VSS \_ E- \_ Objekt \_ nicht \_ gefunden<br/>                                                            | Ein Parameter verweist auf ein Objekt, das nicht gefunden wurde (z. b. eine Schatten Kopie-ID, eine Schattenkopiesatz-ID oder ein Volume).<br/>                                                                                                                               |
| <span id="VSS_E_INSUFFICIENT_STORAGE"></span><span id="vss_e_insufficient_storage"></span>VSS \_ E \_ nicht genügend \_ Speicherplatz<br/>                                                 | Der Anbieter kann den Vorgang nicht durchführen, da nicht genügend Speicherplatz vorhanden ist.<br/>                                                                                                                                                           |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED"></span><span id="vss_e_volume_not_supported"></span>VSS \_ E \_ - \_ Volume \_ wird nicht unterstützt.<br/>                                                | Der angeforderte Vorgang auf dem Volume wird von keinem Anbieter unterstützt.<br/>                                                                                                                                                                |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER"></span><span id="vss_e_volume_not_supported_by_provider"></span>VSS \_ E \_ - \_ Volume \_ wird \_ vom \_ Anbieter nicht unterstützt.<br/>          | Der Anbieter unterstützt das Volume nicht.<br/>                                                                                                                                                                                                   |
| <span id="VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED"></span><span id="vss_e_maximum_number_of_snapshots_reached"></span>VSS \_ E \_ Maximale \_ Anzahl \_ von \_ Momentaufnahmen \_ erreicht<br/> | Der Anbieter hat die maximal unterstützte Anzahl von Schatten Kopien erreicht.<br/>                                                                                                                                                           |
| <span id="VSS_E_PROVIDER_VETO"></span><span id="vss_e_provider_veto"></span>VSS \_ E- \_ Anbieter- \_ Veto<br/>                                                                      | Der Anbieter hat einen internen Laufzeitfehler feststellt, der keinem anderen Rückgabewert zugeordnet ist. Der Anbieter muss auch ein Ereignis in das Anwendungs Ereignisprotokoll schreiben, um dem Benutzerinformationen zum Beheben dieses Problems zu geben.<br/> |
| <span id="VSS_E_CANNOT_REVERT_DISKID"></span><span id="vss_e_cannot_revert_diskid"></span>VSS \_ E \_ kann \_ \_ DiskId nicht zurücksetzen.<br/>                                                | Die MBR-Signatur oder GPT-ID für einen oder mehrere Datenträger konnte nicht auf den angeforderten Wert festgelegt werden. Weitere Informationen finden Sie im Anwendungs Ereignisprotokoll.<br/>                                                                                            |



 

Der Anbieter sollte nicht versuchen, andere Fehlercodes zurückzugeben.

Wenn der Anbieter einen Fehlercode zurückgibt, der nicht erwartet wird (z. b. **\_ false**, **e \_ Fail**, **e \_ unerwartete** oder **e \_ Abort**), schreibt VSS ein Ereignis in das Ereignisprotokoll, in dem der Anbieter und **die fehlerhafte Methode erwähnt \_ \_ \_ \_** werden Dies erfolgt nicht bei Rückgabe von [**ivssproviderkreatesnapshotset:: abortnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) oder [**ivssprovidernotification:: onentladen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidernotifications-onunload).

 

 




