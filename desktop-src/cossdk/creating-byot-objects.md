---
description: Erstellen von BYOT-Objekten
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Erstellen von BYOT-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343172"
---
# <a name="creating-byot-objects"></a>Erstellen von BYOT-Objekten

Ein neues BYOT-Objekt erstellt Objekte mit manuellen Transaktionen. Die beiden Schnittstellen [**ikreatewithtransaktionex**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) und [**ikreatewithtiptransaktionex**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex)verfügen über eine einzige Methode, " **kreateinstance**", die einen **ITransaction** -Schnittstellen Zeiger bzw. eine Tip-URL annimmt. " [**Kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) " gibt einen Schnittstellen Zeiger auf das neu erstellte Objekt zurück, das in der angegebenen Transaktion eingetragen ist.

Wenn ein Objekt mit einer manuellen Transaktion freigegeben wird, versucht com+ nicht, einen Commit für die Transaktion durchführen. Die Transaktion wird explizit vom externen Transaktions-Manager gesteuert, der die Transaktion ausgegeben hat, in der dieses Objekt erstellt wurde.

> [!Note]  
> Das BYOT. ByotServerEx-Objekt muss in eine COM+-Anwendung importiert werden.

 

 

 



