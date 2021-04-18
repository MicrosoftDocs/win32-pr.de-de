---
description: Senden von COPP-Befehlen
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Senden von COPP-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345393"
---
# <a name="sending-copp-commands"></a><span data-ttu-id="f2b46-103">Senden von COPP-Befehlen</span><span class="sxs-lookup"><span data-stu-id="f2b46-103">Sending COPP Commands</span></span>

<span data-ttu-id="f2b46-104">Um einen zertifizierten Befehl für das Ausgabe Schutz Protokoll (COPP) zu senden, füllen Sie die [**amcoppcommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) -Struktur wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="f2b46-104">To send a Certified Output Protection Protocol (COPP) command, fill in an [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) structure as follows:</span></span>

-   <span data-ttu-id="f2b46-105">**guidcommandid**.</span><span class="sxs-lookup"><span data-stu-id="f2b46-105">**guidCommandID**.</span></span> <span data-ttu-id="f2b46-106">Die GUID, die den Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f2b46-106">The GUID that identifies the command.</span></span> <span data-ttu-id="f2b46-107">Weitere Informationen finden Sie in der COPP-Befehlsreferenz.</span><span class="sxs-lookup"><span data-stu-id="f2b46-107">See the COPP Command Reference.</span></span>
-   <span data-ttu-id="f2b46-108">**dwsequence**.</span><span class="sxs-lookup"><span data-stu-id="f2b46-108">**dwSequence**.</span></span> <span data-ttu-id="f2b46-109">Die Sequenznummer des Befehls.</span><span class="sxs-lookup"><span data-stu-id="f2b46-109">The command sequence number.</span></span> <span data-ttu-id="f2b46-110">Erhöhen Sie diesen Wert nach jedem Befehl.</span><span class="sxs-lookup"><span data-stu-id="f2b46-110">Increment this value after each command.</span></span> <span data-ttu-id="f2b46-111">(Dieser Wert wird als **ucommandabq** in [Initiieren einer COPP-Sitzung](initiating-a-copp-session.md)angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="f2b46-111">(This value is shown as **uCommandSeq** in [Initiating a COPP Session](initiating-a-copp-session.md).)</span></span>
-   <span data-ttu-id="f2b46-112">**cbsizedata**.</span><span class="sxs-lookup"><span data-stu-id="f2b46-112">**cbSizeData**.</span></span> <span data-ttu-id="f2b46-113">Die Größe (in Bytes) der Daten, die für den Befehl erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f2b46-113">The size, in bytes, of any data needed for the command.</span></span>
-   <span data-ttu-id="f2b46-114">**Commanddata**.</span><span class="sxs-lookup"><span data-stu-id="f2b46-114">**CommandData**.</span></span> <span data-ttu-id="f2b46-115">Daten für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="f2b46-115">Data for the command.</span></span>

<span data-ttu-id="f2b46-116">Nachdem Sie diese Daten ausgefüllt haben, berechnen Sie den Mac für den Befehl:</span><span class="sxs-lookup"><span data-stu-id="f2b46-116">After you have filled in this data, calculate the MAC for the command:</span></span>

1.  <span data-ttu-id="f2b46-117">Berechnen Sie das OMAC-1-Tag für den Datenblock, der nach dem **mackdi** -Member der **amcoppcommand** -Struktur angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f2b46-117">Calculate the OMAC-1 tag for the block of data that appears after the **macKDI** member of the **AMCOPPCommand** structure.</span></span>
2.  <span data-ttu-id="f2b46-118">Kopieren Sie diesen Wert in den **mackdi** -Member der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="f2b46-118">Copy this value into the **macKDI** member of the structure.</span></span>

<span data-ttu-id="f2b46-119">Übergeben Sie nun die Struktur an die [**iamcertifiedoutputprotection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f2b46-119">Now pass the structure to the [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2b46-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2b46-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2b46-121">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="f2b46-121">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



