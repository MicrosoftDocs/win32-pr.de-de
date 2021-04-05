---
title: Zuweisen von Anforderungs bezeichlern
description: Eine WinSNMP-Anwendung kann die snmpkreatepdu-Funktion oder die snmpsetpdudata-Funktion aufrufen, um einem PDU einen Anwendungs generierten Anforderungs Bezeichner zuzuweisen. Die Anwendung muss den Wert im Anforderungs- \_ ID-Parameter übergeben.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707319"
---
# <a name="assigning-request-identifiers"></a>Zuweisen von Anforderungs bezeichlern

Eine WinSNMP-Anwendung kann die [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion oder die [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion aufrufen, um einem PDU einen Anwendungs generierten Anforderungs Bezeichner zuzuweisen. Die Anwendung muss den Wert im Anforderungs- *\_ ID* -Parameter übergeben.

Eine Anwendung kann anfordern, dass die Microsoft WinSNMP-Implementierung einen Anforderungs Bezeichner generiert und einem PDU zuweist, indem er im *Anforderungs- \_ ID* -Parameter der [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion NULL übergibt. Die Anwendung kann den zugewiesenen Anforderungs Bezeichner mit einem Aufrufen der [**snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) -Funktion abrufen.

Um einen Anforderungs Bezeichner, der einem bestimmten Wert entspricht, einschließlich null zuzuweisen, muss die Anwendung diesen Wert im *Anforderungs- \_ ID* -Parameter der [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion übergeben.

Wenn die Implementierung die Richtlinie zur erneuten Übertragung der Anwendung ausführt, enthält Sie das Feld **Anforderungs- \_ ID** des ursprünglichen PDU in jeder erneut übertragenen SNMP-Nachricht. Weitere Informationen finden Sie unter Informationen [zur erneuten Übertragung](about-retransmission.md) und zur [Verwaltung der Richtlinie für die Neuübertragung](managing-the-retransmission-policy.md).

> [!Note]  
> Wenn die Implementierung Traps von einer SNMPv1-Entität empfängt, weist Sie dem **Anforderungs- \_ ID** -Feld des PDU einen Wert ungleich 0 (null) zu. Dieser Wert kann einen von der Anwendung verwendeten Anforderungs Bezeichner in einem Anforderungs-PDU duplizieren. Anwendungen müssen auf Duplizierung prüfen.

 

 

 




