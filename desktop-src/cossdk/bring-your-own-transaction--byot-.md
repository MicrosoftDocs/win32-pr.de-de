---
description: Bring Your Own Transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Bring Your Own Transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b6177471d1c56956bba5fafd4f728a6295b29afcc6873495ddb690d2e59c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308663"
---
# <a name="bring-your-own-transaction-byot"></a>Bring Your Own Transaction (BYOT)

BYOT ermöglicht das Erstellen einer Komponente mit oder zum Erben einer externen Transaktion. Das heißt, eine Komponente, der noch keine Transaktion zugeordnet ist, kann eine Transaktion abrufen. Derzeit werden MTS-Transaktionen automatisch ausgeführt. ob sich eine Komponenteninstanz in einer Transaktion befindet, wird zum Zeitpunkt der Erstellung bestimmt. Die Transaktionsattribute einer Komponente und deren Ersteller bestimmen, welche Transaktion einer bestimmten Instanz zugeordnet ist. In allen Fällen steuert MTS die Transaktionslebensdauer. COM+ erweitert dies, um das Festlegen einer beliebigen bereits vorhandenen DTC- oder TIP-Transaktion als Transaktionseigenschaft des Kontexts einer neuen Komponente zu ermöglichen. Dadurch können konfigurierte Komponenten Transaktionen zugeordnet werden, deren Lebensdauer von einem TP-Monitor, OTS oder DBMS gesteuert wird.

> [!Note]  
> BYOT-Transaktionen müssen mit Vorsicht verwendet werden. In bestimmten Situationen können sie zu einer Transaktion führen, die sich über mehrere Synchronisierungsdomänen erstreckt, d. h., sie ermöglichen Parallelität mit einer Transaktion und verursachen eine Deadlockbedingung. Automatische Transaktionen anstelle von BYOT-Transaktionen sind das bevorzugte Programmiermodell für Writer von Geschäftskomponenten.

 

Zu den Schnittstellen für BYOT-Transaktionen gehören die [**ICreateWithTransactionEx-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) und die [**ICreateWithTipTransactionEx-Schnittstelle.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) Die **ICreateWithTransactionEx-Schnittstelle** erstellt ein Objekt, das in einer manuellen Transaktion eingetragen wird. Die **ICreateWithTipTransactionEx-Schnittstelle** erstellt ein Objekt, das in einer manuellen Transaktion mithilfe des Transaction Internet Protocol (TIP) eingetragen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erben manueller Transaktionen](inheriting-manual-transactions.md)
</dt> </dl>

 

 



