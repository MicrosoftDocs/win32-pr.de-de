---
description: Netzwerkmonitor verwendet drei Typen von BLOB (Binary Large Objects) zum auswählen und Verbinden von Netzwerkschnittstellenkarten (NICs), zum Erfassen von Daten und zum Bearbeiten von NPP-Daten.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: BLOB-Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218334"
---
# <a name="blob-types"></a><span data-ttu-id="cf020-103">BLOB-Typen</span><span class="sxs-lookup"><span data-stu-id="cf020-103">BLOB Types</span></span>

<span data-ttu-id="cf020-104">Netzwerkmonitor verwendet drei Typen von BLOB (Binary Large Objects) zum auswählen und Verbinden von Netzwerkschnittstellenkarten (NICs), zum Erfassen von Daten und zum Bearbeiten von NPP-Daten.</span><span class="sxs-lookup"><span data-stu-id="cf020-104">Network Monitor uses three types of binary large objects (BLOBs) to select and connect network interface cards (NICs), capture data, and manipulate NPP data.</span></span>

## <a name="npp-blob"></a><span data-ttu-id="cf020-105">NPP-BLOB</span><span class="sxs-lookup"><span data-stu-id="cf020-105">NPP BLOB</span></span>

<span data-ttu-id="cf020-106">Anwendungen verwenden NPP-blobfunktionen, um über eine NPP eine Verbindung mit einer bestimmten NIC herzustellen.</span><span class="sxs-lookup"><span data-stu-id="cf020-106">Applications use NPP BLOBs to connect to a specific NIC through an NPP.</span></span> <span data-ttu-id="cf020-107">(Die Anwendung stellt die Verbindung mit einem aufzurufenden Aufrufen von " **anatenppinterface** " und Standortdaten im NPP-BLOB her.) Eine Anwendung kann Ihre Konfigurationsdaten auch im NPP-BLOB speichern, um den NPP zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cf020-107">(The application makes the connection with a call to **CreateNPPInterface** and location data in the NPP BLOB.) An application can also store its configuration data in the NPP BLOB to configure the NPP.</span></span> <span data-ttu-id="cf020-108">Außerdem ist es nicht erforderlich, dass eine Anwendung, die das NPP-BLOB speichert, den Finder durchläuft, um das BLOB wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="cf020-108">Also, an application that saves its NPP BLOB is not required to go through the Finder to reuse that BLOB.</span></span>

## <a name="filter-blob"></a><span data-ttu-id="cf020-109">Filterblob</span><span class="sxs-lookup"><span data-stu-id="cf020-109">Filter BLOB</span></span>

<span data-ttu-id="cf020-110">Ein filterblob enthält Anwendungs definierte Kriterien, die Sie verwenden können, um eine NPP und eine NIC auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cf020-110">A filter BLOB contains application-defined criteria that you can use to select an NPP and a NIC.</span></span> <span data-ttu-id="cf020-111">Beispielsweise kann eine Anwendung eine bestimmte NIC, nur Ethernet-Karten oder Karten anfordern, die eine bestimmte Frame Erfassungs Rate unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cf020-111">For example, an application can request a specific NIC, only Ethernet cards, or cards that support a specific frame capture rate.</span></span>

## <a name="special-blob"></a><span data-ttu-id="cf020-112">Spezielles BLOB</span><span class="sxs-lookup"><span data-stu-id="cf020-112">Special BLOB</span></span>

<span data-ttu-id="cf020-113">Wenn ein NPP zusätzliche Daten benötigt, bevor er ein NPP-BLOB an eine Anwendung zurückgeben kann, verwendet der NPP ein spezielles BLOB.</span><span class="sxs-lookup"><span data-stu-id="cf020-113">When an NPP requires additional data before it can return an NPP BLOB to an application, the NPP uses a special BLOB.</span></span> <span data-ttu-id="cf020-114">In den meisten Fällen benötigt die Anwendung keine speziellen blobwerte, sodass Sie nicht an eine Anwendung zurückgegeben werden, es sei denn, ein bestimmtes Flag wird in einem Funktions Aufrufsatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf020-114">Most often, the application will not need or use special BLOBs so they are not returned to an application unless a specific flag is set in one function call.</span></span> <span data-ttu-id="cf020-115">Ein Remote-NPP verwendet beispielsweise ein spezielles BLOB, da zum Herstellen einer Verbindung ein Pfadname erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cf020-115">For example, a remote NPP uses a special BLOB because a path name is required to make a connection.</span></span> <span data-ttu-id="cf020-116">Eine Anwendung, die ein Remote-NPP-spezielles BLOB empfängt, kann die Zeichenfolge hinzufügen und zum Finder zurückkehren, um eine NPP-BLOB-Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cf020-116">An application that receives a remote NPP special BLOB could add the string and call back into the Finder to get an NPP BLOB table.</span></span> <span data-ttu-id="cf020-117">Weitere Informationen finden Sie unter [Special BLOB Entries](special-blob-entries.md).</span><span class="sxs-lookup"><span data-stu-id="cf020-117">For more information, see [Special BLOB Entries](special-blob-entries.md).</span></span>

 

 



