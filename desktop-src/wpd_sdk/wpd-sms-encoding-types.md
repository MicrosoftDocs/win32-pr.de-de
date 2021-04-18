---
description: Der \_ Enumerationstyp der WPD-SMS- \_ Codierungs \_ Typen beschreibt den Codierungstyp einer SMS (Short Message Service)-Nachricht.
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: WPD_SMS_ENCODING_TYPES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371487"
---
# <a name="wpd_sms_encoding_types-enumeration"></a><span data-ttu-id="96b4a-103">WPD- \_ SMS- \_ \_ Codierungstypen Enumeration</span><span class="sxs-lookup"><span data-stu-id="96b4a-103">WPD\_SMS\_ENCODING\_TYPES enumeration</span></span>

<span data-ttu-id="96b4a-104">Der Enumerationstyp der **WPD- \_ SMS- \_ Codierungs \_ Typen** beschreibt den Codierungstyp einer SMS (Short Message Service)-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="96b4a-104">The **WPD\_SMS\_ENCODING\_TYPES** enumeration type describes the encoding type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b4a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96b4a-105">Syntax</span></span>


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="96b4a-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="96b4a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="96b4a-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS- \_ Codierung ( \_ 7 \_ Bit)**</span><span class="sxs-lookup"><span data-stu-id="96b4a-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS\_ENCODING\_7\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="96b4a-108">7-Bit-Codierung.</span><span class="sxs-lookup"><span data-stu-id="96b4a-108">Seven-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="96b4a-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS- \_ Codierung ( \_ 8 \_ Bit)**</span><span class="sxs-lookup"><span data-stu-id="96b4a-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS\_ENCODING\_8\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="96b4a-110">8-Bit-Codierung.</span><span class="sxs-lookup"><span data-stu-id="96b4a-110">Eight-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="96b4a-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS- \_ Codierung \_ UTF \_ 16**</span><span class="sxs-lookup"><span data-stu-id="96b4a-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS\_ENCODING\_UTF\_16**</span></span>
</dt> <dd>

<span data-ttu-id="96b4a-112">16-Bit-Codierung (UTF).</span><span class="sxs-lookup"><span data-stu-id="96b4a-112">Sixteen-bit encoding (UTF).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96b4a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96b4a-113">Remarks</span></span>

<span data-ttu-id="96b4a-114">Diese Enumeration wird von der [WPD- \_ SMS- \_ Codierungs](sms-properties.md) Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="96b4a-114">This enumeration is used by the [WPD\_SMS\_ENCODING](sms-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="96b4a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96b4a-115">Requirements</span></span>



| <span data-ttu-id="96b4a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96b4a-116">Requirement</span></span> | <span data-ttu-id="96b4a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="96b4a-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="96b4a-118">Header</span><span class="sxs-lookup"><span data-stu-id="96b4a-118">Header</span></span><br/> | <dl> <span data-ttu-id="96b4a-119"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="96b4a-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96b4a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96b4a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b4a-121">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="96b4a-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




