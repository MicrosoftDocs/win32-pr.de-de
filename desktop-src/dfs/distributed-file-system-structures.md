---
description: Im Folgenden sind die verteiltes Dateisystem DFS-Strukturen dargestellt.
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: verteiltes Dateisystem Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1561a4586cc03304c6aa1c1e323eb42fd09766df0cc3c7210636367337873a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541281"
---
# <a name="distributed-file-system-structures"></a>verteiltes Dateisystem Strukturen

Im Folgenden sind die dfs-Strukturen (verteiltes Dateisystem) dargestellt:

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Eingabepuffer, der [](fsctl-dfs-get-pkt-entry-state.md) mit dem FSCTL_DFS_GET_PKT_ENTRY_STATE-Steuerelementcode verwendet wird
</dd> <dt>

[_DFS_INFO_1-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Enthält den Namen eines verteiltes Dateisystem (DFS)-Stamm- oder -Links.

</dd> <dt>

[_DFS_INFO_2-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder -Link. Diese Struktur enthält den Namen, den Status und die Anzahl der DFS-Ziele für den Stamm oder Link.

</dd> <dt>

[_DFS_INFO_3-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder -Link. Diese Struktur enthält den Namen, den Status, die Anzahl der DFS-Ziele und Informationen zu jedem Ziel des Stamms oder Links.

</dd> <dt>

[_DFS_INFO_4-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder -Link. Diese Struktur enthält den Namen, den Status, **die GUID,** das Time out, die Anzahl der Ziele und Informationen zu jedem Ziel des Stamms oder Links.

</dd> <dt>

[_DFS_INFO_5 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder -Link. Diese Struktur enthält Name, Status, **GUID,** Time out, Namespace-/Stamm-/Linkeigenschaften, Metadatengröße und Anzahl der Ziele für den Stamm oder Link.

</dd> <dt>

[_DFS_INFO_6-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder -Link. Diese Struktur enthält Name, Status, **GUID,** Time out, Namespace-/Stamm-/Linkeigenschaften, Metadatengröße, Anzahl der Ziele und Informationen zu jedem Ziel des Stamms oder Links.

</dd> <dt>

[_DFS_INFO_7-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Enthält Informationen zu einem DFS-Namespace. Diese Struktur enthält die **Versions-GUID** für die Metadaten für den Namespace.

</dd> <dt>

[_DFS_INFO_8 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Enthält name, status, **GUID,** time-out, property flags, metadata size, DFS target information und link reparse point security descriptor for a root or link.

</dd> <dt>

[_DFS_INFO_9 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Enthält name, status, **GUID,** time-out, property flags, metadata size, DFS target information, link reparse point security descriptor und eine Liste der DFS-Ziele für einen Stamm oder Link.

</dd> <dt>

[_DFS_INFO_50-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Enthält die DFS-Metadatenversion und die Funktionen eines vorhandenen DFS-Namespace.

</dd> <dt>

[_DFS_INFO_100-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Enthält einen Kommentar, der einem verteiltes Dateisystem (DFS)-Stamm oder -Link zugeordnet ist.

</dd> <dt>

[_DFS_INFO_101-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Beschreibt den Zustand des Speichers auf einem DFS-Stamm-, Link-, Stamm- oder Linkziel.

</dd> <dt>

[_DFS_INFO_102-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Enthält einen Time out-Wert, der einem verteiltes Dateisystem (DFS)-Stamm oder einem Link in einem benannten DFS-Stamm zugeordnet werden soll.

</dd> <dt>

[_DFS_INFO_103-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Enthält Eigenschaften, die bestimmte Verhaltensweisen für einen DFS-Stamm oder -Link festlegen.

</dd> <dt>

[_DFS_INFO_104-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Enthält die Priorität eines DFS-Stammziels oder -Linkziels.

</dd> <dt>

[_DFS_INFO_105-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Enthält Informationen zu einem DFS-Stamm oder -Link, einschließlich Kommentar, Status, Time out und DFS-Verhalten, die durch Eigenschaftenflags angegeben werden.

</dd> <dt>

[_DFS_INFO_106-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Enthält den Speicherstatus und die Priorität für ein DFS-Stammziel oder -Linkziel. Diese Struktur ist nur für die Verwendung mit der [**NetDfsSetInfo-Funktion**](netdfssetinfo.md) vorgesehen.

</dd> <dt>

[_DFS_INFO_107-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Enthält Informationen zu einem DFS-Stamm oder -Link, einschließlich Kommentar, Status, Time out, Eigenschaftsflags und Sicherheitsbeschreibung des Verknüpfungsrearsepunkts.

</dd> <dt>

[_DFS_INFO_150 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Enthält die Sicherheitsbeschreibung für den Wiederholungspunkt eines DFS-Links.

</dd> <dt>

[_DFS_INFO_200 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Enthält den Namen eines domänenbasierten verteiltes Dateisystem-Namespace (DFS).

</dd> <dt>

[_DFS_INFO_300-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Enthält den Namen und Typ (domänenbasiert oder eigenständig) eines DFS-Namespace.

</dd> <dt>

[_DFS_STORAGE_INFO-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Enthält Informationen zu einem DFS-Stamm- oder -Linkziel in einem DFS-Namespace oder aus dem Cache, der vom DFS-Client verwaltet wird.

</dd> <dt>

[_DFS_STORAGE_INFO_1-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Enthält Informationen zu einem DFS-Ziel, einschließlich des DFS-Zielservernamens und freigabenamens sowie des Status und der Priorität des Ziels.

</dd> <dt>

[_DFS_SUPPORTED_NAMESPACE_VERSION_INFO-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Enthält Versionsinformationen für einen DFS-Namespace.

</dd> <dt>

[_DFS_TARGET_PRIORITY-Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Enthält die Prioritätsklasse und den Rang eines bestimmten DFS-Ziels.

</dd> </dl>
