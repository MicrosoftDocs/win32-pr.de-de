---
description: Im folgenden finden Sie die verteiltes Dateisystem DFS-Strukturen.
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Verteiltes Dateisystem Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483771"
---
# <a name="distributed-file-system-structures"></a>Verteiltes Dateisystem Strukturen

Im folgenden sind die verteiltes Dateisystem (DFS)-Strukturen aufgeführt:

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Der Eingabepuffer wird mit dem [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) Steuerungs Code verwendet.
</dd> <dt>

[_DFS_INFO_1 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Enthält den Namen eines DFS-Stamms oder-Links (verteiltes Dateisystem).

</dd> <dt>

[_DFS_INFO_2 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link. Diese Struktur enthält den Namen, den Status und die Anzahl der DFS-Ziele für den Stamm oder Link.

</dd> <dt>

[_DFS_INFO_3 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link. Diese Struktur enthält den Namen, den Status, die Anzahl der DFS-Ziele und Informationen zu den einzelnen Zielen des Stamms oder Links.

</dd> <dt>

[_DFS_INFO_4 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link. Diese Struktur enthält den Namen, den Status, die **GUID**, das Timeout, die Anzahl der Ziele und Informationen zu den einzelnen Zielen des Stamms oder Links.

</dd> <dt>

[_DFS_INFO_5 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link. Diese Struktur enthält den Namen, den Status, die **GUID**, das Timeout, den Namespace bzw. die Stamm-/Linkeigenschaften, die Metadatengröße und die Anzahl der Ziele für den Stamm oder Link.

</dd> <dt>

[_DFS_INFO_6 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link. Diese Struktur enthält den Namen, den Status, die **GUID**, das Timeout, den Namespace bzw. die Stamm-/Linkeigenschaften, die Metadatengröße, die Anzahl der Ziele und Informationen zu den einzelnen Zielen des Stamms oder Links.

</dd> <dt>

[_DFS_INFO_7 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Enthält Informationen zu einem DFS-Namespace. Diese Struktur enthält die Versions- **GUID** für die Metadaten für den Namespace.

</dd> <dt>

[_DFS_INFO_8 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Enthält den Namen, den Status, die **GUID**, das Timeout, die Eigenschaftenflags, die Metadatengröße, Informationen zum DFS-Ziel und die Sicherheits Beschreibung für den Link Analyse Punkt für einen Stamm oder Link.

</dd> <dt>

[_DFS_INFO_9 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Enthält den Namen, den Status, die **GUID**, das Timeout, die Eigenschaftenflags, die Metadatengröße, Informationen zum DFS-Ziel, die Sicherheits Beschreibung für den Link Analyse Punkt und eine Liste der DFS-Ziele für einen Stamm oder Link.

</dd> <dt>

[_DFS_INFO_50 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Enthält die DFS-Metadatenversion und die Funktionen eines vorhandenen DFS-Namespace.

</dd> <dt>

[_DFS_INFO_100 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Enthält einen Kommentar, der einem DFS-Stamm oder einem verteiltes Dateisystem-Link zugeordnet ist.

</dd> <dt>

[_DFS_INFO_101 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Beschreibt den Zustand des Speichers in einem DFS-Stamm, einem Link, einem Stammziel oder einem Verknüpfungs Ziel.

</dd> <dt>

[_DFS_INFO_102 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Enthält einen Timeout Wert, der einem verteiltes Dateisystem (DFS)-Stamm oder einem Link in einem benannten DFS-Stamm zugeordnet werden soll.

</dd> <dt>

[_DFS_INFO_103 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Enthält Eigenschaften, mit denen bestimmte Verhalten für einen DFS-Stamm oder-Link festgelegt werden.

</dd> <dt>

[_DFS_INFO_104 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Enthält die Priorität eines DFS-Stammpink oder-Verknüpfungs Ziels.

</dd> <dt>

[_DFS_INFO_105 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Enthält Informationen zu einem DFS-Stamm oder-Link, einschließlich Kommentar-, Zustands-, Timeout-und DFS-Verhalten, die durch Eigenschaftenflags angegeben werden.

</dd> <dt>

[_DFS_INFO_106 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Enthält den Speicher Zustand und die Priorität für ein DFS-Stamm Ziel oder-Verknüpfungs Ziel. Diese Struktur ist nur für die Verwendung mit der [**netdfssetinfo**](netdfssetinfo.md) -Funktion vorgesehen.

</dd> <dt>

[_DFS_INFO_107 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Enthält Informationen zu einem DFS-Stamm oder-Link, einschließlich Kommentar, Status, Timeout, Eigenschaftenflags und Sicherheits Beschreibung für den Link Analyse Punkt.

</dd> <dt>

[_DFS_INFO_150 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Enthält die Sicherheits Beschreibung für den Analyse Punkt eines DFS-Links.

</dd> <dt>

[_DFS_INFO_200 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Enthält den Namen eines domänenbasierten verteiltes Dateisystem-Namespace (DFS).

</dd> <dt>

[_DFS_INFO_300 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Enthält den Namen und den Typ (Domänen basiert oder eigenständig) eines DFS-Namespace.

</dd> <dt>

[_DFS_STORAGE_INFO Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Enthält Informationen zu einem DFS-Stamm oder-Verknüpfungs Ziel in einem DFS-Namespace oder dem vom DFS-Client verwalteten Cache.

</dd> <dt>

[_DFS_STORAGE_INFO_1 Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Enthält Informationen zu einem DFS-Ziel, einschließlich des DFS-Zielserver namens und des Freigabe namens sowie des Ziel Zustands und der Ziel Priorität.

</dd> <dt>

[_DFS_SUPPORTED_NAMESPACE_VERSION_INFO Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Enthält Versionsinformationen für einen DFS-Namespace.

</dd> <dt>

[_DFS_TARGET_PRIORITY Struktur](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Enthält die Prioritäts Klasse und den Rang eines bestimmten DFS-Ziels.

</dd> </dl>
