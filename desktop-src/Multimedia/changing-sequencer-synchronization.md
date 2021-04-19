---
title: Ändern der Sequencer-Synchronisierung
description: Ändern der Sequencer-Synchronisierung
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET Befehls Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "106367252"
---
# <a name="changing-sequencer-synchronization"></a><span data-ttu-id="895bc-104">Ändern der Sequencer-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="895bc-104">Changing Sequencer Synchronization</span></span>

> [!NOTE]
> <span data-ttu-id="895bc-105">Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.</span><span class="sxs-lookup"><span data-stu-id="895bc-105">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="895bc-106">In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="895bc-106">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="895bc-107">Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.</span><span class="sxs-lookup"><span data-stu-id="895bc-107">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="895bc-108">Dieser Wortlaut wird verwendet, da es sich zurzeit um den in der Software verwendeten Wortlaut handelt.</span><span class="sxs-lookup"><span data-stu-id="895bc-108">This wording is used as it is currently the wording used within the software.</span></span> <span data-ttu-id="895bc-109">Aus Konsistenz Gründen enthält dieses Dokument dieses Wort.</span><span class="sxs-lookup"><span data-stu-id="895bc-109">For consistency, this document contains this word.</span></span> <span data-ttu-id="895bc-110">Wenn dieses Wort aus der Software entfernt wird, korrigieren wir dieses Dokument als Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="895bc-110">When this word is removed from the software, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="895bc-111">Um den Synchronisierungs Modus eines Sequencer-Geräts zu ändern, verwenden Sie die [**MCI \_ set**](mci-set.md) -Befehls Meldung mit den MCI \_ Seq \_ Set \_ Master-und MCI \_ Seq \_ Set \_ Slave-Flags.</span><span class="sxs-lookup"><span data-stu-id="895bc-111">To change the synchronization mode of a sequencer device, use the [**MCI\_SET**](mci-set.md) command message with the MCI\_SEQ\_SET\_MASTER and MCI\_SEQ\_SET\_SLAVE flags.</span></span> <span data-ttu-id="895bc-112">Zwei Member in der [**MCI \_ Seq \_ Set- \_ Parametern**](mci-seq-set-parms.md) -Struktur, **dwmaster** und **dwslave**, werden verwendet, um den Master-und den untergeordneten Synchronisierungs Modus anzugeben.</span><span class="sxs-lookup"><span data-stu-id="895bc-112">Two members in the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, **dwMaster** and **dwSlave**, are used to specify the master and subordinate synchronization modes.</span></span>

<span data-ttu-id="895bc-113">Der Master Synchronisierungs Modus steuert die vom Sequencer gesendeten Synchronisierungs Informationen an einen Ausgabeport.</span><span class="sxs-lookup"><span data-stu-id="895bc-113">The master synchronization mode controls synchronization information sent by the sequencer to an output port.</span></span> <span data-ttu-id="895bc-114">Im folgenden finden Sie die Konstanten für den **dwmaster** -Member und die entsprechenden Master Synchronisierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="895bc-114">Following are the constants for the **dwMaster** member and their corresponding master synchronization modes.</span></span>



| <span data-ttu-id="895bc-115">Konstante</span><span class="sxs-lookup"><span data-stu-id="895bc-115">Constant</span></span>        | <span data-ttu-id="895bc-116">Synchronisierungsmodus</span><span class="sxs-lookup"><span data-stu-id="895bc-116">Synchronization mode</span></span>                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="895bc-117">MCI \_ -Integration \_</span><span class="sxs-lookup"><span data-stu-id="895bc-117">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="895bc-118">MIDI-Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="895bc-118">MIDI Synchronization.</span></span> <span data-ttu-id="895bc-119">Senden von Zeit Steuerungsinformationen an den Ausgabeport mithilfe von MIDI-Zeitachsen Nachrichten</span><span class="sxs-lookup"><span data-stu-id="895bc-119">Send timing information to output port using MIDI timing clock messages.</span></span>   |
| <span data-ttu-id="895bc-120">MCI- \_ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="895bc-120">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="895bc-121">SMPTE-Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="895bc-121">SMPTE Synchronization.</span></span> <span data-ttu-id="895bc-122">Senden von Zeit Steuerungsinformationen an den Ausgabeport mithilfe von Nachrichten im Rahmen von MIDI</span><span class="sxs-lookup"><span data-stu-id="895bc-122">Send timing information to output port using MIDI quarter-frame messages.</span></span> |
| <span data-ttu-id="895bc-123">MCI-nicht verfügbar \_ \_</span><span class="sxs-lookup"><span data-stu-id="895bc-123">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="895bc-124">Keine Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="895bc-124">No Synchronization.</span></span> <span data-ttu-id="895bc-125">Senden Sie keine Zeit Steuerungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="895bc-125">Send no timing information.</span></span>                                                  |



 

