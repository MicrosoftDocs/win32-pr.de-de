---
title: DRM_ATTR_DATATYPE-Enumeration (wmdrmsdk. h)
description: Die DRM \_ attr \_ DataType-Enumeration definiert die Datentypen, die für DRM-Attribute und-Eigenschaften verwendet werden.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- DRM_ATTR_DATATYPE-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e684ba1c09a86c65a13adbd189bb185f65598b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371738"
---
# <a name="drm_attr_datatype-enumeration"></a><span data-ttu-id="01617-105">DRM- \_ attr- \_ DataType-Enumeration</span><span class="sxs-lookup"><span data-stu-id="01617-105">DRM\_ATTR\_DATATYPE enumeration</span></span>

<span data-ttu-id="01617-106">Die **DRM \_ attr \_ DataType** -Enumeration definiert die Datentypen, die für DRM-Attribute und-Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01617-106">The **DRM\_ATTR\_DATATYPE** enumeration defines the data types used for DRM attributes and properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01617-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="01617-107">Syntax</span></span>


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="01617-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="01617-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="01617-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="01617-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="01617-110">Die-Eigenschaft ist ein 4-Byte- **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="01617-110">The property is a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="01617-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM \_ - \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01617-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="01617-112">Die-Eigenschaft ist eine NULL-terminierte Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="01617-112">The property is a null-terminated Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="01617-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM \_ - \_ typbinär Datei**</span><span class="sxs-lookup"><span data-stu-id="01617-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="01617-114">Die-Eigenschaft ist ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="01617-114">The property is an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="01617-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="01617-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="01617-116">Die-Eigenschaft ist ein boolescher Wert mit 4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="01617-116">The property is a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="01617-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM- \_ Typ \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="01617-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="01617-118">Die-Eigenschaft ist ein 8-Byte- **QWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="01617-118">The property is an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="01617-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM \_ - \_ typwort**</span><span class="sxs-lookup"><span data-stu-id="01617-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="01617-120">Die-Eigenschaft ist ein 2-Byte- **Wort** Wert.</span><span class="sxs-lookup"><span data-stu-id="01617-120">The property is a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="01617-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM- \_ Typ- \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="01617-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="01617-122">Die-Eigenschaft ist ein 128-Bit-GUID-Wert (6-Byte).</span><span class="sxs-lookup"><span data-stu-id="01617-122">The property is a 128-bit (6-byte) GUID value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01617-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01617-123">Requirements</span></span>



| <span data-ttu-id="01617-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01617-124">Requirement</span></span> | <span data-ttu-id="01617-125">Wert</span><span class="sxs-lookup"><span data-stu-id="01617-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01617-126">Header</span><span class="sxs-lookup"><span data-stu-id="01617-126">Header</span></span><br/> | <dl> <span data-ttu-id="01617-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="01617-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01617-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01617-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01617-129">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="01617-129">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





