---
description: Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: MFPKEY_CODEDNONZEROFRAMES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347561"
---
# <a name="mfpkey_codednonzeroframes-property"></a><span data-ttu-id="3f5b5-103">Mfpkey \_ codednonzeroframes (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3f5b5-103">MFPKEY\_CODEDNONZEROFRAMES Property</span></span>

<span data-ttu-id="3f5b5-104">Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="3f5b5-104">Specifies the number of video frames encoded by the codec that actually contain data.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3f5b5-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3f5b5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3f5b5-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f5b5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="3f5b5-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3f5b5-107">Data Type</span></span>

<span data-ttu-id="3f5b5-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3f5b5-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="3f5b5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f5b5-109">Remarks</span></span>

<span data-ttu-id="3f5b5-110">Dieser Wert ist gleich " [mfpkey \_ totalFrames](mfpkey-totalframesproperty.md) " abzüglich aller Frames, die aufgrund von Bitraten Einschränkungen (abzüglich aller NULL-Byte-Frames) gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="3f5b5-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints, minus any zero-byte frames.</span></span> <span data-ttu-id="3f5b5-111">Sie können diesen Wert erhalten, nachdem Sie die Übergabe von Beispielen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="3f5b5-111">You can get this value after you are finished passing samples.</span></span> <span data-ttu-id="3f5b5-112">Für doppelte Frames können NULL-Byte-Frames erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3f5b5-112">Zero-byte frames can be created for duplicate frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f5b5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f5b5-113">Requirements</span></span>



| <span data-ttu-id="3f5b5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f5b5-114">Requirement</span></span> | <span data-ttu-id="3f5b5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3f5b5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5b5-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f5b5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3f5b5-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f5b5-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3f5b5-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f5b5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3f5b5-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f5b5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f5b5-120">Header</span><span class="sxs-lookup"><span data-stu-id="3f5b5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f5b5-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f5b5-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f5b5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f5b5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f5b5-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f5b5-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
