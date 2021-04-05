---
title: Aktualisieren eines PDU
description: Eine WinSNMP-Anwendung kann ausgewählte PDU-Felder mithilfe der snmpgetpdudata-Funktion und der snmpsetpdudata-Funktion abrufen und aktualisieren.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713337"
---
# <a name="updating-a-pdu"></a><span data-ttu-id="940ee-103">Aktualisieren eines PDU</span><span class="sxs-lookup"><span data-stu-id="940ee-103">Updating a PDU</span></span>

<span data-ttu-id="940ee-104">Eine WinSNMP-Anwendung kann ausgewählte PDU-Felder mithilfe der [**snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) -Funktion und der [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion abrufen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="940ee-104">A WinSNMP application can retrieve and update selected PDU fields by using the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) and the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) functions.</span></span>

<span data-ttu-id="940ee-105">Die Anwendung kann die Felder "PDU", "Anforderungs Bezeichner", "Fehlerstatus" und "Fehler index" von einem bestimmten PDU abrufen.</span><span class="sxs-lookup"><span data-stu-id="940ee-105">The application can retrieve the PDU type, request identifier, error status, and error index fields from a specific PDU.</span></span> <span data-ttu-id="940ee-106">Außerdem kann das Handle für die Variablen Bindungs Liste abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="940ee-106">It can also retrieve the handle to the variable binding list.</span></span> <span data-ttu-id="940ee-107">Die Anwendung kann die Felder **PDU- \_ Typ** und **Anforderungs- \_ ID** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="940ee-107">The application can update the **PDU\_type** and **request\_id** fields.</span></span>

<span data-ttu-id="940ee-108">Wenn der PDU-Typ gleich SNMP \_ PDU \_ Getbulk ist, kann die Anwendung auch die **nicht \_ Wiederhol** enden und die Felder für die **Maximale \_ Wiederholung** des PDU-Vorgangs aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="940ee-108">If the PDU type is equal to SNMP\_PDU\_GETBULK, the application can also update the **non\_repeaters** and the **max\_repetitions** fields of the PDU.</span></span>

 

 




