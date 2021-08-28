---
title: verteiltes Dateisystem Functions
description: Im Folgenden finden Sie die verteiltes Dateisystem (DFS)-Funktionen.
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3fd41879293f376dfdb3d769d5152b2e747fc6e387f8f9538854d4d3e06e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096720"
---
# <a name="distributed-file-system-functions"></a>verteiltes Dateisystem Functions

Im Folgenden finden Sie die verteiltes Dateisystem (DFS)-Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[NetDfsAdd](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
Erstellt einen neuen verteiltes Dateisystem (DFS) oder fügt einem vorhandenen Link in einem DFS-Namespace Ziele hinzu.

</dd> <dt>

[NetDfsAddFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
Erstellt einen neuen domänenbasierten verteiltes Dateisystem (DFS)-Namespace. Wenn der Namespace bereits vorhanden ist, fügt die Funktion das angegebene Stammziel hinzu.

</dd> <dt>

[NetDfsAddRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
Erstellt einen domänenbasierten oder eigenständigen DFS-Namespace oder fügt einem vorhandenen domänenbasierten Namespace ein neues Stammziel hinzu.

</dd> <dt>

[NetDfsAddStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
Erstellt einen neuen eigenständigen verteiltes Dateisystem (DFS)-Namespace.

</dd> <dt>

[NetDfsEnum](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
Enumeriert die verteiltes Dateisystem(DFS)-Namespaces, die auf einem Server gehostet werden, oder DFS-Links eines namespace, der von einem Server gehostet wird.

</dd> <dt>

[NetDfsGetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
Ruft Informationen zu einem verteiltes Dateisystem(DFS)-Stamm oder -Link aus dem Cache ab, der vom DFS-Client verwaltet wird.

</dd> <dt>

[NetDfsGetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
Ruft die Sicherheitsbeschreibung des Containerobjekts für die domänenbasierten DFS-Namespaces in der angegebenen Active Directory-Domäne ab.

</dd> <dt>

[NetDfsGetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
Ruft Informationen zu einem angegebenen VERTEILTES DATEISYSTEM (DFS)-Stamm oder -Link in einem DFS-Namespace ab.

</dd> <dt>

[NetDfsGetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
Ruft die Sicherheitsbeschreibung für das Stammobjekt des angegebenen DFS-Namespace ab.

</dd> <dt>

[NetDfsGetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
Ruft die Sicherheitsbeschreibung für das Containerobjekt des angegebenen eigenständigen DFS-Namespace ab.

</dd> <dt>

[NetDfsGetSupportedNamespaceVersion](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
Bestimmt die unterstützte Metadatenversionsnummer.

</dd> <dt>

[NetDfsMove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
Benennt einen DFS-Link um oder verschiebt diesen.

</dd> <dt>

[NetDfsRemove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
Entfernt einen verteiltes Dateisystem (DFS) oder ein bestimmtes Linkziel eines DFS-Links in einem DFS-Namespace. Beim Entfernen eines bestimmten Linkziels wird der Link selbst entfernt, wenn das letzte Linkziel des Links entfernt wird.

</dd> <dt>

[NetDfsRemoveFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
Entfernt das angegebene Stammziel aus einem domänenbasierten verteiltes Dateisystem -Namespace (DFS). Wenn das letzte Stammziel des DFS-Namespace entfernt wird, löscht die Funktion auch den DFS-Namespace. Ein DFS-Namespace kann gelöscht werden, ohne zuerst alle links in ihm zu löschen.

</dd> <dt>

[NetDfsRemoveFtRootForced](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
Entfernt das angegebene Stammziel aus einem domänenbasierten verteiltes Dateisystem(DFS)-Namespace, auch wenn der Stammzielserver offline ist. Wenn das letzte Stammziel des DFS-Namespace entfernt wird, löscht die Funktion auch den DFS-Namespace. Ein DFS-Namespace kann gelöscht werden, ohne zuerst alle links in ihm zu löschen.

> [!Note]
> Die [**NetDfsRemoveFtRootForced-Funktion**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) aktualisiert die Registrierung auf dem DFS-Stammzielserver nicht. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

[NetDfsRemoveRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
Entfernt ein DFS-Stammziel aus einem domänenbasierten DFS-Namespace. Wenn das Stammziel das letzte Stammziel im DFS-Namespace ist, entfernt diese Funktion den DFS-Namespace. Diese Funktion kann auch verwendet werden, um einen eigenständigen DFS-Namespace zu entfernen.

</dd> <dt>

[NetDfsRemoveStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
Löscht einen eigenständigen verteiltes Dateisystem (DFS)-Namespace.

</dd> <dt>

[NetDfsSetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
Ändert Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder -Link im Cache, der vom DFS-Client verwaltet wird.

</dd> <dt>

[NetDfsSetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
Legt die Sicherheitsbeschreibung des Containerobjekts für die domänenbasierten DFS-Namespaces in der angegebenen Active Directory-Domäne fest.

</dd> <dt>

[NetDfsSetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
Legt Informationen zu einem bestimmten Stamm-, Verteiltes Dateisystem-, Link- oder Linkziel (DFS) fest oder ändert diese.

</dd> <dt>

[NetDfsSetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
Legt die Sicherheitsbeschreibung für das Stammobjekt des angegebenen DFS-Namespace fest.

</dd> <dt>

[NetDfsSetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
Legt die Sicherheitsbeschreibung für das Containerobjekt des angegebenen eigenständigen DFS-Namespace fest.

</dd> </dl>

Beachten Sie, dass eine Anwendung, die eine der Funktionen aufruft, indirekt dazu führen kann, dass der lokale DFS-Namespaceserver, der den Funktionsaufruf bedient, eine vollständige Synchronisierung der zugehörigen Namespacemetadaten aus dem PDC-Emulatormaster für diese Domäne durchführen kann. Diese vollständige Synchronisierung kann auch dann ausgeführt werden, wenn der Stammskalierbarkeitsmodus für diesen Namespace konfiguriert ist.
