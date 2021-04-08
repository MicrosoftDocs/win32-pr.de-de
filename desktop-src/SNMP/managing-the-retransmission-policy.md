---
title: Verwalten der Richtlinie für Neuübertragungen
description: Die WinSNMP-Anwendung kann anfordern, dass die Microsoft WinSNMP-Implementierung die Richtlinie zur erneuten Übertragung der Anwendung ausführt. Wenn die Implementierung die erneute Übertragung verwaltet, werden die Timeout-und Wiederholungs Zählerwerte in der Datenbank verwendet.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037292"
---
# <a name="managing-the-retransmission-policy"></a><span data-ttu-id="19dc3-104">Verwalten der Richtlinie für Neuübertragungen</span><span class="sxs-lookup"><span data-stu-id="19dc3-104">Managing the Retransmission Policy</span></span>

<span data-ttu-id="19dc3-105">Die WinSNMP-Anwendung kann anfordern, dass die Microsoft WinSNMP-Implementierung die Richtlinie zur erneuten Übertragung der Anwendung ausführt.</span><span class="sxs-lookup"><span data-stu-id="19dc3-105">The WinSNMP application can request that the Microsoft WinSNMP implementation execute the application's retransmission policy.</span></span> <span data-ttu-id="19dc3-106">Wenn die Implementierung die erneute Übertragung verwaltet, werden die Timeout-und Wiederholungs Zählerwerte in der Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="19dc3-106">When the implementation manages retransmission, it uses the time-out period and the retry count values in its database.</span></span>

<span data-ttu-id="19dc3-107">Die-Implementierung identifiziert den Standardmodus für Neuübertragungen in einem Rückgabewert der [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) -Funktion während der Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="19dc3-107">The implementation identifies the default retransmission mode in a return value from the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function during initialization.</span></span> <span data-ttu-id="19dc3-108">Der Modus kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19dc3-108">The mode can be one of the following values.</span></span>



| <span data-ttu-id="19dc3-109">Wert</span><span class="sxs-lookup"><span data-stu-id="19dc3-109">Value</span></span>        | <span data-ttu-id="19dc3-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="19dc3-110">Meaning</span></span>                                                                      |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="19dc3-111">Snmpapi \_ auf</span><span class="sxs-lookup"><span data-stu-id="19dc3-111">SNMPAPI\_ON</span></span>  | <span data-ttu-id="19dc3-112">Die Implementierung führt die Neuübertragungs Richtlinie der Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="19dc3-112">The implementation is executing the application's retransmission policy.</span></span>     |
| <span data-ttu-id="19dc3-113">Snmpapi \_ deaktiviert</span><span class="sxs-lookup"><span data-stu-id="19dc3-113">SNMPAPI\_OFF</span></span> | <span data-ttu-id="19dc3-114">Die-Implementierung führt nicht die Neuübertragungs Richtlinie der Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="19dc3-114">The implementation is not executing the application's retransmission policy.</span></span> |



 

<span data-ttu-id="19dc3-115">Eine WinSNMP-Anwendung kann jederzeit den aktuellen Neuübertragungs Modus für die Implementierung abrufen, indem die [**snmpgetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="19dc3-115">A WinSNMP application can retrieve at any time the current retransmission mode in effect for the implementation by calling the [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) function.</span></span> <span data-ttu-id="19dc3-116">Die WinSNMP-API bietet andere [Datenbankfunktionen](winsnmp-functions.md) , die die Verwaltung der Richtlinie zur erneuten Übertragung vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="19dc3-116">The WinSNMP API provides other [database functions](winsnmp-functions.md) that simplify management of the retransmission policy.</span></span>

<span data-ttu-id="19dc3-117">Die WinSNMP-Anwendung kann während der Ausführung eines Programms jederzeit die Ausführung der Richtlinie anpassen, indem Sie einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="19dc3-117">At any time during program execution, the WinSNMP application can adjust execution of the policy by performing one of the following steps:</span></span>

-   <span data-ttu-id="19dc3-118">Fordern Sie an, dass die Implementierung die Neuübertragungs Richtlinie startet oder beendet, indem Sie die [**snmpstretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="19dc3-118">Request that the implementation start or stop executing the retransmission policy by calling the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="19dc3-119">Weitere Informationen finden Sie unter [aktivieren und Deaktivieren der erneuten Übertragung](turning-retransmission-on-and-off.md).</span><span class="sxs-lookup"><span data-stu-id="19dc3-119">For more information, see [Turning Retransmission On and Off](turning-retransmission-on-and-off.md).</span></span>
-   <span data-ttu-id="19dc3-120">Ändern Sie den Timeout Zeitraum und die Anzahl der Wiederholungswerte in der Datenbank der Implementierung.</span><span class="sxs-lookup"><span data-stu-id="19dc3-120">Modify the time-out period and retry count values in the implementation's database.</span></span> <span data-ttu-id="19dc3-121">Weitere Informationen finden Sie unter [Ändern der Richtlinie für Neuübertragungen](changing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="19dc3-121">For more information, see [Changing the Retransmission Policy](changing-the-retransmission-policy.md).</span></span>
-   <span data-ttu-id="19dc3-122">Rufen Sie die [**snmpcancelmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) -Funktion auf, um den Neuübertragungs Zyklen abzubrechen und interne Datenstrukturen freizugeben, die einer einzelnen SNMP-Nachrichten Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="19dc3-122">Call the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function to cancel the retransmission cycle and release internal data structures associated with a single SNMP message request.</span></span> <span data-ttu-id="19dc3-123">Weitere Informationen finden Sie unter [Abbrechen der erneuten Übertragung](canceling-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="19dc3-123">For more information, see [Canceling Retransmission](canceling-retransmission.md).</span></span>

<span data-ttu-id="19dc3-124">Die Anwendung kann Ihre eigene Neuübertragungs Richtlinie ausführen.</span><span class="sxs-lookup"><span data-stu-id="19dc3-124">The application can execute its own retransmission policy.</span></span> <span data-ttu-id="19dc3-125">In diesem Fall basiert die Ausführung möglicherweise auf den Werten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="19dc3-125">In this case, execution may or may not be based on the values in the database.</span></span>

 

 




