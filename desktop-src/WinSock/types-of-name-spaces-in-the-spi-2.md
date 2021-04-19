---
description: Die drei Typen von Namespaces im Windows Sockets (Winsock) SPI enthalten dynamische, statische und persistente Namespaces.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Typen von Namespaces in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368933"
---
# <a name="types-of-namespaces-in-the-spi"></a><span data-ttu-id="1271a-103">Typen von Namespaces in der SPI</span><span class="sxs-lookup"><span data-stu-id="1271a-103">Types of Namespaces in the SPI</span></span>

<span data-ttu-id="1271a-104">Es gibt drei verschiedene Typen von Namespaces, in denen ein Dienst registriert werden kann:</span><span class="sxs-lookup"><span data-stu-id="1271a-104">There are three different types of namespaces in which a service could be registered:</span></span>

-   <span data-ttu-id="1271a-105">Dynamisch</span><span class="sxs-lookup"><span data-stu-id="1271a-105">Dynamic</span></span>
-   <span data-ttu-id="1271a-106">statischen</span><span class="sxs-lookup"><span data-stu-id="1271a-106">Static</span></span>
-   <span data-ttu-id="1271a-107">Beständig</span><span class="sxs-lookup"><span data-stu-id="1271a-107">Persistent</span></span>

<span data-ttu-id="1271a-108">Mithilfe dynamischer Namespaces können Dienste bei Bedarf beim Namespace registriert werden, und Clients können die verfügbaren Dienste zur Laufzeit ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1271a-108">Dynamic namespaces allow services to register with the namespace on the fly, and for clients to discover the available services at run time.</span></span> <span data-ttu-id="1271a-109">Dynamische Namespaces basieren häufig auf Übertragungen, um die fortgesetzte Verfügbarkeit eines Netzwerk Dienstanbieter anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1271a-109">Dynamic namespaces frequently rely on broadcasts to indicate the continued availability of a network service.</span></span> <span data-ttu-id="1271a-110">Beispiele für dynamische Namespaces sind der SAP-Namespace, der in einer NetWare-Umgebung verwendet wird, und der NBP-Namespace, der von AppleTalk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1271a-110">Examples of dynamic namespaces include the SAP namespace used within a NetWare environment and the NBP namespace used by AppleTalk.</span></span>

<span data-ttu-id="1271a-111">Statische Namespaces erfordern, dass alle Dienste vorab registriert werden, d. h. wenn der Namespace erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1271a-111">Static namespaces require all of the services to be registered ahead of time, that is, when the namespace is created.</span></span> <span data-ttu-id="1271a-112">Der DNS ist ein Beispiel für einen statischen Namespace.</span><span class="sxs-lookup"><span data-stu-id="1271a-112">The DNS is an example of a static namespace.</span></span> <span data-ttu-id="1271a-113">Obwohl es eine programmgesteuerte Methode zum Auflösen von Namen gibt, gibt es keine programmgesteuerte Methode zum Registrieren von Namen.</span><span class="sxs-lookup"><span data-stu-id="1271a-113">Although there is a programmatic way to resolve names, there is no programmatic way to register names.</span></span>

<span data-ttu-id="1271a-114">Persistente Namespaces ermöglichen es Diensten, sich dynamisch bei dem Namespace zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="1271a-114">Persistent namespaces allow services to register with the namespace on the fly.</span></span> <span data-ttu-id="1271a-115">Im Gegensatz zu dynamischen Namespaces behalten persistente Namespaces jedoch die Registrierungsinformationen im nicht flüchtigen Speicher bei, wo Sie bis zu dem Zeitpunkt verbleibt, an dem der Dienst die Entfernung anfordert.</span><span class="sxs-lookup"><span data-stu-id="1271a-115">Unlike dynamic namespaces however, persistent namespaces retain the registration information in nonvolatile storage where it remains until such time as the service requests that it be removed.</span></span> <span data-ttu-id="1271a-116">Persistente Namespaces werden durch Verzeichnisdienste wie z. b. X. 500 und den NDS (NetWare-Verzeichnisdienst) typisierten.</span><span class="sxs-lookup"><span data-stu-id="1271a-116">Persistent namespaces are typified by directory services such as X.500 and the NDS (NetWare Directory Service).</span></span> <span data-ttu-id="1271a-117">Diese Umgebungen ermöglichen das Hinzufügen, löschen und Ändern von Dienst Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1271a-117">These environments allow the adding, deleting, and modification of service properties.</span></span> <span data-ttu-id="1271a-118">Außerdem kann das Dienst Objekt, das den Dienst im Verzeichnisdienst darstellt, über eine Vielzahl von Attributen verfügen, die mit dem Dienst verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1271a-118">In addition, the service object representing the service within the directory service could have a variety of attributes associated with the service.</span></span> <span data-ttu-id="1271a-119">Das wichtigste Attribut für Client Anwendungen sind die Adressierungs Informationen des dienstanders.</span><span class="sxs-lookup"><span data-stu-id="1271a-119">The most important attribute for client applications is the service's addressing information.</span></span>

 

 



