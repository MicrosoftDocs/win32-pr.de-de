---
description: Pooled Resource States Available to COM+ Resource Dispenser
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Pooled Resource States Available to COM+ Resource Dispenser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0f28a54a85ed134bf95a8150b5bb4b9cb0d2fda15a16b0b96238ac8c2da18f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305619"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>Pooled Resource States Available to COM+ Resource Dispenser

Eine Ressource wird entweder verwendet oder nicht verwendet und ist entweder eingetragen oder nicht in einer Transaktion eingetragen. Dies ergibt vier mögliche Ressourcenzustände wie folgt:

-   **Ressourcen im nicht eingetragenen Bestand.** Eine Ressource, die nicht von einem Objekt verwendet und nicht in einer Transaktion eingetragen ist, befindet sich im nicht eingetragenen Bestand. Eine Ressource im allgemeinen Bestand ist für die Zuweisung verfügbar.

-   **Ressourcen im eingetragenen Bestand.** Eine Ressource, die nicht von einem Objekt verwendet wird, aber in einer Transaktion eingetragen ist, befindet sich im eingetragenen Bestand. Eine solche Ressource ist nur für die Zuweisung zu Objekten verfügbar, die in derselben Transaktion ausgeführt werden. Eine Ressource wechselt vom eingetragenen Inventar zum nicht eingetragenen Bestand, wenn COM+ den Versender-Manager benachrichtigt, dass die Transaktion abgeschlossen ist.

-   **Ressourcen in nicht eingetragener Verwendung.** Wenn eine Ressource einem Objekt zugewiesen ist und die Instanz nicht in einer Transaktion ausgeführt wird oder der Ressourcenverzehrer die Ressource als nicht transaktional identifiziert hat, wird diese Ressource nicht eingetragen.

-   **Ressourcen in der eingetragenen Verwendung.** Wenn eine Ressource einem Objekt zugewiesen ist, die Instanz in einer Transaktion ausgeführt wird und der Ressourcensender die Ressource erfolgreich in die Transaktion eingetragen hat, wird diese Ressource in die Liste aufgenommen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KONZEPTE DES COM+-Ressourcensenders](com--resource-dispenser-concepts.md)
</dt> <dt>

[Eintragung einer Ressource in eine Transaktion](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



