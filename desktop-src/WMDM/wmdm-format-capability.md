---
title: WMDM_FORMAT_CAPABILITY Struktur
description: Die Funktionsstruktur des WMDM- \_ Formats \_ beschreibt die Funktionen eines Geräts für ein bestimmtes Format.
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- WMDM_FORMAT_CAPABILITY Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367558"
---
# <a name="wmdm_format_capability-structure"></a><span data-ttu-id="81844-104">Struktur der WMDM- \_ Format \_ Funktion</span><span class="sxs-lookup"><span data-stu-id="81844-104">WMDM\_FORMAT\_CAPABILITY structure</span></span>

<span data-ttu-id="81844-105">Die Funktionsstruktur des **WMDM- \_ Formats \_** beschreibt die Funktionen eines Geräts für ein bestimmtes Format.</span><span class="sxs-lookup"><span data-stu-id="81844-105">The **WMDM\_FORMAT\_CAPABILITY** structure describes the capabilities of a device for a particular format.</span></span> <span data-ttu-id="81844-106">Diese Struktur enthält eine Reihe von Eigenschaften Konfigurationen in einem Array von **WMDM- \_ Prop- \_ Konfigurations** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="81844-106">This structure contains a set of property configurations in an array of **WMDM\_PROP\_CONFIG** structures.</span></span> <span data-ttu-id="81844-107">Jede Eigenschaften Konfiguration stellt einen Satz kompatibler Eigenschaftswerte für alle Eigenschaften dar, die für ein bestimmtes Format unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="81844-107">Each property configuration represents a set of compatible property values across all the properties supported for a given format.</span></span> <span data-ttu-id="81844-108">Die Anwendung kann diese Struktur abrufen, indem Sie die **IWMDMDevice3:: getformatcapability** -Methode aufruft und den Format Code übergibt.</span><span class="sxs-lookup"><span data-stu-id="81844-108">The application can get this structure by calling the **IWMDMDevice3::GetFormatCapability** method and passing in the format code.</span></span> <span data-ttu-id="81844-109">Eine Liste der Formatcodes finden Sie unter [**WMDM \_ Formatcode**](wmdm-formatcode.md).</span><span class="sxs-lookup"><span data-stu-id="81844-109">For a list of format codes, see [**WMDM\_FORMATCODE**](wmdm-formatcode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="81844-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="81844-110">Syntax</span></span>


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a><span data-ttu-id="81844-111">Member</span><span class="sxs-lookup"><span data-stu-id="81844-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="81844-112">**npropconfig**</span><span class="sxs-lookup"><span data-stu-id="81844-112">**nPropConfig**</span></span>
</dt> <dd>

<span data-ttu-id="81844-113">Anzahl der Eigenschafts Konfigurationen im **pconfigs** -Array.</span><span class="sxs-lookup"><span data-stu-id="81844-113">Number of property configurations in the **pConfigs** array.</span></span>

</dd> <dt>

<span data-ttu-id="81844-114">**pconfigs**</span><span class="sxs-lookup"><span data-stu-id="81844-114">**pConfigs**</span></span>
</dt> <dd>

<span data-ttu-id="81844-115">Zeiger auf ein Array von [**WMDM- \_ Prop- \_ Konfigurations**](wmdm-prop-config.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="81844-115">Pointer to an array of [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures.</span></span> <span data-ttu-id="81844-116">Die Größe des Arrays ist gleich dem Wert von **npropconfig**.</span><span class="sxs-lookup"><span data-stu-id="81844-116">The size of array is equal to the value of **nPropConfig**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81844-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81844-117">Remarks</span></span>

<span data-ttu-id="81844-118">Die Struktur der **WMDM- \_ Format \_ Funktionen** bietet einen flexiblen Mechanismus zum Ausdrücken der Funktionen des Geräts für ein bestimmtes Format.</span><span class="sxs-lookup"><span data-stu-id="81844-118">The **WMDM\_FORMAT\_CAPABILITY** structure provides a flexible mechanism to express the capabilities of the device for a particular format.</span></span>

<span data-ttu-id="81844-119">Wenn der Inhalt vom Gerät gerendert werden soll (z. b. eine Audiodatei, die vom Gerät abgespielt werden soll), müssen die Eigenschaften des Inhalts einer der Eigenschafts Konfigurationen entsprechen, die von [**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) in der Funktionsstruktur des **WMDM- \_ Formats \_** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="81844-119">If the content is meant to be rendered by the device (for example, an audio file to be played by the device), the properties of the content must match one of the property configurations returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) in the **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="81844-120">Beispielsweise müssen für eine Audiodatei die Bitrate und die Samplingrate eine der zurückgegebenen Eigenschafts Konfigurationen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="81844-120">For example, for an audio file, the bit rate and sample rate must satisfy one of the property configurations returned.</span></span>

<span data-ttu-id="81844-121">Der Aufrufer ist dafür verantwortlich, den für diese Struktur zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="81844-121">The caller is responsible for freeing the memory allocated for this structure.</span></span> <span data-ttu-id="81844-122">Die folgende Funktion veranschaulicht, wie Sie eine Funktionsstruktur des **WMDM- \_ Formats \_** löschen.</span><span class="sxs-lookup"><span data-stu-id="81844-122">The following function demonstrates how to clear a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



## <a name="requirements"></a><span data-ttu-id="81844-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81844-123">Requirements</span></span>



| <span data-ttu-id="81844-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81844-124">Requirement</span></span> | <span data-ttu-id="81844-125">Wert</span><span class="sxs-lookup"><span data-stu-id="81844-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="81844-126">Header</span><span class="sxs-lookup"><span data-stu-id="81844-126">Header</span></span><br/> | <dl> <span data-ttu-id="81844-127"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81844-127"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81844-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81844-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81844-129">**IWMDMDevice3:: getformatcapability**</span><span class="sxs-lookup"><span data-stu-id="81844-129">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="81844-130">**\_ \_ \_ Formular für gültige \_ Werte \_ für WMDM-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="81844-130">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="81844-131">**WMDM- \_ Prop- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="81844-131">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="81844-132">**WMDM- \_ Prop- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="81844-132">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="81844-133">**WMDM- \_ Prop \_ Values- \_ Enumeration**</span><span class="sxs-lookup"><span data-stu-id="81844-133">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="81844-134">**Bereich der WMDM- \_ Prop- \_ Werte \_**</span><span class="sxs-lookup"><span data-stu-id="81844-134">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="81844-135">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="81844-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





