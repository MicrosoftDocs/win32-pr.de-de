---
title: Die WinSNMP-Datenbank
description: Die Microsoft WinSNMP-Implementierung verwaltet einen Speicher von administrativen Informationen in einer-Datenbank.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471093"
---
# <a name="the-winsnmp-database"></a><span data-ttu-id="88037-103">Die WinSNMP-Datenbank</span><span class="sxs-lookup"><span data-stu-id="88037-103">The WinSNMP Database</span></span>

<span data-ttu-id="88037-104">Die Microsoft WinSNMP-Implementierung verwaltet einen Speicher von administrativen Informationen in einer-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="88037-104">The Microsoft WinSNMP implementation maintains a store of administrative information in a database.</span></span> <span data-ttu-id="88037-105">Die-Datenbank enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="88037-105">The database includes the following information:</span></span>

-   <span data-ttu-id="88037-106">Netzwerk-und Versions Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="88037-106">Network and version properties.</span></span>

    <span data-ttu-id="88037-107">Die-Implementierung verwendet diese Eigenschaften, um zu bestimmen, welches Netzwerk Transportprotokoll und welches SNMP-Versions Framework zum Durchführen von Übertragungsanforderungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="88037-107">The implementation uses these properties to determine which network transport protocol and SNMP version framework to use to complete transmission requests.</span></span> <span data-ttu-id="88037-108">Weitere Informationen finden Sie unter Informationen [zu SNMP-Versionen](about-snmp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="88037-108">For more information, see [About SNMP Versions](about-snmp-versions.md).</span></span>

-   <span data-ttu-id="88037-109">Der Entitäts-und Kontext Übersetzungsmodus.</span><span class="sxs-lookup"><span data-stu-id="88037-109">Entity and context translation mode.</span></span>

    <span data-ttu-id="88037-110">Die-Implementierung verwendet diesen Modus, um benutzerfreundliche Namen für SNMP-Entitäten und-Kontexte zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="88037-110">The implementation uses this mode to interpret user-friendly names for SNMP entities and contexts.</span></span> <span data-ttu-id="88037-111">Weitere Informationen finden Sie unter [Festlegen des Entitäts-und Kontext Übersetzungsmodus](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="88037-111">For more information, see [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

-   <span data-ttu-id="88037-112">Neuübertragungs Richtlinien Einstellung.</span><span class="sxs-lookup"><span data-stu-id="88037-112">Retransmission policy setting.</span></span>

    <span data-ttu-id="88037-113">Die-Implementierung verwendet diese Einstellung, um zu bestimmen, ob Sie die Richtlinie zur erneuten Übertragung der Anwendung ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="88037-113">The implementation uses this setting to determine whether or not it should execute the application's retransmission policy.</span></span> <span data-ttu-id="88037-114">Die-Implementierung speichert einen Timeout Wert und eine Wiederholungs Anzahl für jede Ziel Entität.</span><span class="sxs-lookup"><span data-stu-id="88037-114">The implementation stores a time-out value and a retry count for each destination entity.</span></span> <span data-ttu-id="88037-115">Weitere Informationen finden Sie unter Informationen [zur erneuten Übertragung](about-retransmission.md) und zur [Verwaltung der Richtlinie für die Neuübertragung](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="88037-115">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 




