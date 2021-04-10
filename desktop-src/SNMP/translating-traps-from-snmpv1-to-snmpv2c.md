---
title: Übersetzen von Traps von SNMPv1 in SNMPv2C
description: Wenn die Microsoft WinSNMP-Implementierung Traps von einer Entität empfängt, die unter dem SNMPv1 Framework betrieben wird, übersetzt Sie die Traps in das SNMPv2C-Format.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d36870bda9b434bcc19f42332f2751020689591
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855747"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a><span data-ttu-id="9a22c-103">Übersetzen von Traps von SNMPv1 in SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="9a22c-103">Translating Traps from SNMPv1 to SNMPv2C</span></span>

<span data-ttu-id="9a22c-104">Wenn die Microsoft WinSNMP-Implementierung Traps von einer Entität empfängt, die unter dem SNMPv1 Framework betrieben wird, übersetzt Sie die Traps in das SNMPv2C-Format.</span><span class="sxs-lookup"><span data-stu-id="9a22c-104">When the Microsoft WinSNMP implementation receives traps from an entity operating under the SNMPv1 framework, it translates the traps to the SNMPv2C format.</span></span> <span data-ttu-id="9a22c-105">Wenn [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) einen Trap liefert, befindet er sich daher immer im SNMPv2C-Format.</span><span class="sxs-lookup"><span data-stu-id="9a22c-105">Therefore, when [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) delivers a trap it is always in the SNMPv2C format.</span></span> <span data-ttu-id="9a22c-106">RFC 1908, "Koexistenz zwischen Version 1 und Version 2 des Internet-Standard-Netzwerk Verwaltungs-Frameworks", gibt die Regeln für die Übersetzung aus SNMPv1 in das SNMPv2C Trap-Format an.</span><span class="sxs-lookup"><span data-stu-id="9a22c-106">RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework," specifies the rules for translating from the SNMPv1 to the SNMPv2C trap format.</span></span>

<span data-ttu-id="9a22c-107">Eine WinSNMP-Anwendung kann den letzten Variablen Bindungs Eintrag in einer Variablen Bindungs Liste überprüfen, um zu bestimmen, ob es sich bei dem Eintrag um einen Trap handelt, der aus dem SNMPv1-Format in das SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="9a22c-107">A WinSNMP application can check the last variable binding entry in a variable binding list to determine if the entry is a trap translated from the SNMPv1 to the SNMPv2C format.</span></span> <span data-ttu-id="9a22c-108">Wenn dies der Fall ist, ist die letzte Variablen Bindung immer gleich dem Wert "snmptrapterprieloid. 0".</span><span class="sxs-lookup"><span data-stu-id="9a22c-108">If so, the last variable binding will always be equal to the value "snmpTrapEnterpriseOID.0".</span></span>

<span data-ttu-id="9a22c-109">Weitere Informationen finden Sie unter [Verwalten von Traps und Benachrichtigungen](managing-traps-and-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="9a22c-109">For more information, see [Managing Traps and Notifications](managing-traps-and-notifications.md).</span></span>

 

 




