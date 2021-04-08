---
title: Ändern der Richtlinie für Neuübertragungen
description: Die Microsoft WinSNMP-Implementierung bietet Unterstützung für Neuübertragungs Richtlinien, indem ein Timeout Wert und eine Wiederholungs Anzahl für die WinSNMP-Anwendung in einer-Datenbank gespeichert werden.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856188"
---
# <a name="changing-the-retransmission-policy"></a><span data-ttu-id="2431f-103">Ändern der Richtlinie für Neuübertragungen</span><span class="sxs-lookup"><span data-stu-id="2431f-103">Changing the Retransmission Policy</span></span>

<span data-ttu-id="2431f-104">Die Microsoft WinSNMP-Implementierung bietet Unterstützung für Neuübertragungs Richtlinien, indem ein Timeout Wert und eine Wiederholungs Anzahl für die WinSNMP-Anwendung in einer-Datenbank gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2431f-104">The Microsoft WinSNMP implementation provides retransmission policy support by storing a time-out value and a retry count for the WinSNMP application in a database.</span></span> <span data-ttu-id="2431f-105">Die-Implementierung speichert Werte für einzelne Ziel Entitäten.</span><span class="sxs-lookup"><span data-stu-id="2431f-105">The implementation stores values for individual destination entities.</span></span> <span data-ttu-id="2431f-106">Die-Implementierung liefert anfänglich Standardwerte für diese Elemente, aber eine Anwendung kann Werte für einzelne Entitäten hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="2431f-106">The implementation initially supplies default values for these elements, but an application can add or modify values for individual entities.</span></span>

<span data-ttu-id="2431f-107">Ein Aufruf der Funktionen [**snmpgettimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) und [**snmpgetretry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) gibt die Werte für Timeout und Wiederholungs Anzahl für eine bestimmte Ziel Entität zurück.</span><span class="sxs-lookup"><span data-stu-id="2431f-107">A call to the [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) and [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) functions returns the time-out and retry count values for a specific destination entity.</span></span> <span data-ttu-id="2431f-108">Um den Timeout Wert zu ändern, muss eine WinSNMP-Anwendung die [**snmpsettimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2431f-108">To change the time-out value, a WinSNMP application must call the [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) function.</span></span> <span data-ttu-id="2431f-109">Um den Wert für die Anzahl der Wiederholungs Versuche zu ändern, muss die Anwendung die [**snmpsetretry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="2431f-109">To change the retry count value the application must call the [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) function.</span></span> <span data-ttu-id="2431f-110">Die aktualisierten Einstellungen wirken sich auf neue SNMP-Nachrichten Anforderungen an die Ziel Entität aus.</span><span class="sxs-lookup"><span data-stu-id="2431f-110">The updated settings affect new SNMP message requests to the destination entity.</span></span>

 

 




