---
title: Überwachen des Fortschritts von Kompressoren und Dekompressoren
description: Überwachen des Fortschritts von Kompressoren und Dekompressoren
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- Videokomprimierungs-Manager (VCM), Überwachung
- VCM (Videokomprimierungs-Manager), Überwachung
- Icsetstatusproc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338193"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a><span data-ttu-id="f36a4-106">Überwachen des Fortschritts von Kompressoren und Dekompressoren</span><span class="sxs-lookup"><span data-stu-id="f36a4-106">Monitoring the Progress of Compressors and Decompressors</span></span>

<span data-ttu-id="f36a4-107">Die Anwendung kann den Fortschritt eines langwierigen Vorgangs überwachen, der von einem Kompressor oder Dekompressor durchgeführt wird, indem Sie die Adresse einer Rückruffunktion sendet.</span><span class="sxs-lookup"><span data-stu-id="f36a4-107">Your application can monitor the progress of a lengthy operation performed by a compressor or decompressor by sending it the address of a callback function.</span></span> <span data-ttu-id="f36a4-108">Sie können die [**icsetstatusproc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) -Funktion verwenden, um die Adresse an den Kompressor oder Dekompressor zu senden.</span><span class="sxs-lookup"><span data-stu-id="f36a4-108">You can use the [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) function to send the address to the compressor or decompressor.</span></span> <span data-ttu-id="f36a4-109">Wenn der-Kompressor oder der Dekompressor diese Adresse empfängt, sendet er Statusmeldungen an die-Funktion.</span><span class="sxs-lookup"><span data-stu-id="f36a4-109">When the compressor or decompressor receives this address, it sends status messages to the function.</span></span> <span data-ttu-id="f36a4-110">Diese Meldungen geben an, ob der Vorgang gestartet, angehalten, bereitstellt oder fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f36a4-110">These messages indicate whether the operation is starting, stopping, yielding, or proceeding.</span></span>

 

 




