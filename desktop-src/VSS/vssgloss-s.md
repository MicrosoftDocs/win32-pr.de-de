---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92843e9277709a1138bc51b403089c932387e1b282e349c7907fc4cde88e9de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124480"
---
# <a name="s-volume-shadow-copy-service"></a>S (Volumeschattenkopie-Dienst)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-f.md) [](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S T [U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**Auswählbarkeit für die Sicherung**
</dt> <dd>

Eine Komponente kann für die Sicherung ausgewählt werden, wenn die explizite Einbeziehung in einen Sicherungsvorgang optional ist. Die Auswählbarkeit für die Sicherung ist aktiviert, wenn der Wert des **bSelectable-Members** der [**VSS \_ COMPONENTINFO-Struktur**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) **true ist.** Es gibt keinen Standardwert für die Auswahl einer Komponente für die Sicherung. Ein Writer muss diesen Wert immer explizit festlegen.

Writer verwenden auch die Auswahlbarkeit für die Wiederherstellung, um die Teilnahme ihrer Komponente an Wiederherstellungsvorgängen zu organisieren.

Siehe auch *auswählbare Komponente,* *Auswählbarkeit für wiederherzustellen,* [*explizite Komponenteneinschluss,*](vssgloss-e.md) [*implizite Komponenteneinschluss.*](vssgloss-i.md)

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**Auswählbarkeit für die Wiederherstellung**
</dt> <dd>

Eine Komponente kann für die Wiederherstellung ausgewählt werden, wenn sie implizit als Teil eines Komponentensets sichern und später einzeln wiederhergestellt werden kann, ohne dass der Rest der Komponente festgelegt ist. Die Auswählbarkeit für die Wiederherstellung ist aktiviert, wenn der Wert des **bSelectableForRestore-Members** der [**VSS \_ COMPONENTINFO-Struktur**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) **true ist.** Standardmäßig ist die Auswählbarkeit einer Komponente für die Wiederherstellung **false.** Die Wählbarkeit für die Wiederherstellung hat nur dann eine Bedeutung, wenn dem Sicherungsdokument keine Komponente hinzugefügt wurde.

