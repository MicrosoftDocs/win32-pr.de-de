---
title: Falsche Schnittstellenwarnungsrückrufe
description: Nachdem die Kernel-Forwarder Multicastdaten von einer bestimmten Quelle auf der falschen Schnittstelle empfangen hat, benachrichtigt sie den Multicastgruppen-Manager.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3354b1355cbcb1654b41a61ab046e74ec41b8dc716de6d50f7d9d52b18d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024650"
---
# <a name="wrong-interface-alert-callbacks"></a>Falsche Schnittstellenwarnungsrückrufe

Nachdem die Kernel-Forwarder Multicastdaten von einer bestimmten Quelle auf der falschen Schnittstelle empfangen hat, benachrichtigt sie den Multicastgruppen-Manager. Der Multicastgruppen-Manager ruft dann den [**PMGM \_ WRONG \_ IF \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) für das Routingprotokoll auf, das die Schnittstelle besitzt, auf der die Daten fälschlicherweise eingetroffen sind.

> [!Note]  
> Dieser Rückruf ist in dieser Version der MGM-API derzeit nicht implementiert.

 

 

 




