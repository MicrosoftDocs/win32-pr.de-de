---
title: Veröffentlichen mit dem RPC-Namensdienst
description: RPC-Dienste können ihre Bezeichner in einem Namespace mithilfe der RPC-Namensdienst-APIs (RPCNs) veröffentlichen.
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Veröffentlichen mit DEM RPC-Namensdienst-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd53922bd4ce952c18c58d1b71cb485887bdc0fd020f4113679eb114b32b6f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025368"
---
# <a name="publishing-with-the-rpc-name-service"></a>Veröffentlichen mit dem RPC-Namensdienst

RPC-Dienste können ihre Bezeichner in einem Namespace mithilfe der RPC-Namensdienst-APIs (RPCNs) veröffentlichen. Die RPCNs-APIs in Windows 2000 veröffentlichen die RPC-Einträge in Active Directory Domain Services. Dienste erstellen RPC-Bindungen und veröffentlichen sie im Namespace als benannte RPC-Servereinträge mit Attributen, einschließlich der eindeutigen Schnittstellen-ID, einer GUID, die von Clients erkannt wird. Ein Client kann dann nach RPC-Servern suchen, die die gewünschte Schnittstelle bieten, die Bindung importieren und eine Verbindung mit dem Server herstellen.

Weitere Informationen zum Veröffentlichen eines RPC-Diensts finden Sie unter [Serverseitige Bindung.](/windows/desktop/Rpc/server-side-binding)

 

 