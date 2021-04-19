---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345068"
---
# <a name="s-volume-shadow-copy-service"></a>S (Volumeschattenkopie-Dienst)

[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selekabilität für Sicherung**
</dt> <dd>

Eine Komponente kann für die Sicherung ausgewählt werden, wenn die explizite Einbindung in einen Sicherungs Vorgang optional ist. Die selectlichkeit der Sicherung ist aktiviert, wenn der Wert des **bwählbaren** Members der [**VSS \_ ComponentInfo**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) -Struktur **true** ist. Es ist kein Standardwert für die selekabilität einer Komponente für die Sicherung vorhanden. ein Writer muss diesen Wert immer explizit festlegen.

Writer verwenden auch selectlichkeit für die Wiederherstellung, um die Beteiligung der Komponente an Wiederherstellungs Vorgängen zu organisieren.

Weitere Informationen finden Sie unter *auswählbare Komponente*, *Auswahlmöglichkeit für die Wiederherstellung*, [*explizite Komponenten Einbindung*](vssgloss-e.md), [*implizite Komponenten Einbindung*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selekabilität für die Wiederherstellung**
</dt> <dd>

Eine Komponente kann für die Wiederherstellung ausgewählt werden, wenn Sie implizit als Teil eines Komponenten Satzes gesichert werden kann, und später einzeln ohne den Rest des Komponenten Satzes wieder hergestellt werden kann. Die Auswahlfunktion für die Wiederherstellung ist aktiviert, wenn der Wert des **bselectableforrestore** -Members der [**VSS \_ ComponentInfo**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) -Struktur " **true**" ist. Standardmäßig ist die Wählbarkeit einer Komponente für Restore auf **false**. Die Auswahl für die Wiederherstellung ist nur dann von Bedeutung, wenn eine Komponente nicht zum Sicherungs Dokument hinzugefügt wurde.

Weitere Informationen finden Sie unter *auswählbare Komponente*, *Auswahlmöglichkeit für Sicherungen*, [*explizite Komponenten Einbindung*](vssgloss-e.md), [*impliziter Komponenten Einbindung*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**auswählbare Komponente**
</dt> <dd>

Eine Komponente wird als auswählbar bezeichnet, wenn die explizite Einbindung in einen Sicherungs-oder Wiederherstellungs Vorgang optional ist.

Die Auswahl der für die Wiederherstellung von Sicherungs-und Auswahl Optionen ist unabhängig voneinander – eine Komponente kann für beide Vorgänge, für die Wiederherstellung, nicht für Sicherungen oder für Sicherungen und nicht für die Wiederherstellung auswählbar sein.

Writer verwenden auch selectlichkeit, um Ihre Komponenten in Gruppen zu organisieren:

-   Nicht auswählbare Komponenten ohne auswählbare Vorgänger in ihren logischen Pfaden müssen immer explizit eingeschlossen werden, wenn ein Writer gesichert oder wieder hergestellt werden soll.
-   Nicht auswählbare Komponenten mit auswählbaren Vorgängern werden nur in eine Sicherung oder Wiederherstellung eingeschlossen, wenn mindestens ein auswählbarer Vorgänger eingeschlossen ist.
-   Auswählbare Komponenten ohne auswählbare Vorgänger können nur explizit in einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden.
-   Auswählbare Komponenten mit auswählbaren Vorgängern können explizit in einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden, oder Sie können implizit eingeschlossen werden, wenn einer ihrer auswählbaren Vorgänger eingeschlossen ist.

Weitere Informationen finden Sie unter [*Komponenten*](vssgloss-c.md), *selectlichkeit für Sicherung*, *selektbarkeit für die Wiederherstellung*, [*explizite Komponenten Einbindung*](vssgloss-e.md), [*implizite Komponenten Einbindung*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**Schatten Kopie**
</dt> <dd>

Ein Schreib geschütztes Zeit Punkt Replikat des Inhalts eines ursprünglichen Volumes. Jede Schatten Kopie wird mit einer permanenten GUID verschlüsselt. Wird auch als Volumeschattenkopie bezeichnet. Siehe auch *Schattenkopiesatz*.

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Schattenkopien für freigegebene Ordner**
</dt> <dd>

Ein Windows-Feature, das mithilfe von VSS Lightweight-, Online-Sicherungskopien von Volumes erstellt. Clients können über die Windows-Shell auf diese Sicherungen zugreifen, um alte Versionen von Dateien anzuzeigen und Fehler rückgängig zu machen, ohne eine vollständige Wiederherstellung zu erfordern Siehe auch zum [*Client zugänglichen Schatten Kopie*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**Schattenkopiesatz**
</dt> <dd>

Eine Auflistung von Volumeschattenkopien, die gleichzeitig erstellt und durch eine gemeinsame Schattenkopiesatz-ID (einen persistenten GUID-Wert) identifiziert werden. Dies ist der Mechanismus, der verwendet wird, um die Verwaltung eines schattenkopiervorgangs auf mehreren Volumes zuzulassen. Siehe auch *Schatten Kopie*.

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**Softwareanbieter**
</dt> <dd>

Ein Anbieter, der e/a-Anforderungen auf Software Ebene zwischen dem Dateisystem und dem Volumemanager abfängt. Siehe auch [*Hardware Anbieter*](vssgloss-h.md), [*Anbieter*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**Unterkomponente**
</dt> <dd>

Jede Komponente, die über einen logischen Pfad verfügt, der eine auswählbare (für die Sicherung oder Wiederherstellung) übergeordnete Komponente enthält. Unter Komponenten müssen einen logischen Pfad in der Form {Component \_ Name} \\ {subcomponent \_ Name} aufweisen. Wenn eine der auswählbaren (für Sicherungs-oder Wiederherstellungs Vorgänger) Komponenten explizit in eine Sicherung oder Wiederherstellung eingeschlossen ist, wird die Unterkomponente implizit in den Vorgang eingeschlossen. Implizit enthaltene unter Komponenten enthalten keine Daten im Sicherungs Komponenten Dokument – unabhängig davon, ob Sie ausgewählt werden können (entweder bei der Wiederherstellung oder bei der Sicherung). Siehe auch [*Komponente*](vssgloss-c.md), [*logischer Pfad*](vssgloss-l.md).

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**schattenkopieschattenkopie**
</dt> <dd>

Ein schattenkopiertes Volume, das für den Mount Manager-Namespace eines Systems sichtbar ist – dies bedeutet, dass **findfirstvolume** und **findnextvolume** es finden können und dass Volumen-und Abbruch Benachrichtigungen generiert werden. Alle verfügbar gemachten Schatten Kopien sind auch Schatten Kopien. Allerdings muss eine aufgeschietete Schatten Kopie nicht verfügbar gemacht werden. Wenn eine Schatten Kopie transportierbar ist, kann Sie nicht angezeigt werden. Siehe auch verfügbar gemachte [*Schatten Kopie*](vssgloss-e.md), [*austauschen-Schatten Kopie*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**System Datei Schutz**
</dt> <dd>

Siehe [*Windows-Datei Schutz*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**Anwendungen auf Systemebene**
</dt> <dd>

Gibt den Punkt an, an dem VSS einen Writer über eine Sperrung benachrichtigt. Writer, die als Anwendungen auf Systemebene initialisiert werden, werden nach dem Initialisieren von Writern als Anwendungen auf Front-End-Ebene oder als Anwendungen auf Back-End-Ebene benachrichtigt. Weitere Informationen finden Sie auch auf [*Anwendungsebene*](vssgloss-a.md), [*Back-End-Anwendungen*](vssgloss-b.md), Anwendungen auf [*Front-End-Ebene*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**Systemanbieter**
</dt> <dd>

Der vorinstallierte Standardanbieter, der als Teil von Windows bereitgestellt wird.

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Ordner "System Volume"**
</dt> <dd>

Ein frei gegebenes Verzeichnis, in dem die freigegebenen Kopien der öffentlichen Dateien einer Domäne gespeichert werden, d. –. die Dateien, die von allen Domänen Controllern in der Domäne repliziert werden.

</dd> </dl>

 

 



