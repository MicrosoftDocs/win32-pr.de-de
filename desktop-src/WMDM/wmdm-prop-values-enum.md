---
title: WMDM_PROP_VALUES_ENUM Struktur
description: Die Enum-Struktur der WMDM- \_ Prop- \_ Werte \_ enthält einen Aufzählungs Satz gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352864"
---
# <a name="wmdm_prop_values_enum-structure"></a><span data-ttu-id="d420b-104">Enumerationsstruktur der WMDM- \_ Prop- \_ Werte \_</span><span class="sxs-lookup"><span data-stu-id="d420b-104">WMDM\_PROP\_VALUES\_ENUM structure</span></span>

<span data-ttu-id="d420b-105">Die **\_ \_ \_ enum-Struktur der WMDM-Prop-Werte** enthält einen Aufzählungs Satz gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d420b-105">The **WMDM\_PROP\_VALUES\_ENUM** structure contains an enumerated set of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d420b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d420b-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a><span data-ttu-id="d420b-107">Member</span><span class="sxs-lookup"><span data-stu-id="d420b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d420b-108">**cenum Values**</span><span class="sxs-lookup"><span data-stu-id="d420b-108">**cEnumValues**</span></span>
</dt> <dd>

<span data-ttu-id="d420b-109">Anzahl von Enumerationswerten.</span><span class="sxs-lookup"><span data-stu-id="d420b-109">Count of enumerated values.</span></span>

</dd> <dt>

<span data-ttu-id="d420b-110">**pvalues**</span><span class="sxs-lookup"><span data-stu-id="d420b-110">**pValues**</span></span>
</dt> <dd>

<span data-ttu-id="d420b-111">Zeiger auf ein Array von-Werten.</span><span class="sxs-lookup"><span data-stu-id="d420b-111">Pointer to an array of values.</span></span> <span data-ttu-id="d420b-112">Die Größe des Arrays ist gleich dem Wert von " **cenum Values**".</span><span class="sxs-lookup"><span data-stu-id="d420b-112">The size of the array is equal to the value of **cEnumValues**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d420b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d420b-113">Remarks</span></span>

<span data-ttu-id="d420b-114">Diese Struktur wird in der-Struktur der **WMDM- \_ Prop \_** -Struktur verwendet, um einen enumerierten Satz gültiger Werte zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d420b-114">This structure is used in the **WMDM\_PROP\_DESC** structure to describe an enumerated set of valid values.</span></span> <span data-ttu-id="d420b-115">Ein aufgelisteter Satz gültiger Werte ist anwendbar, wenn \_ \_ \_ \_ \_ die Enumeration für die Enumeration der Werte für die WMDM-Enumeration gültige Werte aus der WMDM-Enumeration gültig ist. **\_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d420b-115">An enumerated set of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration.</span></span>

<span data-ttu-id="d420b-116">Der Aufrufer muss den von **pvalues** verwendeten Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="d420b-116">The caller is required to free the memory used by **pValues**.</span></span> <span data-ttu-id="d420b-117">Ein Beispiel hierfür finden Sie unter [**WMDM- \_ Format \_ Funktion**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="d420b-117">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d420b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d420b-118">Requirements</span></span>



| <span data-ttu-id="d420b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d420b-119">Requirement</span></span> | <span data-ttu-id="d420b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d420b-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d420b-121">Header</span><span class="sxs-lookup"><span data-stu-id="d420b-121">Header</span></span><br/> | <dl> <span data-ttu-id="d420b-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d420b-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d420b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d420b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d420b-124">**IWMDMDevice3:: getformatcapability**</span><span class="sxs-lookup"><span data-stu-id="d420b-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="d420b-125">**\_ \_ \_ Formular für gültige \_ Werte \_ für WMDM-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d420b-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="d420b-126">**WMDM- \_ Format \_ Funktion**</span><span class="sxs-lookup"><span data-stu-id="d420b-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="d420b-127">**WMDM- \_ Prop- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="d420b-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="d420b-128">**WMDM- \_ Prop- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="d420b-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="d420b-129">**Bereich der WMDM- \_ Prop- \_ Werte \_**</span><span class="sxs-lookup"><span data-stu-id="d420b-129">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="d420b-130">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="d420b-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





