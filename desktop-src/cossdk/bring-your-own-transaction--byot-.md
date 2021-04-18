---
description: Bring Your Own Transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Bring Your Own Transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344618"
---
# <a name="bring-your-own-transaction-byot"></a>Bring Your Own Transaction (BYOT)

BYOT ermöglicht das Erstellen einer Komponente mit oder, um eine externe Transaktion zu erben. Dies bedeutet, dass eine Komponente, die noch nicht über eine zugehörige Transaktion verfügt, eine Transaktion abrufen kann. Derzeit sind MTS-Transaktionen automatisch. ob eine Komponenteninstanz in einer Transaktion aktiv ist, wird zur Erstellungszeit bestimmt. Die Transaktions Attribute einer Komponente und deren Ersteller bestimmen, welche Transaktion mit einer bestimmten Instanz verknüpft ist. In allen Fällen steuert MTS die Transaktions Lebensdauer. Com+ erweitert dieses, um das Festlegen einer beliebigen bereits vorhandenen DTC-oder Tip-Transaktion als Transaktions Eigenschaft des Kontexts einer neuen Komponente zuzulassen. Dadurch können konfigurierte Komponenten mit Transaktionen verknüpft werden, deren Lebensdauer durch einen TP-Monitor, OTS oder DBMS gesteuert wird.

> [!Note]  
> BYOT-Transaktionen müssen mit Bedacht verwendet werden. In bestimmten Situationen können Sie zu einer Transaktion führen, die mehrere Synchronisierungs Domänen umfasst, d. –., Sie ermöglichen eine Parallelität mit einer Transaktion, wodurch eine Deadlockbedingung verursacht wird. Automatische Transaktionen und keine BYOT-Transaktionen sind das bevorzugte Programmiermodell für Writer von Geschäftskomponenten.

 

Die Schnittstellen für BYOT-Transaktionen umfassen die [**ikreatewithtransaktionex**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) -Schnittstelle und die [**ikreatewithtiptransaktionex**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) -Schnittstelle. Mit der **ikreatewithtransaktionex** -Schnittstelle wird ein Objekt erstellt, das in einer manuellen Transaktion eingetragen ist. Mit der **ikreatewithtiptransaktionex** -Schnittstelle wird ein Objekt erstellt, das in einer manuellen Transaktion mit dem Tip (Transaction Internet Protocol) eingetragen ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erben von manuellen Transaktionen](inheriting-manual-transactions.md)
</dt> </dl>

 

 



