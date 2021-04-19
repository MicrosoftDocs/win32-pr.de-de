---
description: Glossar der Netzwerkmonitor Begriffe, die mit dem Buchstaben C beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373025"
---
# <a name="c-network-monitor"></a><span data-ttu-id="4b49e-103">C (Netzwerkmonitor)</span><span class="sxs-lookup"><span data-stu-id="4b49e-103">C (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="4b49e-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**einver**</span><span class="sxs-lookup"><span data-stu-id="4b49e-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**capture**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-105">Netzwerkverkehrs Daten, die in Frames gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="4b49e-105">Network traffic data that is collected in frames.</span></span> <span data-ttu-id="4b49e-106">Ein Netzwerk Paketanbieter (NPP) führt eine Erfassung aus.</span><span class="sxs-lookup"><span data-stu-id="4b49e-106">A network packet provider (NPP) performs a capture.</span></span> <span data-ttu-id="4b49e-107">Siehe auch [*verzögerte Erfassung*](d.md)und *echt Zeiterfassung*</span><span class="sxs-lookup"><span data-stu-id="4b49e-107">See also [*delayed capture*](d.md), and *real-time capture*</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**Erfassungs Datei**</span><span class="sxs-lookup"><span data-stu-id="4b49e-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**capture file**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-109">Eine Datei, die Netzwerkmonitor erstellt, um erfasste Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4b49e-109">A file that Network Monitor creates to store captured data.</span></span> <span data-ttu-id="4b49e-110">Die Dateinamenerweiterung. Cap identifiziert eine Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="4b49e-110">The .cap file name extension identifies a capture file.</span></span> <span data-ttu-id="4b49e-111">Netzwerkmonitor generiert nach dem Zufallsprinzip einen Aufzeichnungs Dateinamen, aber Sie können den Dateinamen ändern, wenn Sie die Erfassungs Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="4b49e-111">Network Monitor randomly generates a capture file name, but you can change the file name when you save the capture file.</span></span>

<span data-ttu-id="4b49e-112">Netzwerkmonitor erstellt jedes Mal, wenn der Aufzeichnungsprozess startet, eine Erfassungs Datei und speichert die Datei dann während des Erfassungs Vorgangs geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4b49e-112">Network Monitor creates a capture file each time the capture process starts, and then keeps the file open during the capture process.</span></span> <span data-ttu-id="4b49e-113">Der Zugriff auf den Inhalt einer Erfassungs Datei ist erst möglich, nachdem der Aufzeichnungsprozess beendet und die Aufzeichnungsdatei geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4b49e-113">You cannot access the contents of a capture file until the capture process is stopped and the capture file is closed.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**Erfassungs Filter**</span><span class="sxs-lookup"><span data-stu-id="4b49e-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**capture filter**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-115">Eine Reihe von Netzwerkmonitor Funktionen, die verwendet werden, um eingehende Frames einzuschränken, die von einer Netzwerk Paketanbieter-Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b49e-115">A set of Network Monitor functions used to restrict incoming frames that a network packet provider (NPP) application uses.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**Erfassungs-**</span><span class="sxs-lookup"><span data-stu-id="4b49e-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**capture trigger**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-117">Ein Auslöserereignis, das festgelegt wird, um den Aufzeichnungsprozess zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4b49e-117">A trigger event that is set to stop the capture process.</span></span> <span data-ttu-id="4b49e-118">Das Erfassungs Auslöserereignis kann eine temporäre Erfassungs Datei sein, die an eine bestimmte Ebene oder ein bestimmtes Datenmuster weitergeleitet wird, das in einem aufgezeichneten Frame auftritt.</span><span class="sxs-lookup"><span data-stu-id="4b49e-118">The capture trigger event can be a temporary capture file that is directed to a specific level or data pattern that occurs in a captured frame.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**erfasste Daten**</span><span class="sxs-lookup"><span data-stu-id="4b49e-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**captured data**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-120">Frames, die über einen definierten Satz von Kriterien verfügen.</span><span class="sxs-lookup"><span data-stu-id="4b49e-120">Frames that have a defined set of criteria.</span></span> <span data-ttu-id="4b49e-121">Die Datenrahmen sind in einer temporären Erfassungs Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="4b49e-121">The data frames are contained in a temporary capture file.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**Konversations Statistik**</span><span class="sxs-lookup"><span data-stu-id="4b49e-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**conversation statistics**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-123">Statistik von Netzwerk Datenverkehr, die während einer Erfassung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="4b49e-123">Statistics of network traffic saved during a capture.</span></span> <span data-ttu-id="4b49e-124">Diese Statistiken enthalten Stations-und Sitzungsinformationen, beginnend beim Start des Aufzeichnungsprozesses und beenden, wenn die Erfassung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="4b49e-124">These statistics include station and session information beginning when the capture process starts, and ending when the capture stops.</span></span> <span data-ttu-id="4b49e-125">Wenn Sie den Aufzeichnungsprozess anhalten, werden Netzwerkmonitor weiterhin Statistiken hinzufügen, wenn Sie den Prozess fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="4b49e-125">If you pause the capture process, Network Monitor continues to add statistics when you resume the process.</span></span> <span data-ttu-id="4b49e-126">Um Konversations Statistiken abzurufen, rufen Sie die **getconversation ationstatistics** -Methode für die verwendete Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="4b49e-126">To retrieve conversation statistics, call the **GetConversationStatistics** method for the interface you are using.</span></span>

</dd> </dl>

 

 



