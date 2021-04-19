---
description: Der Netzwerkmonitor Binary Large Object (BLOB) ist eine generische Datenstruktur, die Konfigurations-und Speicherort Informationen von Netzwerkschnittstellenkarten (NICs) enthält.
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: BlobNetzwerkmonitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354029"
---
# <a name="network-monitor-blobs"></a><span data-ttu-id="6b957-103">BlobNetzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="6b957-103">Network Monitor BLOBs</span></span>

<span data-ttu-id="6b957-104">Der Netzwerkmonitor Binary Large Object (BLOB) ist eine generische Datenstruktur, die Konfigurations-und Speicherort Informationen von Netzwerkschnittstellenkarten (NICs) enthält.</span><span class="sxs-lookup"><span data-stu-id="6b957-104">The Network Monitor binary large object (BLOB) is a generic data structure that contains configuration and location information of network interface cards (NICs).</span></span> <span data-ttu-id="6b957-105">Verwenden Sie blobfunktionen zum Darstellen von NICs und zum Filtern von Einträgen in einer Liste von NICs.</span><span class="sxs-lookup"><span data-stu-id="6b957-105">Use BLOBs to represent NICs and to filter entries in a list of NICs.</span></span> <span data-ttu-id="6b957-106">Blobdaten können auch anwendungsspezifische Daten enthalten, ohne dass sich dies auf die anderen Daten auswirkt, die Sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b957-106">BLOBS can also contain application-specific data without affecting the other data that they hold.</span></span> <span data-ttu-id="6b957-107">Die BLOB-Implementierung ist für alle Ebenen, die auf BLOBs mit BLOB-APIs zugreifen müssen, nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="6b957-107">BLOB implementation is opaque to all levels that must access BLOBs with BLOB APIs.</span></span>

## <a name="blob-structure"></a><span data-ttu-id="6b957-108">BLOB-Struktur</span><span class="sxs-lookup"><span data-stu-id="6b957-108">BLOB Structure</span></span>

<span data-ttu-id="6b957-109">Ein BLOB kann als hierarchische Struktur angesehen werden, die zum Festlegen von Zeichen folgen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b957-109">A BLOB can be considered as a hierarchical tree used to designate strings.</span></span> <span data-ttu-id="6b957-110">Diese Struktur verfügt über drei Ebenen: "Owner", "Category" und "Tag".</span><span class="sxs-lookup"><span data-stu-id="6b957-110">This tree has three layers: Owner, Category, and Tag.</span></span> <span data-ttu-id="6b957-111">Owner ist eine Zeichenfolge, die im allgemeinen angibt, wer einen Eintrag liest.</span><span class="sxs-lookup"><span data-stu-id="6b957-111">Owner is a string that indicates, in general, who reads an entry.</span></span> <span data-ttu-id="6b957-112">Die Kategorie ist auch eine Zeichenfolge, die eine allgemeine funktionale Gruppierung von Tags unter dem Besitzer angibt.</span><span class="sxs-lookup"><span data-stu-id="6b957-112">The Category is also a string, which designates a general functional grouping of tags under the owner.</span></span> <span data-ttu-id="6b957-113">Das-Tag ist der tatsächliche Name des Eintrags.</span><span class="sxs-lookup"><span data-stu-id="6b957-113">The Tag is the actual name of the entry.</span></span>

<span data-ttu-id="6b957-114">Zu den strukturellen Merkmalen von blobden zählen folgende:</span><span class="sxs-lookup"><span data-stu-id="6b957-114">The structural characteristics of BLOBs include:</span></span>

-   <span data-ttu-id="6b957-115">BLOB-Hilfsprogramme innerhalb eines Prozesses werden von einem in jedem BLOB integrierten Mutex voneinander geschützt.</span><span class="sxs-lookup"><span data-stu-id="6b957-115">BLOB helpers within one process are protected from one another by a mutex built into each BLOB.</span></span>
-   <span data-ttu-id="6b957-116">Jedes BLOB verfügt über eine interne Versionsnummer, sodass die Hilfsprogramme sowohl das vorhandene als auch das zukünftige BLOB-Formular verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="6b957-116">Each BLOB has an internal version number so that the helpers can handle both present and future BLOB forms.</span></span> <span data-ttu-id="6b957-117">Versions Konflikte können auftreten, wenn Sie ein BLOB über einen Remote Prozedur Rückruf an einen anderen Computer senden.</span><span class="sxs-lookup"><span data-stu-id="6b957-117">Version conflicts may occur if you send a BLOB to another computer via a remote procedure call.</span></span>
-   <span data-ttu-id="6b957-118">Das BLOB selbst ist ein Zeiger auf eine leere.</span><span class="sxs-lookup"><span data-stu-id="6b957-118">The BLOB itself is a pointer to a void.</span></span> <span data-ttu-id="6b957-119">Beachten Sie, dass Anwendungen dem **Konstanten** -Modifizierer blobzuordnungen zuordnen sollten, um zu vermeiden, dass der Inhalt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6b957-119">Be aware that applications should allocate BLOBs with the **const** modifier to avoid altering the contents.</span></span>
-   <span data-ttu-id="6b957-120">Jeder der Kenn Zeichner und ihre Werte sind Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="6b957-120">Each of the designators, as well as their values, are strings.</span></span> <span data-ttu-id="6b957-121">Beachten Sie, dass die von **GetString** -Funktionen zurückgegebenen Zeichen folgen tatsächlich Zeiger auf das BLOB sind und nicht geändert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="6b957-121">Be aware that the strings returned by **GetString** functions are actually pointers into the BLOB and should not be changed.</span></span> <span data-ttu-id="6b957-122">Aus diesem Grund müssen diese Zeichen folgen als "Konstante **char** _ px \*" angegeben werden \_ , damit Anwendungen nicht versehentlich geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6b957-122">For this reason, these strings must be specified as **const char** _\_pX\* to keep applications from accidentally changing them.</span></span>

<span data-ttu-id="6b957-123">Im Allgemeinen wird der Aufrufer von allen Parametern mit dem Konstanten Kenn Zeichner ermutigt, das Ändern der Werte zu unterbinden, anstatt zu verhindern, dass die **Hilfsfunktionen** diese ändern.</span><span class="sxs-lookup"><span data-stu-id="6b957-123">In general, all parameters with the **const** designator encourage the caller to refrain from changing the values rather than prohibit the helper functions from changing them.</span></span> <span data-ttu-id="6b957-124">Tatsächlich ändern die Hilfsfunktionen diese Werte in der Regel.</span><span class="sxs-lookup"><span data-stu-id="6b957-124">In fact, the helper functions will usually change those values.</span></span>

 

 



