---
description: Erstellen von BYOT-Objekten
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Erstellen von BYOT-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c2f0f999cb758a46dc779d29dac9fdfc71d2dbc245a84d1ca86060108e5663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128763"
---
# <a name="creating-byot-objects"></a>Erstellen von BYOT-Objekten

Ein neues BYOT-Objekt erstellt Objekte mit manuellen Transaktionen. Die beiden Schnittstellen [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) und [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex)verfügen über eine einzelne Methode, **CreateInstance,** die einen **ITransaction-Schnittstellenzeiger** bzw. eine TIP-URL annimmt. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) gibt einen Schnittstellenzeiger auf das neu erstellte Objekt zurück, das in der angegebenen Transaktion eingetragen wird.

Wenn ein Objekt mit einer manuellen Transaktion freigegeben wird, versucht COM+ nicht, einen Commit für die Transaktion durchzuführen. Die Transaktion wird explizit vom externen Transaktions-Manager gesteuert, der die Transaktion verteilt hat, unter der dieses Objekt erstellt wurde.

> [!Note]  
> Das Byot.ByotServerEx-Objekt muss in eine COM+-Anwendung importiert werden.

 

 

 



