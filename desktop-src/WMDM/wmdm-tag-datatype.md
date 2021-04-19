---
title: WMDM_TAG_DATATYPE-Enumeration
description: Der \_ \_ DataType-Enumerationstyp des WMDM-Tags definiert einen-Datentyp.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- Device Manager der WMDM_TAG_DATATYPE-Enumeration Windows Media
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354037"
---
# <a name="wmdm_tag_datatype-enumeration"></a><span data-ttu-id="cc1d2-104">\_DataType-Enumeration des WMDM-Tags \_</span><span class="sxs-lookup"><span data-stu-id="cc1d2-104">WMDM\_TAG\_DATATYPE enumeration</span></span>

<span data-ttu-id="cc1d2-105">Der **\_ \_ DataType** -Enumerationstyp des WMDM-Tags definiert einen-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="cc1d2-105">The **WMDM\_TAG\_DATATYPE** enumeration type defines a data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc1d2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc1d2-106">Syntax</span></span>


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a><span data-ttu-id="cc1d2-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="cc1d2-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cc1d2-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cc1d2-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="cc1d2-109">Gibt einen 4-Byte- **DWORD** -Wert an.</span><span class="sxs-lookup"><span data-stu-id="cc1d2-109">Specifies a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d2-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cc1d2-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="cc1d2-111">Gibt eine NULL-terminierte Unicode-Zeichenfolge (2 Bytes pro Zeichen) an.</span><span class="sxs-lookup"><span data-stu-id="cc1d2-111">Specifies a null-terminated Unicode string (2 bytes per character).</span></span>

</dd> <dt>

<span data-ttu-id="cc1d2-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM \_ - \_ typbinär Datei**</span><span class="sxs-lookup"><span data-stu-id="cc1d2-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="cc1d2-113">Gibt ein Bytearray an.</span><span class="sxs-lookup"><span data-stu-id="cc1d2-113">Specifies an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d2-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc1d2-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="cc1d2-115">Gibt einen booleschen Wert mit 4 Byte an.</span><span class="sxs-lookup"><span data-stu-id="cc1d2-115">Specifies a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d2-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM- \_ Typ \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="cc1d2-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="cc1d2-117">Gibt einen 8-Byte- **QWORD** -Wert an.</span><span class="sxs-lookup"><span data-stu-id="cc1d2-117">Specifies an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d2-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM- \_ Typ \_ Wort**</span><span class="sxs-lookup"><span data-stu-id="cc1d2-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="cc1d2-119">Gibt einen 2-Byte- **Wort** Wert an.</span><span class="sxs-lookup"><span data-stu-id="cc1d2-119">Specifies a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d2-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM- \_ Typ- \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="cc1d2-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="cc1d2-121">Gibt eine 128-Bit-GUID (16-Byte-GUID) an.</span><span class="sxs-lookup"><span data-stu-id="cc1d2-121">Specifies a 128-bit (16-byte) GUID.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d2-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**Datum des WMDM- \_ Typs \_**</span><span class="sxs-lookup"><span data-stu-id="cc1d2-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM\_TYPE\_DATE**</span></span>
</dt> <dd>

<span data-ttu-id="cc1d2-123">Gibt ein Datum an.</span><span class="sxs-lookup"><span data-stu-id="cc1d2-123">Specifies a date.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc1d2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc1d2-124">Requirements</span></span>



| <span data-ttu-id="cc1d2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc1d2-125">Requirement</span></span> | <span data-ttu-id="cc1d2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="cc1d2-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1d2-127">Header</span><span class="sxs-lookup"><span data-stu-id="cc1d2-127">Header</span></span><br/> | <dl> <span data-ttu-id="cc1d2-128"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cc1d2-128"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc1d2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc1d2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc1d2-130">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="cc1d2-130">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





