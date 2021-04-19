---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359841"
---
# <a name="a-volume-shadow-copy-service"></a>A (Volumeschattenkopie-Dienst)

a [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abbruch Ereignis**
</dt> <dd>

Ein vom Volumeschattenkopie-Dienst ausgestelltes VSS-Ereignis, das angibt, dass ein kompatibler Sicherungs-oder Wiederherstellungs Vorgang abgebrochen wurde. Der Ereignishandler ist **CVssWriter:: OnAbort**.

</dd> <dt>

<span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**
</dt> <dd>

Bei Active Directory Service (ADSI) handelt es sich um einen com-basierten Dienst, der einen Mechanismus zum Suchen, identifizieren und Zugreifen auf die Benutzer und Ressourcen bereitstellt, die in einem verteilten Computer Umgebungs System verfügbar sind. Insbesondere wird der Active Directory-Dienst zum Verwalten von Enterprise-Verzeichnisinformationen für die Verteilung durch einen Windows-Domänen Server verwendet.

</dd> <dt>

<span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**Zuordnung alternativer Speicherorte**
</dt> <dd>

Ein Pfad, der nicht der ursprüngliche Pfad einer Datei ist, in den die Datei unter bestimmten Bedingungen wieder hergestellt werden kann. In der Regel sind alternative Speicherort Zuordnungen nicht für eine einzelne klar definierte Datei definiert, sondern für ein Pfad-/dateispezifikations-paar und können rekursiv sein.

Eine Alternative Speicherort Zuordnung wird nur während eines Wiederherstellungs Vorgangs verwendet und sollte nicht mit einem alternativen Pfad verwechselt werden, der nur während eines Sicherungs Vorgangs verwendet wird. Siehe auch *Alternativer Pfad*.

</dd> <dt>

<span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**Alternativer Pfad**
</dt> <dd>

Bei Sicherungs Vorgängen weist ein Pfad-/dateispezifikations-Paar (das von einer Instanz der **ivsswmfiledesc** -Schnittstelle verarbeitet wird) einen alternativen Pfad auf, wenn der zugehörige Dateideskriptor (wie von **ivsswmfiledesc:: getalternateloation** zurückgegeben) nicht NULL ist. Der Pfad ist von diesem Pfad und nicht vom standardmäßigen angegebenen Pfad. diese Dateien müssen bei der Sicherung eines Volumes kopiert werden.

Ein alternativer Pfad wird nur während eines Sicherungs Vorgangs verwendet und sollte nicht mit einer alternativen Speicherort Zuordnung verwechselt werden. Eine Alternative Speicherort Zuordnung wird nur bei Wiederherstellungs Vorgängen verwendet. Siehe auch *Alternative Speicherort Zuordnung*.

</dd> <dt>

<span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**Anwendungsebene**
</dt> <dd>

Wird von VSS verwendet, um den Punkt im Verlauf der Erstellung einer Schatten Kopie anzugeben, die ein Writer über einen Einfrieren benachrichtigt wird. Weitere Informationen finden Sie unter [*Anwendungen auf Back-End-Ebene*](vssgloss-b.md), [*Einfrieren*](vssgloss-f.md), [*Front-End-Anwendungen*](vssgloss-f.md), [*Schatten Kopie*](vssgloss-s.md), [*Anwendungen auf Systemebene*](vssgloss-s.md), [*Writer*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**automatisch wiederhergestellte Schatten Kopie**
</dt> <dd>

Eine Schatten Kopie, bei der eine zusätzliche Verarbeitung durch einen Writer in einem vollständig konsistenten Zustand für Sicherungs-oder Data Mining Aktionen aufgetreten ist (z. b. ein Rollback aller Transaktionen, die noch nicht abgeschlossen wurden, während die Schatten Kopie erstellt wurde). Dies kann durch einen Writer initiiert werden, indem Sie ein entsprechendes Flag aus der **VSS- \_ \_ Komponentenflags** -Enumeration im **dwcomponentflags** -Member der **VSS \_ ComponentInfo** -Struktur oder durch einen Anforderer angeben, indem Sie dem Kontext für die Schatten Kopie das **VSS- \_ Volsnap \_ attr- \_ Rollback- \_ Wiederherstellungsflag** hinzufügen. Die automatische Wiederherstellung ermöglicht die Verwendung der schattenkopierten Daten auf einem schreibgeschützten Volume, für Data Mining, für Teil Wiederherstellungen (z. b. ausgewählte Elemente in einer Datenbank) oder für andere Zwecke.

Siehe auch [*austauschen Shadow Copy*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**Schatten Kopie automatisch freigeben**
</dt> <dd>

Eine Schatten Kopie, die bei Beendigung eines Sicherungs Vorgangs gelöscht wird. Programm gesteuert bedeutet dies, dass die Schatten Kopie gelöscht wird, wenn die **IVssBackupComponents** -Schnittstelle freigegeben wird. Eine automatische releaseschattenkopie kann nicht persistent sein.

Standardmäßig werden alle Schatten Kopien automatisch veröffentlicht. Siehe auch [*persistente Schatten Kopie*](vssgloss-p.md), [*austauschen-Schatten Kopie*](vssgloss-t.md).

</dd> </dl>

 

 



