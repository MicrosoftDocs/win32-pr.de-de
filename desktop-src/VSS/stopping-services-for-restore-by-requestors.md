---
description: Möglicherweise ist es erforderlich, dass ein Dienst vor und nach einem Wiederherstellungs Vorgang beendet und neu gestartet wird.
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: Beenden von Diensten für die Wiederherstellung durch Anforderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548af25a4b4550d35a8e6fa4d4c0e791897b6e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356702"
---
# <a name="stopping-services-for-restore-by-requesters"></a>Beenden von Diensten für die Wiederherstellung durch Anforderer

Möglicherweise ist es erforderlich, dass ein Dienst vor und nach einem Wiederherstellungs Vorgang beendet und neu gestartet wird.

In der Regel wird das Beenden und Starten eines Diensts zur Unterstützung einer Wiederherstellung von einem Writer durchgeführt, wenn das [*PreRestore*](vssgloss-p.md) -Ereignis (mit [**CVssWriter:: onprerestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) und das [*postrestore*](vssgloss-p.md) -Ereignis (mit [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)) verarbeitet werden.

Es kann jedoch vorkommen, dass es erforderlich ist, dass ein Anforderer einen laufenden Dienst explizit beendet. Writer geben an, ob dies der Fall ist, indem der Start Wert der VSS- \_ RME- \_ \_ Wiederherstellung beenden \_ bzw. der VSS- \_ RME- \_ Wiederherstellungs Beendigungs \_ \_ Start der [**VSS \_ restoremethod \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) -Enumeration als Restore Method-Argument eines Aufrufens der [**ivsskreatewritermetadata::**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) Abort-Methode festgelegt wird.

Ein Anforderer Ruft Informationen über die Wiederherstellungsmethode und den Namen des Diensts ab, der bei der Arbeit mit Writer-Metadaten mit der [**ivssexamineschreitermetadata:: getrestoremethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod) -Methode beendet werden soll.

Es ist wichtig, dass der Writer beim Angeben des Namens eines zu beendenden Diensts den richtigen öffentlich bekannten Namen dieses Diensts verwendet. Ein mehrdeutiger oder ungenauer Name kann dazu führen, dass die anfordernde Person den falschen Dienst beenden oder nicht ermitteln kann, welcher Dienst beendet werden soll.

Nach Abschluss des Wiederherstellungs Vorgangs müssen anfordernde Personen den Dienst neu starten.

Sie müssen beim Entwerfen und Implementieren von Writern, die Dienste unterstützen, die Anforderer beendet und neu starten müssen, vorsichtig sein. Diese Writer sollten insbesondere nicht Teil des Diensts sein – d. h., der Writer selbst sollte nicht angehalten und dann im Verlauf des Wiederherstellungs Vorgangs neu gestartet werden.

Ein Writer, dessen Prozess beendet wird, hat beim Neustart eine andere Writer-Instanz. Die neue Instanz des Writers empfängt keine VSS-Ereignisse, die für die ursprüngliche Instanz des Writers vorgesehen sind. Insbesondere, wenn der Prozess einer Writer-Instanz beendet wird, nachdem ein vorab Ereignis verarbeitet wurde, empfängt die neue Instanz das postrestore-Ereignis nicht. Außerdem generiert VSS einen Fehler, der den Verlust eines Beteiligten Writers im Wiederherstellungs Vorgang anzeigt, und [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) möglicherweise einen Fehler zurück.

 

 



