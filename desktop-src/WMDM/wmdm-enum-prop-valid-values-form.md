---
title: WMDM_ENUM_PROP_VALID_VALUES_FORM-Enumeration
description: Der Enumerationstyp "der WMDM- \_ \_ \_ \_ Enumerationswert für gültige Werte" \_ beschreibt mögliche Formen gültiger Werte für eine Eigenschaft.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- Device Manager der WMDM_ENUM_PROP_VALID_VALUES_FORM-Enumeration Windows Media
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367536"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a><span data-ttu-id="03d97-104">WMDM- \_ \_ \_ \_ Enumeration gültige Werte \_ Formular Enumeration</span><span class="sxs-lookup"><span data-stu-id="03d97-104">WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM enumeration</span></span>

<span data-ttu-id="03d97-105">Der Enumerationstyp "der **WMDM-Enumerationswert für \_ \_ \_ gültige \_ Werte \_** " beschreibt mögliche Formen gültiger Werte für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="03d97-105">The **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration type describes possible forms of valid values for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d97-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="03d97-106">Syntax</span></span>


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a><span data-ttu-id="03d97-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="03d97-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="03d97-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM- \_ \_ enumerationsprop \_ gültige \_ Werte \_ beliebig**</span><span class="sxs-lookup"><span data-stu-id="03d97-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY**</span></span>
</dt> <dd>

<span data-ttu-id="03d97-109">Alle Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="03d97-109">All values are valid.</span></span>

</dd> <dt>

<span data-ttu-id="03d97-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_ \_ \_ Bereich der gültigen \_ Werte \_ für die WMDM-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="03d97-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="03d97-111">Gültige Werte werden als Bereich ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="03d97-111">Valid values are expressed as a range.</span></span> <span data-ttu-id="03d97-112">Ausführliche Informationen finden Sie in der Struktur von [**WMDM- \_ Prop- \_ Werten \_**](wmdm-prop-values-range.md) .</span><span class="sxs-lookup"><span data-stu-id="03d97-112">For detailed information, see the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="03d97-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**Enumeration \_ \_ \_ gültiger \_ Werte \_ für WMDM-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="03d97-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM**</span></span>
</dt> <dd>

<span data-ttu-id="03d97-114">Gültige Werte sind enumerationssätze.</span><span class="sxs-lookup"><span data-stu-id="03d97-114">Valid values are an enumerated set.</span></span> <span data-ttu-id="03d97-115">Ausführliche Informationen finden Sie in der enumerationsstruktur der [**WMDM- \_ Prop- \_ Werte \_**](wmdm-prop-values-enum.md) .</span><span class="sxs-lookup"><span data-stu-id="03d97-115">For detailed information, see the [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03d97-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03d97-116">Remarks</span></span>

<span data-ttu-id="03d97-117">Diese Enumeration wird in der-Struktur der [**WMDM- \_ Prop \_**](wmdm-prop-desc.md) -Struktur verwendet, um die Form gültiger Werte für eine Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03d97-117">This enumeration is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to specify the form of valid values for a property.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d97-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03d97-118">Requirements</span></span>



| <span data-ttu-id="03d97-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03d97-119">Requirement</span></span> | <span data-ttu-id="03d97-120">Wert</span><span class="sxs-lookup"><span data-stu-id="03d97-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="03d97-121">Header</span><span class="sxs-lookup"><span data-stu-id="03d97-121">Header</span></span><br/> | <dl> <span data-ttu-id="03d97-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03d97-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d97-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03d97-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d97-124">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="03d97-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="03d97-125">**IWMDMDevice3:: getformatcapability**</span><span class="sxs-lookup"><span data-stu-id="03d97-125">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="03d97-126">**WMDM- \_ Format \_ Funktion**</span><span class="sxs-lookup"><span data-stu-id="03d97-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="03d97-127">**WMDM- \_ Prop- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="03d97-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="03d97-128">**WMDM- \_ Prop- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="03d97-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="03d97-129">**WMDM- \_ Prop \_ Values- \_ Enumeration**</span><span class="sxs-lookup"><span data-stu-id="03d97-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="03d97-130">**Bereich der WMDM- \_ Prop- \_ Werte \_**</span><span class="sxs-lookup"><span data-stu-id="03d97-130">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> </dl>

 

 





