---
title: Duplizieren eines PDU
description: Die SnmpDuplicatePdu-Funktion dupliziert ein PDU und gibt den erforderlichen Arbeitsspeicher zu. Um Ressourcen frei zu geben, die von SnmpDuplicatePdu für ein neues PDU zugeordnet werden, muss eine WinSNMP-Anwendung die SnmpFreePdu-Funktion aufrufen.
ms.assetid: 371e566b-0577-4089-b081-17085c9587fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9f9fdecd41ce8ad0d430f5ddc61748b365bd2e0a647067cd2bcf39d050599a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009558"
---
# <a name="duplicating-a-pdu"></a>Duplizieren eines PDU

Die [**SnmpDuplicatePdu-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) dupliziert ein PDU und gibt den erforderlichen Arbeitsspeicher zu. Um Ressourcen frei zu geben, die **von SnmpDuplicatePdu** für ein neues PDU zugeordnet werden, muss eine WinSNMP-Anwendung die [**SnmpFreePdu-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) aufrufen.

 

 




