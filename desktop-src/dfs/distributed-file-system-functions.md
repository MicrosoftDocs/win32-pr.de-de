---
title: Verteiltes Dateisystem Funktionen
description: Im folgenden finden Sie die verteiltes Dateisystem (DFS)-Funktionen.
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483766"
---
# <a name="distributed-file-system-functions"></a>Verteiltes Dateisystem Funktionen

Im folgenden finden Sie die verteiltes Dateisystem (DFS)-Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Netdfsadd](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
Erstellt eine neue DFS-Verknüpfung (verteiltes Dateisystem) oder fügt Ziele zu einem vorhandenen Link in einem DFS-Namespace hinzu.

</dd> <dt>

[Netdfsaddftroot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
Erstellt einen neuen domänenbasierten verteiltes Dateisystem-Namespace (DFS). Wenn der Namespace bereits vorhanden ist, fügt die Funktion ihm das angegebene Stamm Ziel hinzu.

</dd> <dt>

[Netdfsaddroottarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
Erstellt einen domänenbasierten oder eigenständigen DFS-Namespace oder fügt einem vorhandenen domänenbasierten Namespace ein neues Stamm Ziel hinzu.

</dd> <dt>

[Netdfsaddstdroot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
Erstellt einen neuen eigenständigen verteiltes Dateisystem-Namespace (DFS).

</dd> <dt>

[Netdfsenum](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
Listet die verteiltes Dateisystem (DFS)-Namespaces auf, die auf einem Server oder DFS-Verknüpfungen eines von einem Server gehosteten Namespace gehostet werden.

</dd> <dt>

[Netdfsgetclientinfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
Ruft Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link aus dem Cache ab, der vom DFS-Client verwaltet wird.

</dd> <dt>

[Netdfsgetftcontainersecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
Ruft die Sicherheits Beschreibung für das Container Objekt für die domänenbasierten DFS-Namespaces in der angegebenen Active Directory Domäne ab.

</dd> <dt>

[Netdfsgetinfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
Ruft Informationen zu einem angegebenen verteiltes Dateisystem (DFS)-Stamm oder-Link in einem DFS-Namespace ab.

</dd> <dt>

[Netdfsgetsecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
Ruft die Sicherheits Beschreibung für das Stamm Objekt des angegebenen DFS-Namespace ab.

</dd> <dt>

[Netdfsgetstdcontainersecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
Ruft die Sicherheits Beschreibung für das Container Objekt des angegebenen eigenständigen DFS-Namespace ab.

</dd> <dt>

[Netdfsgetsupportednamespaceversion](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
Bestimmt die unterstützte Metadatenversionsnummer.

</dd> <dt>

[Netdfsmove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
Benennt oder verschiebt einen DFS-Link.

</dd> <dt>

[Netdfsremove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
Entfernt einen verteiltes Dateisystem (DFS)-Link oder ein bestimmtes Verknüpfungs Ziel eines DFS-Links in einem DFS-Namespace. Wenn Sie ein bestimmtes Verknüpfungs Ziel entfernen, wird der Link selbst entfernt, wenn das letzte Verknüpfungs Ziel der Verknüpfung entfernt wird.

</dd> <dt>

[Netdfsremovef](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
Entfernt das angegebene Stamm Ziel aus einem domänenbasierten verteiltes Dateisystem (DFS)-Namespace. Wenn das letzte Stamm Ziel des DFS-Namespace entfernt wird, löscht die Funktion auch den DFS-Namespace. Ein DFS-Namespace kann gelöscht werden, ohne zuerst alle darin Verknüpfungen zu löschen.

</dd> <dt>

[Netdfsremovestrootforced](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
Entfernt das angegebene Stamm Ziel aus einem domänenbasierten verteiltes Dateisystem (DFS)-Namespace, auch wenn der Stamm Zielserver offline ist. Wenn das letzte Stamm Ziel des DFS-Namespace entfernt wird, löscht die Funktion auch den DFS-Namespace. Ein DFS-Namespace kann gelöscht werden, ohne zuerst alle darin Verknüpfungen zu löschen.

> [!Note]
> Die [**netdfsremoveftrootforced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) -Funktion aktualisiert die Registrierung auf dem DFS-Stamm Zielserver nicht. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

[Netdfsremoveroottarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
Entfernt ein DFS-Stamm Ziel aus einem domänenbasierten DFS-Namespace. Wenn das Stammziel das letzte Stamm Ziel im DFS-Namespace ist, entfernt diese Funktion den DFS-Namespace. Diese Funktion kann auch verwendet werden, um einen eigenständigen DFS-Namespace zu entfernen.

</dd> <dt>

[Netdfsremovestdroot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
Löscht einen eigenständigen verteiltes Dateisystem (DFS)-Namespace.

</dd> <dt>

[Netdfssetclientinfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
Ändert Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link im Cache, der vom DFS-Client verwaltet wird.

</dd> <dt>

[Netdfssetftcontainersecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
Legt die Sicherheits Beschreibung für das Container Objekt für die domänenbasierten DFS-Namespaces in der angegebenen Active Directory Domäne fest.

</dd> <dt>

[Netdfssetinfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
Legt Informationen über einen bestimmten verteiltes Dateisystem (DFS)-Stamm, ein Stamm Ziel, einen Link oder ein Verknüpfungs Ziel fest oder ändert Sie.

</dd> <dt>

[Netdfssetsecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
Legt die Sicherheits Beschreibung für das Stamm Objekt des angegebenen DFS-Namespace fest.

</dd> <dt>

[Netdfssetstdcontainersecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
Legt die Sicherheits Beschreibung für das Container Objekt des angegebenen eigenständigen DFS-Namespace fest.

</dd> </dl>

Beachten Sie, dass eine Anwendung, die eine der Funktionen aufruft, indirekt bewirken kann, dass der lokale DFS-Namespace Server, der den Funktionsaufruf verarbeitet, eine vollständige Synchronisierung der zugehörigen Namespace Metadaten aus dem PDC-Emulatormaster für diese Domäne ausführt. Diese vollständige Synchronisierung kann auch dann erfolgen, wenn der root-Skalierbarkeits Modus für diesen Namespace konfiguriert ist.
