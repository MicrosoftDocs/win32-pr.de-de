---
description: Datensätze sind eine Möglichkeit für die Kommunikation zwischen Knoten in einem Diagramm oder Mitgliedern einer Gruppe.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Datensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960262"
---
# <a name="records"></a><span data-ttu-id="555e9-103">Datensätze</span><span class="sxs-lookup"><span data-stu-id="555e9-103">Records</span></span>

<span data-ttu-id="555e9-104">Datensätze sind eine Möglichkeit für die Kommunikation zwischen Knoten in einem Diagramm oder Mitgliedern einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="555e9-104">Records are a way to communicate between nodes in a graph or members in a group.</span></span> <span data-ttu-id="555e9-105">Ein Datensatz besteht aus den folgenden zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="555e9-105">A record consists of the following two parts:</span></span>

-   <span data-ttu-id="555e9-106">Datensatz-Header</span><span class="sxs-lookup"><span data-stu-id="555e9-106">Record header</span></span>
-   <span data-ttu-id="555e9-107">Spezifischer undurchsichtiger Dateninhalt</span><span class="sxs-lookup"><span data-stu-id="555e9-107">Specific opaque data content</span></span>

<span data-ttu-id="555e9-108">Der-Header enthält Informationen zum Datensatz, einschließlich der Version, des Erstellers und der Art der Daten, die veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="555e9-108">The header contains information about the record, including the version, creator, and type of data being published.</span></span> <span data-ttu-id="555e9-109">Der Header enthält auch ein XML-Attribut Feld, das Anwendungen das Hinzufügen von Name-Wert-Attributen, die die Daten beschreiben, sowie das effiziente Durchsuchen der datensatzdatenbank nach bestimmten Datensätzen ermöglicht, die zuvor veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="555e9-109">The header also contains an XML attributes field that allows applications to add name-value attributes that describe the data, and to efficiently search the record database for specific records that have previously been published.</span></span> <span data-ttu-id="555e9-110">Der Inhalt ist die Anwendungs definierte Daten, die für die Peer Infrastruktur nicht transparent sind.</span><span class="sxs-lookup"><span data-stu-id="555e9-110">The content is the application-defined data, and is opaque to the Peer Infrastructure.</span></span>

<span data-ttu-id="555e9-111">Wenn ein Datensatz veröffentlicht wird, werden er (sowohl Header als auch Daten) im Diagramm oder in der Gruppe überflutet.</span><span class="sxs-lookup"><span data-stu-id="555e9-111">When a record is published, it (both header and data) is flooded throughout the graph or group.</span></span> <span data-ttu-id="555e9-112">Synchronisierte Peers erhalten diese Daten und speichern Sie in einer lokalen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="555e9-112">Synchronized peers receive this data and store it in a local database.</span></span> <span data-ttu-id="555e9-113">Nicht synchronisierte und Offline-Peers erhalten die Daten beim nächsten Herstellen einer Verbindung und Synchronisieren mit dem Peer Diagramm oder der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="555e9-113">Unsynchronized and offline peers receive the data the next time they connect and synchronize with the peer graph or group.</span></span>

<span data-ttu-id="555e9-114">Weitere Informationen zum Arbeiten mit Datensätzen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="555e9-114">For information about working with records, see the following topics:</span></span>

-   [<span data-ttu-id="555e9-115">Daten Satz Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="555e9-115">Record Dependencies</span></span>](record-dependencies.md)
-   [<span data-ttu-id="555e9-116">Daten Satz Verwaltung</span><span class="sxs-lookup"><span data-stu-id="555e9-116">Record Management</span></span>](record-management.md)
-   [<span data-ttu-id="555e9-117">Attribut Schema aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="555e9-117">Record Attribute Schema</span></span>](record-attribute-schema.md)
-   [<span data-ttu-id="555e9-118">Suchabfrage Format aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="555e9-118">Record Search Query Format</span></span>](record-search-query-format.md)

 

 



