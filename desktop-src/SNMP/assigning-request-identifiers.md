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
# <a name="assigning-request-identifiers"></a><span data-ttu-id="a1559-104">Zuweisen von Anforderungs bezeichlern</span><span class="sxs-lookup"><span data-stu-id="a1559-104">Assigning Request Identifiers</span></span>

<span data-ttu-id="a1559-105">Eine WinSNMP-Anwendung kann die [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion oder die [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion aufrufen, um einem PDU einen Anwendungs generierten Anforderungs Bezeichner zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a1559-105">A WinSNMP application can call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function to assign an application-generated request identifier to a PDU.</span></span> <span data-ttu-id="a1559-106">Die Anwendung muss den Wert im Anforderungs- *\_ ID* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="a1559-106">The application must pass the value in the *request\_id* parameter.</span></span>

<span data-ttu-id="a1559-107">Eine Anwendung kann anfordern, dass die Microsoft WinSNMP-Implementierung einen Anforderungs Bezeichner generiert und einem PDU zuweist, indem er im *Anforderungs- \_ ID* -Parameter der [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion NULL übergibt.</span><span class="sxs-lookup"><span data-stu-id="a1559-107">An application can request that the Microsoft WinSNMP implementation generate and assign a request identifier to a PDU by passing zero in the *request\_id* parameter of the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="a1559-108">Die Anwendung kann den zugewiesenen Anforderungs Bezeichner mit einem Aufrufen der [**snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="a1559-108">The application can retrieve the assigned request identifier with a call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function.</span></span>

<span data-ttu-id="a1559-109">Um einen Anforderungs Bezeichner, der einem bestimmten Wert entspricht, einschließlich null zuzuweisen, muss die Anwendung diesen Wert im *Anforderungs- \_ ID* -Parameter der [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="a1559-109">To assign a request identifier equal to a specific value, including zero, the application must pass that value in the *request\_id* parameter of the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span>

<span data-ttu-id="a1559-110">Wenn die Implementierung die Richtlinie zur erneuten Übertragung der Anwendung ausführt, enthält Sie das Feld **Anforderungs- \_ ID** des ursprünglichen PDU in jeder erneut übertragenen SNMP-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a1559-110">When the implementation executes the application's retransmission policy, it includes the **request\_id** field of the original PDU in each retransmitted SNMP message.</span></span> <span data-ttu-id="a1559-111">Weitere Informationen finden Sie unter Informationen [zur erneuten Übertragung](about-retransmission.md) und zur [Verwaltung der Richtlinie für die Neuübertragung](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="a1559-111">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

> [!Note]  
> <span data-ttu-id="a1559-112">Wenn die Implementierung Traps von einer SNMPv1-Entität empfängt, weist Sie dem **Anforderungs- \_ ID** -Feld des PDU einen Wert ungleich 0 (null) zu.</span><span class="sxs-lookup"><span data-stu-id="a1559-112">When the implementation receives traps from an SNMPv1 entity, it assigns a non-zero value to the **request\_id** field of the PDU.</span></span> <span data-ttu-id="a1559-113">Dieser Wert kann einen von der Anwendung verwendeten Anforderungs Bezeichner in einem Anforderungs-PDU duplizieren.</span><span class="sxs-lookup"><span data-stu-id="a1559-113">This value may duplicate a request identifier used by the application in a request PDU.</span></span> <span data-ttu-id="a1559-114">Anwendungen müssen auf Duplizierung prüfen.</span><span class="sxs-lookup"><span data-stu-id="a1559-114">Applications must check for duplication.</span></span>

 

 

 




