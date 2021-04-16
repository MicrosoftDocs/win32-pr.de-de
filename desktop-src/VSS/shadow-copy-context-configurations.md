---
description: Requesters steuern die Features einer Schatten Kopie durch Festlegen Ihres Kontexts. Dieser Kontext gibt an, ob die Schatten Kopie den aktuellen Vorgang und den Grad der Koordination von Writer und Anbietern überstehen wird.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Kontext Konfigurationen für Schatten Kopien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528697"
---
# <a name="shadow-copy-context-configurations"></a>Kontext Konfigurationen für Schatten Kopien

Requesters steuern die Features einer Schatten Kopie durch Festlegen Ihres Kontexts. Dieser Kontext gibt an, ob die Schatten Kopie den aktuellen Vorgang und den Grad der Koordination von Writer und Anbietern überstehen wird.

## <a name="persistence-and-shadow-copy-context"></a>Persistenz und Schatten Kopier Kontext

Eine Schatten Kopie ist möglicherweise [*persistent*](vssgloss-p.md)– das heißt, die Schatten Kopie wird nach der Beendigung eines Sicherungs Vorgangs oder der Freigabe eines [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Objekts nicht gelöscht.

Persistente Schatten Kopien erfordern [**\_ VSS- \_ Momentaufnahme \_ Kontext**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) Kontexte des **VSS \_ ctx- \_ Clients \_**, auf die zugegriffen werden kann, **VSS \_ ctx- \_ App- \_ Rollback** oder **VSS \_ ctx \_ NAS- \_ Rollback**. Persistente Schatten Kopien können nur für NTFS-Volumes erstellt werden.

Nicht persistente Schatten Kopien werden mit Kontexten der **VSS \_ ctx- \_ Sicherung** oder der **VSS \_ ctx- \_ Datei \_ Freigabe \_ Sicherung** erstellt. Nicht persistente Schatten Kopien können für NTFS-und nicht-NTFS-Volumes erstellt werden.

## <a name="writer-participation-and-shadow-copies"></a>Writer-Teilnahme und Schatten Kopien

Ein schattenkopieskontext kann als Einbeziehung von Writern oder nicht zum Einschließen von Writern klassifiziert werden.

Schattenkopiekontexte, die Writer in ihrer Erstellung einbeziehen, umfassen Folgendes:

-   **VSS- \_ ctx- \_ App- \_ Rollback**
-   **VSS \_ ctx- \_ Sicherung**
-   **VSS \_ ctx- \_ Client \_ barrierefreie \_ Writer**

Zu den Entwicklern, die in ihrer Erstellung keine Writer einschließen, gehören:

-   **verfügbarer VSS- \_ ctx- \_ Client \_**
-   **VSS \_ ctx- \_ Datei \_ Freigabe \_ Sicherung**
-   **VSS- \_ ctx- \_ NAS- \_ Rollback**

Ein Kontext kann mit beiden Arten von Schatten Kopien verwendet werden, kann jedoch nicht zum Erstellen einer Schatten Kopie verwendet werden:

-   **VSS \_ ctx \_ alle**

Das Erstellen einer Schatten Kopie mit einem Kontext von **VSS \_ ctx \_ all** (mithilfe von [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) und [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) wird nicht unterstützt.

Bei Vorgängen, die einen Kontext von **VSS \_ ctx \_** unterstützen, handelt es sich dabei um administrative Vorgänge [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents:: breaksnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)und [**IVssBackupComponents:: exposesnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).

## <a name="obtaining-shadow-copy-information"></a>Abrufen von Schattenkopieinformationen

Wenn ein Anforderer die identifizierende GUID einer Schatten Kopie (seine **VSS- \_ ID**) kennt, kann er Informationen über den Kontext einer bestimmten Schatten Kopie (identifiziert durch seine **VSS- \_ ID**) abrufen, indem die von einem Aufrufen von [**IVssBackupComponents:: gebrannapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)zurückgegebene VSS-momentaufnahmenstruktur entpackt wird. [**\_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)

Zum Abrufen von Kontextinformationen über alle Schatten Kopien eines Systems ein Anforderer untersucht **das m \_ lsnapshotattributes** -Element des **obj. Snap** -Members der [**VSS- \_ Objekt \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (bei der es sich um eine [**VSS-momentaufnahmenstruktur \_ handelt \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ), die mithilfe von [**ivssenuwbject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) abgerufen wurde, um die Liste der Objekte zu durchlaufen, die durch einen-Befehl von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)

 

 



