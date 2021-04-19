---
title: WMDM_PROP_VALUES_RANGE Struktur
description: Die Bereichs Struktur der WMDM- \_ Prop- \_ Werte \_ beschreibt einen Bereich gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356351"
---
# <a name="wmdm_prop_values_range-structure"></a><span data-ttu-id="e2a35-104">Bereichs Struktur der WMDM- \_ Prop- \_ Werte \_</span><span class="sxs-lookup"><span data-stu-id="e2a35-104">WMDM\_PROP\_VALUES\_RANGE structure</span></span>

<span data-ttu-id="e2a35-105">Die **Bereichs Struktur der WMDM- \_ Prop- \_ Werte \_** beschreibt einen Bereich gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e2a35-105">The **WMDM\_PROP\_VALUES\_RANGE** structure describes a range of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a35-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2a35-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a><span data-ttu-id="e2a35-107">Member</span><span class="sxs-lookup"><span data-stu-id="e2a35-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2a35-108">**rangeMin**</span><span class="sxs-lookup"><span data-stu-id="e2a35-108">**rangeMin**</span></span>
</dt> <dd>

<span data-ttu-id="e2a35-109">Minimalwert im Bereich.</span><span class="sxs-lookup"><span data-stu-id="e2a35-109">Minimum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="e2a35-110">**rangeMax**</span><span class="sxs-lookup"><span data-stu-id="e2a35-110">**rangeMax**</span></span>
</dt> <dd>

<span data-ttu-id="e2a35-111">Maximalwert im Bereich.</span><span class="sxs-lookup"><span data-stu-id="e2a35-111">Maximum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="e2a35-112">**rangestep**</span><span class="sxs-lookup"><span data-stu-id="e2a35-112">**rangeStep**</span></span>
</dt> <dd>

<span data-ttu-id="e2a35-113">Die Schrittgröße, in der gültige Werte von dem Minimalwert auf den maximalen Wert erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="e2a35-113">The step size in which valid values increment from the minimum value to the maximum value.</span></span> <span data-ttu-id="e2a35-114">Dies ermöglicht die Angabe diskreter zulässiger Werte in einem Bereich.</span><span class="sxs-lookup"><span data-stu-id="e2a35-114">This permits specifying discrete permissible values in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2a35-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2a35-115">Remarks</span></span>

<span data-ttu-id="e2a35-116">Diese Struktur wird in der-Struktur der [**WMDM- \_ Prop \_**](wmdm-prop-desc.md) -Struktur verwendet, um einen Bereich gültiger Werte zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e2a35-116">This structure is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to describe a range of valid values.</span></span> <span data-ttu-id="e2a35-117">Ein Bereich gültiger Werte ist anwendbar, wenn die Enumeration "gültige Werte für WMDM-Enumerationswerte" \_ \_ \_ \_ \_ aus der Enumeration "gültige Werte" der WMDM-Enumeration ausgewählt wird. [**\_ \_ \_ \_ \_**](wmdm-enum-prop-valid-values-form.md)</span><span class="sxs-lookup"><span data-stu-id="e2a35-117">A range of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2a35-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2a35-118">Requirements</span></span>



| <span data-ttu-id="e2a35-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2a35-119">Requirement</span></span> | <span data-ttu-id="e2a35-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e2a35-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a35-121">Header</span><span class="sxs-lookup"><span data-stu-id="e2a35-121">Header</span></span><br/> | <dl> <span data-ttu-id="e2a35-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2a35-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a35-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2a35-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a35-124">**IWMDMDevice3:: getformatcapability**</span><span class="sxs-lookup"><span data-stu-id="e2a35-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="e2a35-125">**\_ \_ \_ Formular für gültige \_ Werte \_ für WMDM-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e2a35-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="e2a35-126">**WMDM- \_ Format \_ Funktion**</span><span class="sxs-lookup"><span data-stu-id="e2a35-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="e2a35-127">**WMDM- \_ Prop- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="e2a35-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="e2a35-128">**WMDM- \_ Prop- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="e2a35-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="e2a35-129">**WMDM- \_ Prop \_ Values- \_ Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e2a35-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="e2a35-130">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="e2a35-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





