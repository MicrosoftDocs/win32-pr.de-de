---
description: Eine der wichtigsten Aufgaben eines Datentransport Dienstanbieters besteht darin, dem Client Hinweise zu geben, wenn bestimmte Netzwerkereignisse aufgetreten sind.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Benachrichtigung über Netzwerkereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862548"
---
# <a name="notification-of-network-events"></a><span data-ttu-id="10d0f-103">Benachrichtigung über Netzwerkereignisse</span><span class="sxs-lookup"><span data-stu-id="10d0f-103">Notification of Network Events</span></span>

<span data-ttu-id="10d0f-104">Eine der wichtigsten Aufgaben eines Datentransport Dienstanbieters besteht darin, dem Client Hinweise zu geben, wenn bestimmte Netzwerkereignisse aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="10d0f-104">One of the most important responsibilities of a data transport service provider is that of providing indications to the client when certain network events have occurred.</span></span> <span data-ttu-id="10d0f-105">Die Liste der definierten Netzwerkereignisse besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="10d0f-105">The list of defined network events consists of the following:</span></span>

-   <span data-ttu-id="10d0f-106">**FD \_ Connect**– eine Verbindung mit einem Remote Host oder einer Multicast Sitzung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="10d0f-106">**FD\_CONNECT**— A connection to a remote host or to a multicast session has been completed.</span></span>
-   <span data-ttu-id="10d0f-107">**FD \_ Accept**– ein Remote Host stellt eine Verbindungsanforderung her.</span><span class="sxs-lookup"><span data-stu-id="10d0f-107">**FD\_ACCEPT**— A remote host is making a connection request.</span></span>
-   <span data-ttu-id="10d0f-108">**FD \_ Read**– die Netzwerkdaten sind eingetroffen und können gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="10d0f-108">**FD\_READ**— Network data has arrived which is available to be read.</span></span>
-   <span data-ttu-id="10d0f-109">**FD \_ Write**– Space steht in den Puffer des Dienstanbieters zur Verfügung, sodass jetzt zusätzliche Daten gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="10d0f-109">**FD\_WRITE**— Space has become available in the service provider's buffers so that additional data may now be sent.</span></span>
-   <span data-ttu-id="10d0f-110">**FD \_ OOB**– out-of-Band-Daten sind zum Lesen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10d0f-110">**FD\_OOB**— Out of band data is available to be read.</span></span>
-   <span data-ttu-id="10d0f-111">**FD \_ Close**– der Remote Host hat die Verbindung geschlossen.</span><span class="sxs-lookup"><span data-stu-id="10d0f-111">**FD\_CLOSE**— The remote host has closed down the connection.</span></span>
-   <span data-ttu-id="10d0f-112">**FD \_ QoS**– bei ausgehandelten QoS-Ebenen ist eine Änderung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="10d0f-112">**FD\_QOS**— A change has occurred in negotiated QoS levels.</span></span>
-   <span data-ttu-id="10d0f-113">**FD \_ Gruppen- \_ QoS**– reserviert.</span><span class="sxs-lookup"><span data-stu-id="10d0f-113">**FD\_GROUP\_QOS**— Reserved.</span></span>
-   <span data-ttu-id="10d0f-114">**FD \_ Routing \_ Schnittstellen \_ Änderung**– eine lokale Schnittstelle, die verwendet werden soll, um das in der " **SIO \_ Routing \_ Interface \_ Change ioctl** " angegebene Ziel zu erreichen, hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="10d0f-114">**FD\_ROUTING\_INTERFACE\_CHANGE**— A local interface that should be used to reach the destination specified in **SIO\_ROUTING\_INTERFACE\_CHANGE IOCTL** has changed.</span></span>
-   <span data-ttu-id="10d0f-115">**FD \_ Adress \_ Listen \_ Änderung**– die Liste der lokalen Adressen, an die die Anwendung gebunden werden kann, wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="10d0f-115">**FD\_ADDRESS\_LIST\_CHANGE**— The list of local addresses to which application can bind has changed.</span></span>

<span data-ttu-id="10d0f-116">Der oben aufgeführte Satz von Netzwerk Ereignissen wird mitunter als **FD \_ xxx** -Ereignisse bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="10d0f-116">The set of network events enumerated above is sometimes referred to as the **FD\_XXX** events.</span></span> <span data-ttu-id="10d0f-117">Je nachdem, wie der Client eine Benachrichtigung anfordert, kann ein oder mehrere dieser Netzwerkereignisse auf verschiedene Weise angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="10d0f-117">Indication of the occurrence of one or more of such network events may be given in a number of ways depending on how the client requests notification.</span></span>

 

 



