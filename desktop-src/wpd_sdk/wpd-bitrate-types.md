---
description: Der \_ \_ Enumerationstyp der WPD-Bitrate-Typen beschreibt einen Komprimierungstyp für Audiodateien.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: WPD_BITRATE_TYPES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370285"
---
# <a name="wpd_bitrate_types-enumeration"></a><span data-ttu-id="70159-103">WPD \_ Bitrate \_ types-Enumeration</span><span class="sxs-lookup"><span data-stu-id="70159-103">WPD\_BITRATE\_TYPES enumeration</span></span>

<span data-ttu-id="70159-104">Der Enumerationstyp der **WPD- \_ Bitrate- \_ Typen** beschreibt den Komprimierungstyp einer Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="70159-104">The **WPD\_BITRATE\_TYPES** enumeration type describes an audio file's compression type.</span></span>

## <a name="syntax"></a><span data-ttu-id="70159-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70159-105">Syntax</span></span>


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="70159-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="70159-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="70159-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**nicht verwendeter WPD- \_ Bitrate- \_ Typ \_**</span><span class="sxs-lookup"><span data-stu-id="70159-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**WPD\_BITRATE\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="70159-108">Dieser Wert wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="70159-108">This value has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="70159-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**diskreter WPD- \_ Bitrate- \_ Typ \_**</span><span class="sxs-lookup"><span data-stu-id="70159-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD\_BITRATE\_TYPE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="70159-110">Komprimierung konstanter Bitrate.</span><span class="sxs-lookup"><span data-stu-id="70159-110">Constant bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="70159-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD- \_ Bitrate- \_ \_ Typvariable**</span><span class="sxs-lookup"><span data-stu-id="70159-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD\_BITRATE\_TYPE\_VARIABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70159-112">Komprimierung der Variablen Bitrate.</span><span class="sxs-lookup"><span data-stu-id="70159-112">Variable bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="70159-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD- \_ Bitrate ( \_ \_ Free)**</span><span class="sxs-lookup"><span data-stu-id="70159-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD\_BITRATE\_TYPE\_FREE**</span></span>
</dt> <dd>

<span data-ttu-id="70159-114">Kostenlose formatbitrate.</span><span class="sxs-lookup"><span data-stu-id="70159-114">Free format bit rate.</span></span> <span data-ttu-id="70159-115">Dies ist eine Konstante Bitrate, die niedriger als die maximal zulässige Bitrate ist.</span><span class="sxs-lookup"><span data-stu-id="70159-115">This is a constant bit rate that is lower than the maximum allowed bit rate.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70159-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70159-116">Requirements</span></span>



| <span data-ttu-id="70159-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70159-117">Requirement</span></span> | <span data-ttu-id="70159-118">Wert</span><span class="sxs-lookup"><span data-stu-id="70159-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="70159-119">Header</span><span class="sxs-lookup"><span data-stu-id="70159-119">Header</span></span><br/> | <dl> <span data-ttu-id="70159-120"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="70159-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70159-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70159-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70159-122">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="70159-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