Siehe auch *auswählbare Komponente,* *Auswählbarkeit für Sicherung,* [*explizite Komponenteneinschluss,*](vssgloss-e.md) [*implizite Komponenteneinschluss*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**Auswählbare Komponente**
</dt> <dd>

Eine Komponente wird als auswählbar bezeichnet, wenn ihre explizite Einbeziehung in einen Sicherungs- oder Wiederherstellungsvorgang optional ist.

Die Auswahlbarkeit der Sicherung und die Auswählbarkeit für die Wiederherstellung sind voneinander unabhängig. Eine Komponente kann für beide Vorgänge, für die Wiederherstellung und nicht für die Sicherung oder für die Sicherung und nicht für die Wiederherstellung ausgewählt werden.

Writer verwenden auch die Auswählbarkeit, um ihre Komponenten in Gruppen zu organisieren:

-   Nicht auswählbare Komponenten ohne auswählbare Vorgänger in ihren logischen Pfaden müssen immer explizit eingeschlossen werden, wenn ein Writer sichern oder wiederhergestellt werden soll.
-   Nicht auswählbare Komponenten mit auswählbaren Vorgängern werden nur dann in eine Sicherung oder Wiederherstellung einbezogen, wenn mindestens ein auswählbarer Vorgänger enthalten ist.
-   Auswählbare Komponenten ohne auswählbare Vorgänger können nur explizit in einen Sicherungs- oder Wiederherstellungsvorgang eingeschlossen werden.
-   Auswählbare Komponenten mit auswählbaren Vorgängern können explizit in einen Sicherungs- oder Wiederherstellungsvorgang eingeschlossen oder implizit eingeschlossen werden, wenn einer ihrer auswählbaren Vorgänger enthalten ist.

Weitere Informationen finden [*Sie unter Komponenten,*](vssgloss-c.md) *Auswählbarkeit für Sicherung,* *Auswählbarkeit für* die Wiederherstellung, [*expliziter Komponenteneinschluss,*](vssgloss-e.md) [*impliziter Komponenteneinschluss*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**Schattenkopie**
</dt> <dd>

Ein schreibgeschütztes Point-in-Time-Replikat des Inhalts eines ursprünglichen Volumes. Jede Schattenkopie wird durch eine persistente GUID schlüsselt. Wird auch als Volumeschattenkopie bezeichnet. Siehe auch *Schattenkopiesatz*.

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Schattenkopien für freigegebene Ordner**
</dt> <dd>

Ein Feature von Windows, das einfache Onlinesicherungskopien von Volumes mit VSS erstellt. Clients können über die Windows Shell auf diese Sicherungen zugreifen, um alte Versionen von Dateien zu sehen und Fehler rückgängig zu machen, ohne dass eine vollständige Wiederherstellung erforderlich ist. Weitere Informationen finden Sie [*auch unter Clientzugriff auf Schattenkopien.*](vssgloss-c.md)

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**Schattenkopiesatz**
</dt> <dd>

Eine Auflistung von Volumeschattenkopien, die gleichzeitig erstellt und durch einen gemeinsamen Wert für die Schattenkopieset-ID (eine persistente GUID) identifiziert werden. Dies ist der Mechanismus, mit dem ein Schattenkopievorgang volumesübergreifend verwaltet werden kann. Siehe auch *Schattenkopie*.

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**Softwareanbieter**
</dt> <dd>

Ein Anbieter, der E/A-Anforderungen auf Softwareebene zwischen dem Dateisystem und dem Volume-Manager abfingt. Siehe auch [*Hardwareanbieter*](vssgloss-h.md), [*Anbieter*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**Unterkomponente**
</dt> <dd>

Jede Komponente, die über einen logischen Pfad mit einer auswählbaren übergeordneten Komponente (für Sicherung oder Wiederherstellung) verfügt. Unterkomponenten müssen über einen logischen Pfad im Formular {Komponentenname} \_ \\ {Unterkomponentenname} \_ verfügen. Wenn der auswählbare Vorgänger einer Unterkomponenten (für Sicherung oder Wiederherstellung) explizit in eine Sicherung oder Wiederherstellung eingeschlossen wird, wird die Unterkomponenten implizit in den Vorgang eingeschlossen. Implizit eingeschlossene Unterkomponenten enthalten ihre Daten nicht im Sicherungskomponentendokument – unabhängig davon, ob sie ausgewählt werden können (für die Wiederherstellung oder Sicherung). Siehe auch [*Komponente*](vssgloss-c.md), [*logischer Pfad*](vssgloss-l.md).

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**Surfaced Shadow Copy**
</dt> <dd>

Ein schattenkopiertes Volume, das für den Mount Manager-Namespace eines Systems sichtbar ist. Dies bedeutet, dass **FindFirstVolume** und **FindNextVolume** es finden können und dass Benachrichtigungen zum Ein- und Abflug des Volumes generiert werden. Alle verfügbar gemachten Schattenkopien sind ebenfalls als Schattenkopien verfügbar gemacht. Allerdings muss eine oberflächesierte Schattenkopie nicht verfügbar gemacht werden. Wenn eine Schattenkopie transportierbar ist, kann sie nicht auftdeckt werden. Siehe auch [*verfügbar gemachte Schattenkopie*](vssgloss-e.md), [*transportierbare Schattenkopie*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Systemdateischutz**
</dt> <dd>

Siehe [*Windows Dateischutz.*](vssgloss-w.md)

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**Anwendungen auf Systemebene**
</dt> <dd>

Gibt den Punkt an, an dem VSS einen Writer über ein Einfrieren benachrichtigt. Writer, die als Anwendungen auf Systemebene initialisiert werden, werden benachrichtigt, nachdem Writer entweder als Anwendungen auf Front-End-Ebene oder als Back-End-Anwendungen initialisiert wurden. Siehe auch [*Anwendungen auf Anwendungsebene,*](vssgloss-a.md) [*Back-End-Anwendungen*](vssgloss-b.md)und [*Front-End-Anwendungen.*](vssgloss-f.md)

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**Systemanbieter**
</dt> <dd>

Der standardmäßig vorinstallierte Anbieter, der als Teil des Windows.

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**System Volume Folder**
</dt> <dd>

Ein freigegebenes Verzeichnis, in dem die freigegebenen Kopien der öffentlichen Dateien einer Domäne gespeichert werden, d. b. die Dateien, die auf allen Domänencontrollern in der Domäne repliziert werden.

</dd> </dl>

 

 



