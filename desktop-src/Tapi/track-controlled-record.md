---
description: Dieses Thema enthält eine Prozedur zum Durchführen einer Nachverfolgung gesteuerten Aufzeichnung von Audiodatenströmen.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Track-Controlled Datensatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865688"
---
# <a name="track-controlled-record"></a><span data-ttu-id="babef-103">Track-Controlled Datensatz</span><span class="sxs-lookup"><span data-stu-id="babef-103">Track-Controlled Record</span></span>

<span data-ttu-id="babef-104">Dieses Thema enthält eine Prozedur zum Durchführen einer Nachverfolgung gesteuerten Aufzeichnung von Audiodatenströmen.</span><span class="sxs-lookup"><span data-stu-id="babef-104">This topic provides a procedure for performing track-controlled recording of audio streams.</span></span>

<span data-ttu-id="babef-105">**So führen Sie eine Nachverfolgung gesteuerte Aufzeichnung von Audiostreams durch**</span><span class="sxs-lookup"><span data-stu-id="babef-105">**To perform track-controlled recording of audio streams**</span></span>

1.  <span data-ttu-id="babef-106">Wählen Sie Datei nachverfolgen Terminals in Streams aus.</span><span class="sxs-lookup"><span data-stu-id="babef-106">Select File Track Terminals onto streams.</span></span>
2.  <span data-ttu-id="babef-107">Erstellen Sie das Terminal für den Datei Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="babef-107">Create the File Record Terminal.</span></span>
3.  <span data-ttu-id="babef-108">Legen Sie den Dateinamen fest.</span><span class="sxs-lookup"><span data-stu-id="babef-108">Set the file name.</span></span>
4.  <span data-ttu-id="babef-109">Enumerieren von Streams für den TAPI-Befehl.</span><span class="sxs-lookup"><span data-stu-id="babef-109">Enumerate streams on the TAPI call.</span></span> <span data-ttu-id="babef-110">Informationen zu diesen Schritten finden Sie im folgenden Verfahren.</span><span class="sxs-lookup"><span data-stu-id="babef-110">For these steps, see the following procedure.</span></span>
5.  <span data-ttu-id="babef-111">Ruft die [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) -Methode für das Terminal Datei Daten Satz ab, um die Datenstrom Aufzeichnung zu starten</span><span class="sxs-lookup"><span data-stu-id="babef-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Record Terminal to start stream recording.</span></span>

<span data-ttu-id="babef-112">**So zählen Sie Streams für den TAPI-Befehl auf**</span><span class="sxs-lookup"><span data-stu-id="babef-112">**To enumerate streams on the TAPI call**</span></span>

1.  <span data-ttu-id="babef-113">Erstellen Sie eine Spur desselben audiotyps und derselben Richtung wie der Stream.</span><span class="sxs-lookup"><span data-stu-id="babef-113">Create a track of the same audio type and direction as the stream.</span></span>
2.  <span data-ttu-id="babef-114">Legen Sie die Track-Eigenschaften für das Audioformat fest.</span><span class="sxs-lookup"><span data-stu-id="babef-114">Set the track properties for audio format.</span></span> <span data-ttu-id="babef-115">Wenn nicht festgelegt, ist das Format mit dem Stream-Format identisch.</span><span class="sxs-lookup"><span data-stu-id="babef-115">If not set, the format will be the same as the streams format.</span></span>
3.  <span data-ttu-id="babef-116">Wählen Sie den Track im Stream aus.</span><span class="sxs-lookup"><span data-stu-id="babef-116">Select the track on the stream.</span></span>

<span data-ttu-id="babef-117">Wenn eine Spur in mehreren Streams ausgewählt ist, bedeutet dies, dass Datenströme gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="babef-117">If one track is selected on multiple streams, this implies mixing streams.</span></span>

 

 



