---
description: Verarbeiten von Codec DMO-Eingaben und-Ausgaben
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Verarbeiten von Codec DMO-Eingaben und-Ausgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344409"
---
# <a name="processing-codec-dmo-input-and-output"></a><span data-ttu-id="27568-103">Verarbeiten von Codec DMO-Eingaben und-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27568-103">Processing Codec DMO Input and Output</span></span>

<span data-ttu-id="27568-104">Wenn Sie den Eingabetyp und den Ausgabetyp für ein DMO konfiguriert haben, können Sie mit der Verarbeitung von Daten Beispielen beginnen.</span><span class="sxs-lookup"><span data-stu-id="27568-104">When you have configured the input type and output type for a DMO, you can begin processing data samples.</span></span> <span data-ttu-id="27568-105">Sie übergeben Beispiele an den DMO zur Verarbeitung mithilfe der **imediaobject::P rocessinput** -Methode, und rufen Sie dann das verarbeitete Beispiel durch Aufrufen von **imediaobject::P rocess Output** ab.</span><span class="sxs-lookup"><span data-stu-id="27568-105">You pass samples to the DMO for processing using the **IMediaObject::ProcessInput** method, and then retrieve the processed sample by calling **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="27568-106">Sie sollten genaue Zeitstempel und Dauer für alle bestandenen Eingabe Beispiele festlegen.</span><span class="sxs-lookup"><span data-stu-id="27568-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="27568-107">Zeitstempel sind nicht unbedingt erforderlich, unterstützen jedoch die Verwaltung von Audiodaten und Videos.</span><span class="sxs-lookup"><span data-stu-id="27568-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="27568-108">Wenn Sie nicht über die Zeitstempel für die Beispiele verfügen, ist es besser, Sie zu verlassen, als nicht unsichere Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="27568-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27568-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27568-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27568-110">Arbeiten mit Codec-DMOS</span><span class="sxs-lookup"><span data-stu-id="27568-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 



