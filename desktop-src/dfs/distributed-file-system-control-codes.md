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
# <a name="distributed-file-system-control-codes"></a><span data-ttu-id="b6ed3-103">Verteiltes Dateisystem von Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="b6ed3-103">Distributed File System Control Codes</span></span>

<span data-ttu-id="b6ed3-104">Im folgenden finden Sie die verteiltes Dateisystem (DFS)-Steuercodes:</span><span class="sxs-lookup"><span data-stu-id="b6ed3-104">The following are the Distributed File System (DFS) control codes:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6ed3-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b6ed3-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b6ed3-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span><span class="sxs-lookup"><span data-stu-id="b6ed3-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span></span>](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

<span data-ttu-id="b6ed3-107">Der [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) Steuerungs Code kann die gleichen Informationen wie die [**netdfsgetclientinfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) -Funktion erhalten, kann jedoch bei manchen Konfigurationen mit hohen Wartezeiten für die DFS-Server eine bessere Leistung erzielen.</span><span class="sxs-lookup"><span data-stu-id="b6ed3-107">The [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="b6ed3-108">Es wird nicht empfohlen, den **FSCTL_DFS_GET_PKT_ENTRY_STATE** Control-Code zu verwenden, es sei denn, es treten Leistungsprobleme auf.</span><span class="sxs-lookup"><span data-stu-id="b6ed3-108">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="b6ed3-109">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b6ed3-109">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span>

</dd> </dl>