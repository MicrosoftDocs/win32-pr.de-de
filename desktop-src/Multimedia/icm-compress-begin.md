---
title: ICM_COMPRESS_BEGIN Meldung (VFW. h)
description: Mit der ICM- \_ Komprimierungs \_ Begin-Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Komprimieren von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des iccompressbegin-Makros senden.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040988"
---
# <a name="icm_compress_begin-message"></a><span data-ttu-id="7bd77-105">ICM- \_ Komprimierungs \_ Begin-Meldung</span><span class="sxs-lookup"><span data-stu-id="7bd77-105">ICM\_COMPRESS\_BEGIN message</span></span>

<span data-ttu-id="7bd77-106">Mit der **ICM- \_ Komprimierungs \_ Begin** -Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Komprimieren von Daten vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="7bd77-106">The **ICM\_COMPRESS\_BEGIN** message notifies a video compression driver to prepare to compress data.</span></span> <span data-ttu-id="7bd77-107">Sie können diese Nachricht explizit oder mithilfe des [**iccompressbegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="7bd77-107">You can send this message explicitly or by using the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro.</span></span>


```C++
ICM_COMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="7bd77-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bd77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bd77-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="7bd77-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="7bd77-110">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="7bd77-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="7bd77-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*</span><span class="sxs-lookup"><span data-stu-id="7bd77-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="7bd77-112">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="7bd77-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bd77-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bd77-113">Return Value</span></span>

<span data-ttu-id="7bd77-114">Gibt ICERR \_ OK zurück, wenn der Treiber die angegebene Komprimierung oder ICERR badformat unterstützt, \_ Wenn das Eingabe-oder Ausgabeformat nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7bd77-114">Returns ICERR\_OK if the driver supports the specified compression or ICERR\_BADFORMAT if the input or output format is not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bd77-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bd77-115">Remarks</span></span>

<span data-ttu-id="7bd77-116">Der Treiber sollte alle Tabellen oder Arbeitsspeicher zuweisen und initialisieren, die er zum Komprimieren der Datenformate benötigt, wenn er die [**ICM- \_ Komprimierungs**](icm-compress.md) Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="7bd77-116">The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the [**ICM\_COMPRESS**](icm-compress.md) message.</span></span>

<span data-ttu-id="7bd77-117">VCM speichert die Einstellungen der letzten **ICM- \_ Komprimierungs \_ Begin** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7bd77-117">VCM saves the settings of the most recent **ICM\_COMPRESS\_BEGIN** message.</span></span> <span data-ttu-id="7bd77-118">Die **ICM- \_ Komprimierungs \_ Begin** -und [**ICM- \_ Komprimierungs \_**](icm-compress-end.md) Meldungen werden nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="7bd77-118">The **ICM\_COMPRESS\_BEGIN** and [**ICM\_COMPRESS\_END**](icm-compress-end.md) messages do not nest.</span></span> <span data-ttu-id="7bd77-119">Wenn der Treiber **ICM \_ Compress \_ Begin** empfängt, bevor die Komprimierung mit **ICM- \_ Komprimierung \_ beendet** wird, sollte die Komprimierung mit neuen Parametern neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7bd77-119">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bd77-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bd77-120">Requirements</span></span>



| <span data-ttu-id="7bd77-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bd77-121">Requirement</span></span> | <span data-ttu-id="7bd77-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7bd77-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7bd77-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bd77-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7bd77-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bd77-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7bd77-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bd77-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7bd77-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bd77-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7bd77-127">Header</span><span class="sxs-lookup"><span data-stu-id="7bd77-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bd77-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bd77-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bd77-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bd77-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd77-130">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="7bd77-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7bd77-131">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="7bd77-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

