---
description: Verarbeiten von Codec-MFT-Eingaben und-Ausgaben
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Verarbeiten von Codec-MFT-Eingaben und-Ausgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215017"
---
# <a name="processing-codec-mft-input-and-output"></a><span data-ttu-id="49e14-103">Verarbeiten von Codec-MFT-Eingaben und-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49e14-103">Processing Codec MFT Input and Output</span></span>

<span data-ttu-id="49e14-104">Wenn Sie den Eingabetyp und den Ausgabetyp für eine MFT konfiguriert haben, können Sie mit der Verarbeitung von Daten Beispielen beginnen.</span><span class="sxs-lookup"><span data-stu-id="49e14-104">When you have configured the input type and output type for an MFT, you can begin processing data samples.</span></span> <span data-ttu-id="49e14-105">Zum Verarbeiten von Beispielen an den MFT übergeben Sie die [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Methode, und rufen Sie dann das verarbeitete Beispiel durch Aufrufen von [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)ab.</span><span class="sxs-lookup"><span data-stu-id="49e14-105">You pass samples to the MFT for processing by using the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method, and then retrieve the processed sample by calling [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="49e14-106">Sie sollten genaue Zeitstempel und Dauer für alle bestandenen Eingabe Beispiele festlegen.</span><span class="sxs-lookup"><span data-stu-id="49e14-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="49e14-107">Zeitstempel sind nicht unbedingt erforderlich, unterstützen jedoch die Verwaltung von Audiodaten und Videos.</span><span class="sxs-lookup"><span data-stu-id="49e14-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="49e14-108">Wenn Sie nicht über die Zeitstempel für die Beispiele verfügen, ist es besser, Sie zu verlassen, als nicht unsichere Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="49e14-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49e14-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49e14-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49e14-110">Arbeiten mit Codec-MFTs</span><span class="sxs-lookup"><span data-stu-id="49e14-110">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



