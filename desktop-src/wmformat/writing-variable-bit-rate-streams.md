---
title: Schreiben von variablenbitrate-Streams
description: Schreiben von variablenbitrate-Streams
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Advanced Systems Format (ASF), Schreiben von VBR-Streams
- ASF (Advanced Systems Format), Schreiben von VBR-Streams
- variablenbitrate (VBR), Schreiben von Streams
- VBR (Variable Bitrate), Schreiben von Streams
- Streams, Schreiben von VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723392"
---
# <a name="writing-variable-bit-rate-streams"></a><span data-ttu-id="20325-108">Schreiben von variablenbitrate-Streams</span><span class="sxs-lookup"><span data-stu-id="20325-108">Writing Variable Bit Rate Streams</span></span>

<span data-ttu-id="20325-109">VBR-Streams (Variable Bitrate) werden auf die gleiche Weise wie mit konstanten Bitrate (CBR) geschrieben.</span><span class="sxs-lookup"><span data-stu-id="20325-109">Variable bit rate (VBR) streams are written the same way as constant bit rate (CBR) streams.</span></span> <span data-ttu-id="20325-110">Der einzige Unterschied besteht in der vom Writer und den Codecs intern durchgeführten Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="20325-110">The only difference is in the processing performed internally by the writer and the codecs.</span></span> <span data-ttu-id="20325-111">Allerdings erfordert die Bitrate-basierte VBR (sowohl eingeschränkt als auch nicht eingeschränkt) einen Vorverarbeitungs Durchlauf im Writer.</span><span class="sxs-lookup"><span data-stu-id="20325-111">However, bit rate based VBR (both constrained and unconstrained) requires a preprocessing pass in the writer.</span></span>

<span data-ttu-id="20325-112">Überprüfen Sie für jeden Stream den Rückgabewert für den ersten-Befehl, den Sie für " [**iwmwriter:: Write tesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) " vornehmen.</span><span class="sxs-lookup"><span data-stu-id="20325-112">You should check the return value for the first call you make to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) for each stream.</span></span> <span data-ttu-id="20325-113">Wenn der zurückgegebene Fehlercode NS \_ E \_ ungültige \_ NUM- \_ Pässe ist, erfordert der Stream einen Vorverarbeitungs Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="20325-113">If the error code returned is NS\_E\_INVALID\_NUM\_PASSES, the stream requires a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20325-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20325-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20325-115">**Verwenden von Two-Pass Codierung**</span><span class="sxs-lookup"><span data-stu-id="20325-115">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="20325-116">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="20325-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