<span data-ttu-id="895bc-126">Der untergeordnete Synchronisierungs Modus steuert, wo der Sequencer seine Zeit Steuerungsinformationen für die Wiedergabe einer MIDI-Datei abruft.</span><span class="sxs-lookup"><span data-stu-id="895bc-126">The subordinate synchronization mode controls where the sequencer gets its timing information to play a MIDI file.</span></span> <span data-ttu-id="895bc-127">Im folgenden finden Sie die Konstanten für den **dwslave** -Member und die entsprechenden untergeordneten Synchronisierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="895bc-127">Following are the constants for the **dwSlave** member and their corresponding subordinate synchronization modes.</span></span>



| <span data-ttu-id="895bc-128">Konstante</span><span class="sxs-lookup"><span data-stu-id="895bc-128">Constant</span></span>        | <span data-ttu-id="895bc-129">Synchronisierungsmodus</span><span class="sxs-lookup"><span data-stu-id="895bc-129">Synchronization mode</span></span>                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="895bc-130">MCI- \_ \_ Datei</span><span class="sxs-lookup"><span data-stu-id="895bc-130">MCI\_SEQ\_FILE</span></span>  | <span data-ttu-id="895bc-131">Datei Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="895bc-131">File Synchronization.</span></span> <span data-ttu-id="895bc-132">Zeit Steuerungsinformationen aus der MIDI-Datei erhalten.</span><span class="sxs-lookup"><span data-stu-id="895bc-132">Get timing information from MIDI file.</span></span>                                                                                       |
| <span data-ttu-id="895bc-133">MCI \_ -Integration \_</span><span class="sxs-lookup"><span data-stu-id="895bc-133">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="895bc-134">MIDI-Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="895bc-134">MIDI Synchronization.</span></span> <span data-ttu-id="895bc-135">Informationen zur zeitlichen Steuerung aus dem eingabeport mithilfe von MIDI-Zeitachsen Nachrichten</span><span class="sxs-lookup"><span data-stu-id="895bc-135">Get timing information from input port using MIDI timing clock messages.</span></span>                                                     |
| <span data-ttu-id="895bc-136">MCI- \_ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="895bc-136">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="895bc-137">SMPTE-Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="895bc-137">SMPTE Synchronization.</span></span> <span data-ttu-id="895bc-138">Informationen zur zeitlichen Steuerung aus dem eingabeport mithilfe von MIDI-Quartals Frame-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="895bc-138">Get timing information from input port using MIDI quarter-frame messages.</span></span>                                                   |
| <span data-ttu-id="895bc-139">MCI-nicht verfügbar \_ \_</span><span class="sxs-lookup"><span data-stu-id="895bc-139">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="895bc-140">Keine Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="895bc-140">No Synchronization.</span></span> <span data-ttu-id="895bc-141">Erhalten Sie nur Zeit Steuerungsinformationen von MCI-Befehlen, und ignorieren Sie Zeit Steuerungsinformationen (z. b. die Änderung von Änderungen) in der Datei "MIDI"</span><span class="sxs-lookup"><span data-stu-id="895bc-141">Get timing information from MCI commands only and ignore timing information (such as tempo changes) that are in the MIDI file.</span></span> |



 

> [!Note]  
> <span data-ttu-id="895bc-142">Derzeit unterstützt der MCI-Dienst für die Master Synchronisierung nur den Modus "keine Synchronisierung" (MCI-"keine" \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="895bc-142">Currently, for master synchronization, the MCI MIDI sequencer supports only the No Synchronization mode (MCI\_SEQ\_NONE).</span></span> <span data-ttu-id="895bc-143">Bei der untergeordneten Synchronisierung wird nur der Datei Synchronisierungs Modus (MCI \_ \_ -Datei) und der Modus "keine Synchronisierung" (MCI-Datei "keine") unterstützt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="895bc-143">For subordinate synchronization, it supports only the File Synchronization mode (MCI\_SEQ\_FILE) and the No Synchronization mode (MCI\_SEQ\_NONE).</span></span>

 

 

 




