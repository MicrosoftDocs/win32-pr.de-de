---
title: Bufferaverage
description: Das bufferaverage-Attribut enthält die durchschnittliche Puffergröße, die für einen VBR-Stream (Variable Bitrate) benötigt wird.
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- Bufferaverage Windows Media-Format
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100987"
---
# <a name="bufferaverage"></a><span data-ttu-id="2c2dd-104">Bufferaverage</span><span class="sxs-lookup"><span data-stu-id="2c2dd-104">BufferAverage</span></span>

<span data-ttu-id="2c2dd-105">Das **bufferaverage** -Attribut enthält die durchschnittliche Puffergröße, die für einen VBR-Stream (Variable Bitrate) benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2c2dd-105">The **BufferAverage** attribute contains the average buffer size needed for a variable bit rate (VBR) stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="2c2dd-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="2c2dd-106">Global Constant</span></span>

<span data-ttu-id="2c2dd-107">g \_ wszbufferaverage</span><span class="sxs-lookup"><span data-stu-id="2c2dd-107">g\_wszBufferAverage</span></span>

## <a name="data-type"></a><span data-ttu-id="2c2dd-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2c2dd-108">Data Type</span></span>

<span data-ttu-id="2c2dd-109">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2c2dd-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="2c2dd-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c2dd-110">Remarks</span></span>

<span data-ttu-id="2c2dd-111">Beim Zugriff auf die **IWMHeaderInfo3** -Schnittstelle des Writer-Objekts können Sie diesen Wert hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="2c2dd-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="2c2dd-112">In anderen Objekten (Metadaten-Editor, Reader und synchroner Reader) ist dieser Wert schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2c2dd-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="2c2dd-113">Der Writer schreibt automatisch einen **bufferaverage** -Wert für jeden VBR-Stream.</span><span class="sxs-lookup"><span data-stu-id="2c2dd-113">The writer automatically writes a **BufferAverage** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c2dd-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c2dd-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c2dd-115">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="2c2dd-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




