---
title: Bindungs handle-Funktionen
description: Die folgende Tabelle enthält die Liste der RPC-Lauf Zeit Routinen, die für Bindungs Handles verwendet werden, und gibt den Typ des zulässigen Bindungs Handles an.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339188"
---
# <a name="binding-handle-functions"></a>Bindungs handle-Funktionen

Die folgende Tabelle enthält die Liste der RPC-Lauf Zeit Routinen, die für Bindungs Handles verwendet werden, und gibt den Typ des zulässigen Bindungs Handles an.



| -Routine zurückgegebener Wert                                                            | Eingabe Argument   | Ausgabe Argument |
|--------------------------------------------------------------------|------------------|-----------------|
| [**Rpcbindingcopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | Server           | Server          |
| [**Rpcbindingfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | Server           | Keine            |
| [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | Keine             | Server          |
| [**Rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | Client           | Keine            |
| [**Rpcbindinginqauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | Server           | Keine            |
| [**Rpcbindinginqobject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | Server oder Client | Keine            |
| [**Rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | Server           | Keine            |
| [**Rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | Server           | Keine            |
| [**Rpcbindingsetobject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | Server           | Keine            |
| [**Rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | Server oder Client | Keine            |
| [**Rpcbindingvector Free**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | Server           | Keine            |
| [**Rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | Server           | Keine            |
| [**Rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | Keine             | Server          |
| [**Rpcnsbindinglookupnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | Keine             | Server          |
| [**Rpcnsbindingselect**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | Server           | Server          |
| [**Rpcserverinqbindungen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | Keine             | Server          |



 

 

 




