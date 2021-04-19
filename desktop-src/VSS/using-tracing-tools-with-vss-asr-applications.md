---
description: Sie können das Logman-Tool verwenden, um Ablauf Verfolgungs Informationen für VSS-Anwendungen zu sammeln, die automatisierte System Wiederherstellung (ASR) verwenden.
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Verwenden von Ablauf Verfolgungs Tools mit ASR-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356770"
---
# <a name="using-tracing-tools-with-asr-applications"></a><span data-ttu-id="02e74-103">Verwenden von Ablauf Verfolgungs Tools mit ASR-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="02e74-103">Using Tracing Tools with ASR Applications</span></span>

<span data-ttu-id="02e74-104">Sie können das Logman-Tool verwenden, um Ablauf Verfolgungs Informationen für VSS-Anwendungen zu sammeln, die [automatisierte System Wiederherstellung (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="02e74-104">You can use the Logman tool to collect tracing information for VSS applications that use [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span> <span data-ttu-id="02e74-105">Logman (logman.exe) ist ein Ablauf Verfolgungs Controller für Ablauf Verfolgungs Ereignisse und Leistungsindikatoren.</span><span class="sxs-lookup"><span data-stu-id="02e74-105">Logman (logman.exe) is a trace controller for trace events and performance counters.</span></span> <span data-ttu-id="02e74-106">Es ist in Windows XP und höheren Versionen von Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="02e74-106">It is included in Windows XP and later versions of Windows.</span></span> <span data-ttu-id="02e74-107">Oder Sie können, wenn Sie möchten, das tracelog-Tool verwenden, um die gleichen ASR-Ablauf Verfolgungs Informationen zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="02e74-107">Or, if you prefer, you can use the Tracelog tool to collect the same ASR tracing information.</span></span> <span data-ttu-id="02e74-108">TraceLog ist im Windows-Treiberkit (WDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="02e74-108">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="02e74-109">Informationen zur Verwendung von Ablauf Verfolgungs Tools mit VSS finden Sie unter [Verwenden von Ablauf Verfolgungs Tools mit VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="02e74-109">To use tracing tools with VSS, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="using-logman"></a><span data-ttu-id="02e74-110">Verwenden von logman</span><span class="sxs-lookup"><span data-stu-id="02e74-110">Using Logman</span></span>

<span data-ttu-id="02e74-111">Im folgenden Verfahren wird beschrieben, wie Sie Logman mit der ASR-Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="02e74-111">The following procedure describes how to use Logman with your ASR application.</span></span>

<span data-ttu-id="02e74-112">**So verwenden Sie Logman mit der ASR-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="02e74-112">**To use Logman with your ASR application**</span></span>

1.  <span data-ttu-id="02e74-113">Verwenden Sie den folgenden Befehl zum Starten der Ablauf Verfolgung:</span><span class="sxs-lookup"><span data-stu-id="02e74-113">Use the following command to start tracing:</span></span>

    <span data-ttu-id="02e74-114">**logman Start ASR-o** *x: \\ \* \* \* ASR. ETL-ETS-p {6407345b-94f 2-44c8-b3db-4e076be46816} 0xFF 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="02e74-114">**logman start asr -o** *x:\\*\*\*asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="02e74-115">Ersetzen Sie "x: \\ " durch den Pfad zu dem Verzeichnis, in dem die Ablauf Verfolgungs Protokolldatei gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="02e74-115">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="02e74-116">Für eine optimale Leistung sollte sich die Ablauf Verfolgungs Protokolldatei auf einem Volume befinden, das nicht Teil der Schatten Kopie ist.</span><span class="sxs-lookup"><span data-stu-id="02e74-116">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

2.  <span data-ttu-id="02e74-117">Verwenden Sie den folgenden Befehl, um die Ablauf Verfolgung anzuhalten:</span><span class="sxs-lookup"><span data-stu-id="02e74-117">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="02e74-118">**logman beendet ASR-ETS**</span><span class="sxs-lookup"><span data-stu-id="02e74-118">**logman stop asr -ets**</span></span>

<span data-ttu-id="02e74-119">Die Ablauf Verfolgungs Protokolldatei ist *x \\ :* ASR. ETL.</span><span class="sxs-lookup"><span data-stu-id="02e74-119">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="02e74-120">Weitere Informationen zum Logman-Tool finden Sie unter [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="02e74-120">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="02e74-121">Verwenden von tracelog</span><span class="sxs-lookup"><span data-stu-id="02e74-121">Using Tracelog</span></span>

<span data-ttu-id="02e74-122">Im folgenden Verfahren wird die Verwendung von tracelog beschrieben.</span><span class="sxs-lookup"><span data-stu-id="02e74-122">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="02e74-123">**So verwenden Sie tracelog**</span><span class="sxs-lookup"><span data-stu-id="02e74-123">**To use Tracelog**</span></span>

1.  <span data-ttu-id="02e74-124">Erstellen Sie eine Textdatei mit dem Namen ASR. CTL, die nur den folgenden Text enthält:</span><span class="sxs-lookup"><span data-stu-id="02e74-124">Create a text file named asr.ctl that contains only the following text:</span></span>

    <span data-ttu-id="02e74-125">**6407345b-94f 2-44c8-b3db-4e076be46816 ASR**</span><span class="sxs-lookup"><span data-stu-id="02e74-125">**6407345b-94f2-44c8-b3db-4e076be46816 asr**</span></span>

2.  <span data-ttu-id="02e74-126">Verwenden Sie den folgenden Befehl zum Starten der Ablauf Verfolgung:</span><span class="sxs-lookup"><span data-stu-id="02e74-126">Use the following command to start tracing:</span></span>

    <span data-ttu-id="02e74-127">**tracelog-Start ASR-f** *x: \\ \* \* \* ASR. ETL-GUID ASR. CTL-Flag 0xFF-Level 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="02e74-127">**tracelog -start asr -f** *x:\\*\*\*asr.etl -guid asr.ctl -flag 0xff -level 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="02e74-128">Ersetzen Sie "x: \\ " durch den Pfad zu dem Verzeichnis, in dem die Ablauf Verfolgungs Protokolldatei gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="02e74-128">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="02e74-129">Für eine optimale Leistung sollte sich die Ablauf Verfolgungs Protokolldatei auf einem Volume befinden, das nicht Teil der Schatten Kopie ist.</span><span class="sxs-lookup"><span data-stu-id="02e74-129">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

3.  <span data-ttu-id="02e74-130">Verwenden Sie den folgenden Befehl, um die Ablauf Verfolgung anzuhalten:</span><span class="sxs-lookup"><span data-stu-id="02e74-130">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="02e74-131">**tracelog-ASR Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="02e74-131">**tracelog -stop asr**</span></span>

<span data-ttu-id="02e74-132">Die Ablauf Verfolgungs Protokolldatei ist *x \\ :* ASR. ETL.</span><span class="sxs-lookup"><span data-stu-id="02e74-132">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="02e74-133">Weitere Informationen zum tracelog-Tool finden Sie unter [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="02e74-133">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
