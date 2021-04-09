---
title: Verteiltes Dateisystem von Steuerungs Codes
description: Verteiltes Dateisystem DFS-Steuerungs Codes
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe054f87210c40da595dd731b263c485311729a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948871"
---
# <a name="distributed-file-system-control-codes"></a>Verteiltes Dateisystem von Steuerungs Codes

Im folgenden finden Sie die verteiltes Dateisystem (DFS)-Steuercodes:

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

Der [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) Steuerungs Code kann die gleichen Informationen wie die [**netdfsgetclientinfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) -Funktion erhalten, kann jedoch bei manchen Konfigurationen mit hohen Wartezeiten für die DFS-Server eine bessere Leistung erzielen. Es wird nicht empfohlen, den **FSCTL_DFS_GET_PKT_ENTRY_STATE** Control-Code zu verwenden, es sei denn, es treten Leistungsprobleme auf.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) aufzurufen.

</dd> </dl>