---
description: Es kann erforderlich sein, dass ein Dienst vor beendet und nach einem Wiederherstellungsvorgang neu gestartet wird.
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: Beenden von Diensten für die Wiederherstellung durch Anforderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa8051fc20c5ba1bd930da8c7da5c40829c07772572c2b1fb795250d34b8c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511620"
---
# <a name="stopping-services-for-restore-by-requesters"></a>Beenden von Diensten für die Wiederherstellung durch Anforderer

Es kann erforderlich sein, dass ein Dienst vor beendet und nach einem Wiederherstellungsvorgang neu gestartet wird.

In der Regel wird das Beenden und Starten eines Diensts zur Unterstützung einer Wiederherstellung von einem Writer ausgeführt, wenn das [*PreRestore-Ereignis*](vssgloss-p.md) (mit [**CVssWriter::OnPreRestore)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)und das [*PostRestore-Ereignis*](vssgloss-p.md) (mit [**CVssWriter::OnPostRestore)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)behandelt werden.

Es kann jedoch Fälle geben, in denen es erforderlich ist, dass ein Anforderer einen ausgeführten Dienst explizit beendet. Writer geben an, ob dies der Fall ist, indem sie den VSS \_ RME \_ STOP RESTORE \_ \_ START- oder \_ VSS RME \_ RESTORE STOP \_ \_ START-Wert der [**VSS \_ RESTOREMETHOD \_ ENUM-Enumeration**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) als Wiederherstellungsmethodenargument eines Aufrufs der [**IVssCreateWriterMetadata::SetRestoreMethod-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) festlegen und den Namen des zu beendenden Diensts angeben.

Ein Anforderer ruft Informationen über die Wiederherstellungsmethode und den Namen des Diensts ab, der beendet werden soll, wenn er mit Writermetadaten arbeitet, indem er die [**IVssEx usernameWriterMetadata::GetRestoreMethod-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod) verwendet.

Es ist wichtig, dass der Writer beim Angeben des Namens eines diensts, der beendet werden soll, den richtigen öffentlich bekannten Namen dieses Diensts verwendet. Ein mehrdeutiger oder ungenauer Name kann dazu führen, dass anfordernde Personen den falschen Dienst beenden oder nicht ermitteln können, welcher Dienst beendet werden soll.

Nach Abschluss des Wiederherstellungsvorgangs müssen anforderer den Dienst neu starten.

Sie müssen beim Entwerfen und Implementieren von Writern, die Dienste unterstützen, die Anfordernde beenden und neu starten müssen, vorsichtig sein. Insbesondere sollten solche Writer nicht teil des Diensts sein, d. h., der Writer selbst sollte nicht beendet und dann im Verlauf des Wiederherstellungsvorgangs neu gestartet werden müssen.

Ein Writer, dessen Prozess beendet wird, hat nach dem Neustart eine andere Writerinstanz. Die neue Instanz des Writers empfängt keine VSS-Ereignisse, die für die ursprüngliche Instanz des Writers vorgesehen sind. Insbesondere wenn der Prozess einer Writer-Instanz nach der Behandlung eines PreRestore-Ereignisses beendet wird, empfängt die neue Instanz das PostRestore-Ereignis nicht. Darüber hinaus generiert VSS einen Fehler, der den Verlust eines am Wiederherstellungsvorgang beteiligten Writers angibt, und [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) kann einen Fehler zurückgeben.

 

 



