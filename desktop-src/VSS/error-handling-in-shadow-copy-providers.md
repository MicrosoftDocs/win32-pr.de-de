---
description: VSS lässt zu, dass viele Schattenkopien gleichzeitig vorhanden sind, aber es kann nur eine Erstellung eines Schattenkopiesets zwischen dem Aufruf von IVssBackupComponents::StartSnapshotSet und der Rückgabe aus dem Aufruf von IVssBackupComponents::D oSnapshotSet in Bearbeitung sein.
ms.assetid: 26657fc2-180f-4ebb-820c-2159e7fe7584
title: Fehlerbehandlung bei Schattenkopieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0963df4c9c81c2cd9f96e7c1828243f3910a1df34d5ef94a714f17c57b404b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032680"
---
# <a name="error-handling-in-shadow-copy-providers"></a>Fehlerbehandlung bei Schattenkopieanbietern

VSS lässt zu, dass viele Schattenkopien gleichzeitig vorhanden sind. Es wird jedoch nur die Erstellung eines Schattenkopiesets zwischen dem Aufruf von [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) und der Rückgabe aus dem Aufruf von [**IVssBackupComponents::D oSnapshotSet ermöglicht.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)

## <a name="no-partial-commit"></a>Kein teilieller Commit

Wenn bei einem Anbieter ein Fehler bei einer Schattenkopie auf einem Volume oder einer LUN im Schattenkopiesatz auftritt, schlägt die Erstellung des gesamten Schattenkopiesets fehl. Dies ist beabsichtigt. Dieser Entwurf vereinfacht die Verhaltensprobleme im Zusammenhang mit der semantischen Teilfehleranalyse und behält einen konsistenten Zeitpunkt für alle Schattenkopien im Satz bei.

## <a name="reporting-fault-conditions"></a>Melden von Fehlerbedingungen

Wenn ein Anbieterfehler oder eine Fehlerbedingung auftritt, muss der Anbieter einen Fehler im Anwendungsereignisprotokoll protokollieren. Dies schließt anbieterspezifische Fehler beim Erstellen oder Importieren eines Schattenkopiesets oder Ressourcenzuordnungsfehler für Schattenkopien beim Kopieren beim Schreiben nach der Erstellung ein, ist aber nicht darauf beschränkt. Diese Protokollierung darf nicht während der Zeit stattfinden, in der sich die Volumes im Schattenkopiesatz in einem fixierten Zustand befinden.

## <a name="valid-provider-return-values"></a>Gültige Anbieter-Rückgabewerte

In der folgenden Tabelle sind die gültigen Rückgabecodes für Anbietermethoden und deren Bedeutung aufgeführt.



| Wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span>S \_ OK<br/>                                                                                                                     | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                  |
| <span id="E_OUTOFMEMORY"></span><span id="e_outofmemory"></span>E \_ OUTOFMEMORY<br/>                                                                                          | Der Anbieter hat nicht genügend Arbeitsspeicher oder andere Systemressourcen.<br/>                                                                                                                                                                                    |
| <span id="E_INVALIDARG"></span><span id="e_invalidarg"></span>E \_ INVALIDARG<br/>                                                                                             | Einer der Parameterwerte ist ungültig.<br/>                                                                                                                                                                                                   |
| <span id="E_ACCESSDENIED"></span><span id="e_accessdenied"></span>E \_ ACCESSDENIED<br/>                                                                                       | Ein nicht privilegierter Client hat versucht, den Anbieter auf abruft.<br/>                                                                                                                                                                                |
| <span id="VSS_E_BAD_STATE"></span><span id="vss_e_bad_state"></span>VSS \_ E \_ BAD \_ STATE<br/>                                                                                  | Entweder unterstützt kein Anbieter den angeforderten Vorgang, oder der Vorgang kann nicht für das Objekt ausgeführt werden, da sich das Objekt nicht im richtigen Zustand befindet.<br/>                                                                                     |
| <span id="VSS_E_OBJECT_NOT_FOUND"></span><span id="vss_e_object_not_found"></span>VSS \_ \_ E-OBJEKT \_ NICHT \_ GEFUNDEN<br/>                                                            | Ein Parameter bezieht sich auf ein Objekt, das nicht gefunden wurde (z. B. schattenkopie-ID, Schattenkopieset-ID oder Volume).<br/>                                                                                                                               |
| <span id="VSS_E_INSUFFICIENT_STORAGE"></span><span id="vss_e_insufficient_storage"></span>VSS \_ E – NICHT GENÜGEND \_ \_ SPEICHER<br/>                                                 | Der Anbieter kann den Vorgang nicht ausführen, da nicht genügend Speicherplatz vorhanden ist.<br/>                                                                                                                                                           |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED"></span><span id="vss_e_volume_not_supported"></span>VSS \_ \_ E-VOLUME \_ WIRD NICHT \_ UNTERSTÜTZT<br/>                                                | Kein Anbieter auf diesem Computer unterstützt den angeforderten Vorgang auf dem Volume.<br/>                                                                                                                                                                |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER"></span><span id="vss_e_volume_not_supported_by_provider"></span>VSS \_ \_ E-VOLUME \_ WIRD VOM ANBIETER NICHT \_ \_ \_ UNTERSTÜTZT<br/>          | Der Anbieter unterstützt das Volume nicht.<br/>                                                                                                                                                                                                   |
| <span id="VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED"></span><span id="vss_e_maximum_number_of_snapshots_reached"></span>VSS \_ E MAXIMALE ANZAHL VON \_ \_ \_ \_ MOMENTAUFNAHMEN \_ ERREICHT<br/> | Der Anbieter hat die maximale Anzahl von Schattenkopien erreicht, die er unterstützen kann.<br/>                                                                                                                                                           |
| <span id="VSS_E_PROVIDER_VETO"></span><span id="vss_e_provider_veto"></span>VSS \_ E \_ PROVIDER \_ PROVIDERS<br/>                                                                      | Der Anbieter hat einen internen Laufzeitfehler festgestellt, der nicht einem anderen Rückgabewert zugeführt wird. Der Anbieter muss auch ein Ereignis in das Anwendungsereignisprotokoll schreiben, um dem Benutzer Informationen zum Beheben dieses Problems zu geben.<br/> |
| <span id="VSS_E_CANNOT_REVERT_DISKID"></span><span id="vss_e_cannot_revert_diskid"></span>VSS \_ E \_ KANN \_ DISKID NICHT \_ RÜCKGÄNGIG MACHEN<br/>                                                | Die MBR-Signatur oder GPT-ID für einen oder mehrere Datenträger konnte nicht auf den angeforderten Wert festgelegt werden. Weitere Informationen finden Sie im Anwendungsereignisprotokoll.<br/>                                                                                            |



 

Der Anbieter sollte nicht versuchen, andere Fehlercodes zurück zu geben.

Wenn der Anbieter einen nicht erwarteten Fehlercode zurückgibt (z. B. **S \_ FALSE,** **E \_ FAIL,** **E \_ UNEXPECTED** oder **E \_ ABORT),** schreibt VSS ein Ereignis in das Ereignisprotokoll, in dem der Anbieter und die fehlerhafte Methode erwähnt werden, und übersetzt den Fehler in **VSS E UNEXPECTED PROVIDER \_ \_ \_ \_ ERROR,** bevor er an den Anfordernden zurückgegeben wird. Dies erfolgt nicht für Rückgaben von [**IVssProviderCreateSnapshotSet::AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) oder [**IVssProviderNotifications::OnUnload**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidernotifications-onunload).

 

 




