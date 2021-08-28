---
title: verteiltes Dateisystem-Steuerelementcodes
description: verteiltes Dateisystem DFS-Steuerungscodes
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d0a429bdb1e203d9b89f77e951d422cf3c0cef05cd5de5de39b537bb405f6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853530"
---
# <a name="distributed-file-system-control-codes"></a>verteiltes Dateisystem-Steuerelementcodes

Im Folgenden sind die Steuerungscodes für verteiltes Dateisystem (DFS) dargestellt:

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

Der [](fsctl-dfs-get-pkt-entry-state.md) FSCTL_DFS_GET_PKT_ENTRY_STATE-Steuerungscode kann die gleichen Informationen wie die [**NetDfsGetClientInfo-Funktion**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) abrufen, aber in einigen Konfigurationen mit hohen Latenzen für die DFS-Server eine bessere Leistung bieten. Es wird nicht empfohlen, den FSCTL_DFS_GET_PKT_ENTRY_STATE-Steuerungscode zu verwenden, es sei denn, es liegen Leistungsprobleme vor. 

Rufen Sie zum Ausführen dieses Vorgangs die [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) auf.

</dd> </dl>