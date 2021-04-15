---
description: In einem Pool zusammengefasste Ressourcen Zustände für com+-Ressourcen Spender verfügbar
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: In einem Pool zusammengefasste Ressourcen Zustände für com+-Ressourcen Spender verfügbar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483430"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>In einem Pool zusammengefasste Ressourcen Zustände für com+-Ressourcen Spender verfügbar

Eine Ressource wird zu einem beliebigen Zeitpunkt entweder verwendet oder nicht verwendet und ist entweder eingetragen oder nicht in eine Transaktion eingetragen. Dies ergibt vier mögliche Ressourcen Zustände, wie im folgenden dargestellt:

-   **Ressourcen in der aufgelistete Inventur.** Eine Ressource, die nicht von einem Objekt verwendet wird und nicht in einer Transaktion eingetragen ist, befindet sich in der aufgelistete Inventur. Eine Ressource im allgemeinen bestand ist für die Zuweisung verfügbar.

-   **Ressourcen in der eingetragenen Inventur.** Eine Ressource, die nicht von einem Objekt verwendet wird, sondern in einer Transaktion eingetragen ist, befindet sich in der eingetragenen Inventur. Eine solche Ressource steht nur für Objekte zur Verfügung, die in derselben Transaktion ausgeführt werden. Eine Ressource wird von der eingetragenen Inventur in die Registrierung eingetragen, wenn com+ den Dispenser-Manager benachrichtigt, dass die Transaktion abgeschlossen ist.

-   **Ressourcen in der aufgelistete Verwendung.** Wenn eine Ressource einem Objekt zugewiesen ist und die Instanz nicht in einer Transaktion ausgeführt wird oder der Ressourcen Verteiler die Ressource als nicht transaktional identifiziert hat, befindet sich diese Ressource in der Registrierung.

-   **In eingetragene Ressourcen.** Wenn eine Ressource einem Objekt zugewiesen ist, wird die Instanz in einer Transaktion ausgeführt, und der Ressourcen Verteiler hat die Ressource erfolgreich in die Transaktion eingetragen. diese Ressource wird in eingetragen verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte des com+-Ressourcen Verteilers](com--resource-dispenser-concepts.md)
</dt> <dt>

[Eintragen einer Ressource in eine Transaktion](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



