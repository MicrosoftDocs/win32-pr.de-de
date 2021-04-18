---
title: WMDM_PROP_DESC Struktur
description: Die WMDM- \_ Prop- \_ DESC-Struktur beschreibt gültige Werte einer Eigenschaft in einer bestimmten Eigenschaften Konfiguration.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- WMDM_PROP_DESC Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354749"
---
# <a name="wmdm_prop_desc-structure"></a><span data-ttu-id="48010-104">WMDM- \_ Prop- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="48010-104">WMDM\_PROP\_DESC structure</span></span>

<span data-ttu-id="48010-105">Die **WMDM- \_ Prop- \_ DESC** -Struktur beschreibt gültige Werte einer Eigenschaft in einer bestimmten Eigenschaften Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="48010-105">The **WMDM\_PROP\_DESC** structure describes valid values of a property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="48010-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="48010-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a><span data-ttu-id="48010-107">Member</span><span class="sxs-lookup"><span data-stu-id="48010-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="48010-108">**pwszpropname**</span><span class="sxs-lookup"><span data-stu-id="48010-108">**pwszPropName**</span></span>
</dt> <dd>

<span data-ttu-id="48010-109">Der Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="48010-109">Name of the property.</span></span> <span data-ttu-id="48010-110">Die Anwendung muss diesen Arbeitsspeicher freigeben, wenn Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="48010-110">The application must free this memory when it is done using it.</span></span>

</dd> <dt>

<span data-ttu-id="48010-111">**Validvaluesform**</span><span class="sxs-lookup"><span data-stu-id="48010-111">**ValidValuesForm**</span></span>
</dt> <dd>

<span data-ttu-id="48010-112">Ein WMDM-Enumerationswert [**\_ \_ \_ gültige \_ Werte \_ Formular**](wmdm-enum-prop-valid-values-form.md) Enumerationswert, der den Typ der Werte beschreibt, z. b. einen Bereich oder eine Liste.</span><span class="sxs-lookup"><span data-stu-id="48010-112">An [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration value describing the type of values, such as a range or list.</span></span> <span data-ttu-id="48010-113">Der Wert dieser Enumeration bestimmt, welche Member-Variable verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="48010-113">The value of this enumeration determines which member variable is used.</span></span>

</dd> <dt>

<span data-ttu-id="48010-114">**ValidValues**</span><span class="sxs-lookup"><span data-stu-id="48010-114">**ValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="48010-115">Enthält die gültigen Werte der-Eigenschaft in einer bestimmten Eigenschaften Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="48010-115">Holds the valid values of the property in a particular property configuration.</span></span> <span data-ttu-id="48010-116">Dieser Member enthält eines von drei Elementen: den Enumerationswert WMDM- \_ \_ \_ \_ \_ enumerationsprop gültige Werte any, den Member **validvaluesrange** oder den **enumeratedvalidvalues**-Member.</span><span class="sxs-lookup"><span data-stu-id="48010-116">This member holds one of three items: the enumeration value WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY; the member **ValidValuesRange**; or the member **EnumeratedValidValues**.</span></span> <span data-ttu-id="48010-117">Der Wert oder Member wird durch **validvaluesform** angegeben.</span><span class="sxs-lookup"><span data-stu-id="48010-117">The value or member is indicated by **ValidValuesForm**.</span></span>

<dl> <dt>

<span data-ttu-id="48010-118">**Validvaluesrange**</span><span class="sxs-lookup"><span data-stu-id="48010-118">**ValidValuesRange**</span></span>
</dt> <dd>

<span data-ttu-id="48010-119">Eine [**WMDM \_ - \_ Werte \_ Bereichs**](wmdm-prop-values-range.md) Struktur, die einen Bereich gültiger Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="48010-119">A [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure containing a range of valid values.</span></span> <span data-ttu-id="48010-120">Diese ist nur vorhanden, wenn **validvaluesform** auf den \_ \_ \_ gültigen \_ Werte \_ Bereich der WMDM-Enumeration festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="48010-120">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE.</span></span> <span data-ttu-id="48010-121">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="48010-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="48010-122">**Enumeratedvalidvalues**</span><span class="sxs-lookup"><span data-stu-id="48010-122">**EnumeratedValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="48010-123">Eine enumerationsstruktur mit [**WMDM- \_ Prop- \_ Werten \_**](wmdm-prop-values-enum.md) , die einen aufgelisteten Satz gültiger Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="48010-123">A [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure containing an enumerated set of valid values.</span></span> <span data-ttu-id="48010-124">Diese ist nur vorhanden, wenn für **validvaluesform** die Enumeration \_ \_ \_ gültige \_ Values-Enumeration festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="48010-124">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM.</span></span> <span data-ttu-id="48010-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="48010-125">See Remarks.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48010-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48010-126">Remarks</span></span>

<span data-ttu-id="48010-127">Die **WMDM- \_ Prop- \_ DESC** -Struktur enthält eine Eigenschafts Beschreibung, die aus einem Eigenschaftsnamen und den gültigen Werten in einer bestimmten Konfiguration besteht.</span><span class="sxs-lookup"><span data-stu-id="48010-127">The **WMDM\_PROP\_DESC** structure contains a property description that consists of a property name and its valid values in a particular configuration.</span></span>

<span data-ttu-id="48010-128">Der Aufrufer muss den von **validvaluesrange** oder **enumeratedvalues** genutzten Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="48010-128">The caller is required to free the memory used by **ValidValuesRange** or **EnumeratedValues**.</span></span> <span data-ttu-id="48010-129">Ein Beispiel hierfür finden Sie unter [**WMDM- \_ Format \_ Funktion**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="48010-129">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48010-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48010-130">Requirements</span></span>



| <span data-ttu-id="48010-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48010-131">Requirement</span></span> | <span data-ttu-id="48010-132">Wert</span><span class="sxs-lookup"><span data-stu-id="48010-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="48010-133">Header</span><span class="sxs-lookup"><span data-stu-id="48010-133">Header</span></span><br/> | <dl> <span data-ttu-id="48010-134"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48010-134"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48010-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48010-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48010-136">**IWMDMDevice3:: getformatcapability**</span><span class="sxs-lookup"><span data-stu-id="48010-136">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="48010-137">**\_ \_ \_ Formular für gültige \_ Werte \_ für WMDM-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="48010-137">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="48010-138">**WMDM- \_ Format \_ Funktion**</span><span class="sxs-lookup"><span data-stu-id="48010-138">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="48010-139">**WMDM- \_ Prop- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="48010-139">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="48010-140">**WMDM- \_ Prop \_ Values- \_ Enumeration**</span><span class="sxs-lookup"><span data-stu-id="48010-140">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="48010-141">**Bereich der WMDM- \_ Prop- \_ Werte \_**</span><span class="sxs-lookup"><span data-stu-id="48010-141">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="48010-142">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="48010-142">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





