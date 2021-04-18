---
description: Glossar der Netzwerkmonitor Begriffe, die mit dem Buchstaben F beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 6e6b85cc-83bc-4468-b1cf-3480022a8f12
title: F (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605eb27b95526fa2f3839c06e6f259a2afec55c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345482"
---
# <a name="f-network-monitor"></a><span data-ttu-id="c8ca2-103">F (Netzwerkmonitor)</span><span class="sxs-lookup"><span data-stu-id="c8ca2-103">F (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="c8ca2-104"><span id="_netmon_filter_blob_gly"></span><span id="_NETMON_FILTER_BLOB_GLY"></span>**filterblob**</span><span class="sxs-lookup"><span data-stu-id="c8ca2-104"><span id="_netmon_filter_blob_gly"></span><span id="_NETMON_FILTER_BLOB_GLY"></span>**filter BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="c8ca2-105">BLOB (Binary Large Object), das verwendet wird, um die Suche nach einer Netzwerkschnittstellenkarte (NIC) einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-105">Binary large object (BLOB) used to restrict the search for a network interface card (NIC).</span></span> <span data-ttu-id="c8ca2-106">Jeder Eintrag im filterblob muss mit einem entsprechenden Eintrag im NPP-BLOB (Network Packet Provider) übereinstimmen, der die NIC darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-106">Each entry in the filter BLOB must match an equivalent entry in the network packet provider (NPP) BLOB that represents the NIC.</span></span> <span data-ttu-id="c8ca2-107">Beispielsweise kann eine Anwendung nur Ethernet-Karten oder Karten anfordern, die eine bestimmte Framerate unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-107">For example, an application can request only Ethernet cards, or cards that support a specific frame rate.</span></span> <span data-ttu-id="c8ca2-108">Mit einem filterblob können Sie die Funktionen **getnppblobfromui** und **getnppblobtable** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-108">You can use a filter BLOB to call the **GetNPPBlobFromUI** and **GetNPPBlobTable** functions.</span></span>

</dd> <dt>

<span data-ttu-id="c8ca2-109"><span id="_netmon_follow_set_gly"></span><span id="_NETMON_FOLLOW_SET_GLY"></span>**Folgen Satz**</span><span class="sxs-lookup"><span data-stu-id="c8ca2-109"><span id="_netmon_follow_set_gly"></span><span id="_NETMON_FOLLOW_SET_GLY"></span>**follow set**</span></span>
</dt> <dd>

<span data-ttu-id="c8ca2-110">Ein Protokoll Satz, der einem Protokoll folgt.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-110">A protocol set that follows a protocol.</span></span> <span data-ttu-id="c8ca2-111">Netzwerkmonitor verwendet den folgenden Satz eines Protokolls, wenn der Parser das nächste Protokoll aus den Daten in der Erfassung nicht erkennen kann.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-111">Network Monitor uses the follow set of a protocol if the parser cannot detect the next protocol from the data in the capture.</span></span> <span data-ttu-id="c8ca2-112">Siehe auch [ *Übergabe festlegen*](h.md)</span><span class="sxs-lookup"><span data-stu-id="c8ca2-112">See also [*handoff set*](h.md)</span></span>

</dd> <dt>

<span data-ttu-id="c8ca2-113"><span id="_netmon_frame_gly"></span><span id="_NETMON_FRAME_GLY"></span>**Dr**</span><span class="sxs-lookup"><span data-stu-id="c8ca2-113"><span id="_netmon_frame_gly"></span><span id="_NETMON_FRAME_GLY"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="c8ca2-114">Ein Datenpaket, das als eine Einheit über ein Netzwerk übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-114">A packet of data that is transmitted as one unit over a network.</span></span> <span data-ttu-id="c8ca2-115">Jeder Frame folgt der gleichen grundlegenden Organisation und enthält Steuerungsinformationen wie z. b. das Synchronisieren von Zeichen, Stations Adressen, einen Fehler Überprüfungs Wert und eine Variable Datenmenge.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-115">Each frame follows the same basic organization, and contains control information such as synchronizing characters, station addresses, an error-checking value, and a variable amount of data.</span></span> <span data-ttu-id="c8ca2-116">Wird auch als Paket bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-116">Also called a packet.</span></span>

</dd> <dt>

<span data-ttu-id="c8ca2-117"><span id="_netmon_frame_viewer_window_gly"></span><span id="_NETMON_FRAME_VIEWER_WINDOW_GLY"></span>**Frame-Viewer-Fenster**</span><span class="sxs-lookup"><span data-stu-id="c8ca2-117"><span id="_netmon_frame_viewer_window_gly"></span><span id="_NETMON_FRAME_VIEWER_WINDOW_GLY"></span>**frame viewer window**</span></span>
</dt> <dd>

<span data-ttu-id="c8ca2-118">Ein Netzwerkmonitor Fenster, in dem ausführliche Informationen zu einzelnen Frames angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-118">A Network Monitor window that displays detailed information about individual frames.</span></span> <span data-ttu-id="c8ca2-119">Sie können mehrere Frame Viewer-Fenster gleichzeitig öffnen.</span><span class="sxs-lookup"><span data-stu-id="c8ca2-119">You can open several frame viewer windows at one time.</span></span>

</dd> </dl>

 

 



