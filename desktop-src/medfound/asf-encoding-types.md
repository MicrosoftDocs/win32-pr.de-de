---
description: ASF-Codierungs Typen
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: ASF-Codierungs Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128008"
---
# <a name="asf-encoding-types"></a><span data-ttu-id="0c5bb-103">ASF-Codierungs Typen</span><span class="sxs-lookup"><span data-stu-id="0c5bb-103">ASF Encoding Types</span></span>

<span data-ttu-id="0c5bb-104">Die Codierungs Methoden konzentrieren sich alle auf den Puffer, der vom Encoder zum Verwalten nicht komprimierter Eingabedaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-104">The encoding methods all focus on the buffer used by the encoder to manage uncompressed input data.</span></span> <span data-ttu-id="0c5bb-105">Dieser Puffer wird durch die Bitrate des Streams in Bits pro Sekunde und das Puffer Fenster in Millisekunden definiert.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-105">This buffer is defined by the bit rate of the stream, in bits per second, and the buffer window, in milliseconds.</span></span> <span data-ttu-id="0c5bb-106">Beim Codieren in ASF-Dateien halten die Windows Media Encoder die Einschränkungen des Puffers an.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-106">When encoding to ASF files, the Windows Media encoders abide by the constraints of the buffer.</span></span> <span data-ttu-id="0c5bb-107">Weitere Informationen zum Puffer Fenster finden Sie unter unkomplizierter [Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="0c5bb-107">For more information about the buffer window, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span> <span data-ttu-id="0c5bb-108">Wenn Sie wissen, wie und wann die einzelnen Methoden verwendet werden sollen, können Sie hochwertige komprimierte Inhalte erstellen.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-108">Knowing how and when to use each method can help you create high-quality compressed content.</span></span> <span data-ttu-id="0c5bb-109">Die folgende Tabelle enthält Links zu Themen zu den einzelnen verfügbaren Codierungs Methoden, die eine Anwendung verwenden kann, um Mediendaten in ASF zu codieren.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-109">The following table contains links to topics about each of the available encoding methods that an application can use to encode media data to ASF.</span></span>



| <span data-ttu-id="0c5bb-110">Codiermethode</span><span class="sxs-lookup"><span data-stu-id="0c5bb-110">Encoding method</span></span>                                                                                      | <span data-ttu-id="0c5bb-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c5bb-111">Description</span></span>                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c5bb-112">Konstante Bitrate-Codierung</span><span class="sxs-lookup"><span data-stu-id="0c5bb-112">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                         | <span data-ttu-id="0c5bb-113">Der Encoder komprimiert Daten auf eine angegebene Bitrate.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-113">The encoder compresses data to a specified bit rate.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="0c5bb-114">Qualitäts basierte Variable Bitrate Codierung</span><span class="sxs-lookup"><span data-stu-id="0c5bb-114">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="0c5bb-115">Der Encoder komprimiert Daten auf einen bestimmten Qualitäts Wert, sodass die Qualität der codierten Medien während der gesamten Dauer konsistent ist, unabhängig von den Puffer Anforderungen des resultierenden Streams.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-115">The encoder compresses data to a particular quality value so that the quality of the encoded media is consistent throughout its duration, regardless of the buffer requirements of the resulting stream.</span></span> |
| [<span data-ttu-id="0c5bb-116">Unbeschränkte Variablen Bitrate-Codierung</span><span class="sxs-lookup"><span data-stu-id="0c5bb-116">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="0c5bb-117">Der Encoder komprimiert Daten auf die höchste mögliche Qualität, während eine angegebene Bitrate beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-117">The encoder compresses data to the highest possible quality while maintaining a specified bit rate.</span></span> <span data-ttu-id="0c5bb-118">Dieser Modus wird auch als 2-Pass-VBR-Codierung (Variable Bitrate) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-118">This mode is also called 2-pass variable bit rate (VBR) encoding.</span></span>                                    |
| [<span data-ttu-id="0c5bb-119">Mit Spitzenwerten beschränkte Variable Bitrate-Codierung</span><span class="sxs-lookup"><span data-stu-id="0c5bb-119">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="0c5bb-120">Der Encoder komprimiert Daten auf eine angegebene Bitrate und behält dabei die Puffer Werte unter dem angegebenen maximalen Puffer Fenster und der angegebenen Bitrate bei.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-120">The encoder compresses data to a specified bit rate while keeping the buffer values under the specified maximum buffer window and bit rate.</span></span> <span data-ttu-id="0c5bb-121">Dieser Modus wird auch als 2-Durchlauf-Spitzenwert für VBR bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0c5bb-121">This mode is also called 2-pass peak VBR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="0c5bb-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c5bb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c5bb-123">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c5bb-123">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="0c5bb-124">Windows Media Encoder</span><span class="sxs-lookup"><span data-stu-id="0c5bb-124">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



