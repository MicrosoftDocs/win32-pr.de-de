---
title: Sequenz Komprimierung
description: Sequenz Komprimierung
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- Videokomprimierungs-Manager (VCM), Sequenz Komprimierung
- VCM (Videokomprimierungs-Manager), Sequenz Komprimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947664"
---
# <a name="sequence-compression"></a><span data-ttu-id="60742-105">Sequenz Komprimierung</span><span class="sxs-lookup"><span data-stu-id="60742-105">Sequence Compression</span></span>

<span data-ttu-id="60742-106">Die Anwendung kann die Funktionen " [**icseqcompressframe**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)", " [**icseqcompressframestart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)" und " [**icseqcompressframeend**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) " verwenden, um eine Sequenz von Frames zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="60742-106">Your application can use the [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart), and [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) functions to compress a sequence of frames.</span></span> <span data-ttu-id="60742-107">Diese Funktionen verwenden die in der [**compvars**](/windows/desktop/api/Vfw/ns-vfw-compvars) -Struktur gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="60742-107">These functions use the data stored in the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure.</span></span> <span data-ttu-id="60742-108">Anwendungen verwenden die Funktion [**iccompressorchoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) , um dem Benutzer zu ermöglichen, einen Kompressor auszuwählen, zu öffnen und die Komprimierungs Parameter in der **compvars** -Struktur festzulegen. Anwendungen können die Parameter in der Struktur jedoch manuell festlegen.</span><span class="sxs-lookup"><span data-stu-id="60742-108">Applications use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to allow the user to select a compressor, open it, and set the compression parameters in the **COMPVARS** structure; however, applications can set the parameters in the structure manually.</span></span>

<span data-ttu-id="60742-109">Bevor eine Anwendung damit beginnen kann, eine Sequenz von Frames zu komprimieren, muss Sie **icseqcompressframestart** verwenden, um die erforderlichen Ressourcen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="60742-109">Before an application can begin compressing a sequence of frames, it must use **ICSeqCompressFrameStart** to allocate the necessary resources.</span></span> <span data-ttu-id="60742-110">Nachdem die Ressourcen zugewiesen wurden, kann die Anwendung **icseqcompressframe** verwenden, um jeden Frame einzeln zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="60742-110">After the resources are allocated, the application can use **ICSeqCompressFrame** to compress each frame individually.</span></span> <span data-ttu-id="60742-111">Die bei der Komprimierung der Sequenz verwendete Framerate und die Keyframe-Frequenz werden in Elementen der **compvars** -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="60742-111">The frame rate and key-frame frequency used in compressing the sequence are specified in members of the **COMPVARS** structure.</span></span> <span data-ttu-id="60742-112">Der Rückgabewert für **iccqcompressframe** verweist auf die komprimierten Daten.</span><span class="sxs-lookup"><span data-stu-id="60742-112">The return value for **ICSeqCompressFrame** points to the compressed data.</span></span>

<span data-ttu-id="60742-113">Wenn eine Anwendung das Komprimieren einer Sequenz abgeschlossen hat, kann **icseqcompressframeend** verwendet werden, um Systemressourcen freizugeben, die für **icseqcompressframestart** reserviert wurden.</span><span class="sxs-lookup"><span data-stu-id="60742-113">When an application finishes compressing a sequence, it can use **ICSeqCompressFrameEnd** to free system resources allocated for **ICSeqCompressFrameStart**.</span></span> <span data-ttu-id="60742-114">Um die Ressourcen freizugeben, die für die **compvars** -Struktur reserviert werden, kann die Anwendung die [**iccompressorfree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="60742-114">To free the resources allocated for the **COMPVARS** structure, the application can use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function.</span></span>

 

 




