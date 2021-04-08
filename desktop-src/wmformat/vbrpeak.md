---
title: Vbrpeak
description: Das vbrpeak-Attribut enthält die höchste momentane Bitrate in einem VBR-codierten Stream (Variable Bitrate).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- Vbrmaximum Windows Media-Format
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038080"
---
# <a name="vbrpeak"></a><span data-ttu-id="93835-104">Vbrpeak</span><span class="sxs-lookup"><span data-stu-id="93835-104">VBRPeak</span></span>

<span data-ttu-id="93835-105">Das **vbrpeak** -Attribut enthält die höchste momentane Bitrate in einem VBR-codierten Stream (Variable Bitrate).</span><span class="sxs-lookup"><span data-stu-id="93835-105">The **VBRPeak** attribute contains the highest momentary bit rate in a variable bit rate (VBR) encoded stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="93835-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="93835-106">Global Constant</span></span>

<span data-ttu-id="93835-107">g \_ wszvbrpeak</span><span class="sxs-lookup"><span data-stu-id="93835-107">g\_wszVBRPeak</span></span>

## <a name="data-type"></a><span data-ttu-id="93835-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="93835-108">Data Type</span></span>

<span data-ttu-id="93835-109">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="93835-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="93835-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93835-110">Remarks</span></span>

<span data-ttu-id="93835-111">Beim Zugriff auf die **IWMHeaderInfo3** -Schnittstelle des Writer-Objekts können Sie diesen Wert hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="93835-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="93835-112">In anderen Objekten (Metadaten-Editor, Reader und synchroner Reader) ist dieser Wert schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="93835-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="93835-113">Der Writer schreibt automatisch einen **vbrpeak** -Wert für jeden VBR-Stream.</span><span class="sxs-lookup"><span data-stu-id="93835-113">The writer automatically writes a **VBRPeak** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="93835-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93835-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93835-115">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="93835-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




