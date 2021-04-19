---
title: WMDM_PROP_CONFIG Struktur
description: Die WMDM- \_ Prop- \_ Konfigurations Struktur beschreibt eine Reihe kompatibler Eigenschaftswerte für alle Eigenschaften, die vom Gerät für ein bestimmtes Format unterstützt werden. Diese Struktur enthält eine Reihe von Eigenschafts Beschreibungen in einem Array von WMDM-untergeordneten \_ \_ Strukturen.
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- WMDM_PROP_CONFIG Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369368"
---
# <a name="wmdm_prop_config-structure"></a><span data-ttu-id="18dbe-105">WMDM- \_ Prop- \_ Konfigurations Struktur</span><span class="sxs-lookup"><span data-stu-id="18dbe-105">WMDM\_PROP\_CONFIG structure</span></span>

<span data-ttu-id="18dbe-106">Die **WMDM- \_ Prop- \_ Konfigurations** Struktur beschreibt eine Reihe kompatibler Eigenschaftswerte für alle Eigenschaften, die vom Gerät für ein bestimmtes Format unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="18dbe-106">The **WMDM\_PROP\_CONFIG** structure describes a set of compatible property values across all the properties supported by the device for a particular format.</span></span> <span data-ttu-id="18dbe-107">Diese Struktur enthält eine Reihe von Eigenschafts Beschreibungen in einem Array von [**WMDM-unter \_ \_**](wmdm-prop-desc.md) geordneten Strukturen.</span><span class="sxs-lookup"><span data-stu-id="18dbe-107">This structure contains a number of property descriptions in an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="18dbe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="18dbe-108">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a><span data-ttu-id="18dbe-109">Member</span><span class="sxs-lookup"><span data-stu-id="18dbe-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="18dbe-110">**npreference**</span><span class="sxs-lookup"><span data-stu-id="18dbe-110">**nPreference**</span></span>
</dt> <dd>

<span data-ttu-id="18dbe-111">Die bevorzugte Ebene des Geräts für diese Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="18dbe-111">Device's level of preference for this configuration.</span></span> <span data-ttu-id="18dbe-112">Der niedrigste Wert gibt die bevorzugte Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="18dbe-112">The lowest value indicates the most preferred configuration.</span></span>

</dd> <dt>

<span data-ttu-id="18dbe-113">**npropentsc**</span><span class="sxs-lookup"><span data-stu-id="18dbe-113">**nPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="18dbe-114">Anzahl der Eigenschafts Beschreibungen, die in dieser Konfiguration enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="18dbe-114">Number of property descriptions contained in this configuration.</span></span> <span data-ttu-id="18dbe-115">Für jede Eigenschaft, die für das angegebene Format unterstützt wird, gibt es eine einzelne Eigenschafts Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="18dbe-115">There is a single property description for each property supported for the specified format.</span></span>

</dd> <dt>

<span data-ttu-id="18dbe-116">**ppropentsc**</span><span class="sxs-lookup"><span data-stu-id="18dbe-116">**pPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="18dbe-117">Zeiger auf ein Array von [**WMDM \_ \_**](wmdm-prop-desc.md) -untergeordneten Strukturen, die Eigenschafts Beschreibungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="18dbe-117">Pointer to an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures containing property descriptions.</span></span> <span data-ttu-id="18dbe-118">Die Größe des Arrays ist gleich dem Wert von **npropde SC**.</span><span class="sxs-lookup"><span data-stu-id="18dbe-118">The size of the array is equal to the value of **nPropDesc**.</span></span> <span data-ttu-id="18dbe-119">Die Anwendung muss diesen Arbeitsspeicher freigeben, wenn Sie damit fertig ist.</span><span class="sxs-lookup"><span data-stu-id="18dbe-119">The application must free this memory when finished with it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18dbe-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18dbe-120">Remarks</span></span>

<span data-ttu-id="18dbe-121">Die von [**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) für ein bestimmtes Format zurückgegebene [**WMDM- \_ Format \_**](wmdm-format-capability.md) Funktionsstruktur besteht aus einer Reihe von Eigenschafts Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="18dbe-121">The [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) for a particular format consists of a number of property configurations.</span></span> <span data-ttu-id="18dbe-122">**WMDM \_ Diese \_** Konfigurationen werden von der prop-Konfigurations Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="18dbe-122">**WMDM\_PROP\_CONFIG** structures describe those configurations.</span></span>

<span data-ttu-id="18dbe-123">Eine Eigenschaften Konfiguration beschreibt Werte für alle Eigenschaften, die für ein bestimmtes Format unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="18dbe-123">A property configuration describes values for all the properties supported for a given format.</span></span> <span data-ttu-id="18dbe-124">Die Werte verschiedener Eigenschaften in einer einzelnen Konfiguration sind miteinander kompatibel.</span><span class="sxs-lookup"><span data-stu-id="18dbe-124">The values of different properties in a single configuration are compatible with each other.</span></span> <span data-ttu-id="18dbe-125">Beispielsweise enthält eine Konfiguration für eine Audiodatei gültige Werte der Samplingrate und gültige Werte der Bitrate, sodass alle Kombinationen dieser Stichproben-und Bitraten auf dem Gerät wiedergegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="18dbe-125">For example, for an audio file, a configuration will include valid values of sample rate and valid values of the bit rate such that all combinations of these sample and bit rates can be played on the device.</span></span>

<span data-ttu-id="18dbe-126">Der Aufrufer muss den von **ppropde** genutzten Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="18dbe-126">The caller is required to free the memory used by **pPropDesc**.</span></span> <span data-ttu-id="18dbe-127">Ein Beispiel hierfür finden Sie unter [**WMDM- \_ Format \_ Funktion**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="18dbe-127">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18dbe-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18dbe-128">Requirements</span></span>



| <span data-ttu-id="18dbe-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18dbe-129">Requirement</span></span> | <span data-ttu-id="18dbe-130">Wert</span><span class="sxs-lookup"><span data-stu-id="18dbe-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="18dbe-131">Header</span><span class="sxs-lookup"><span data-stu-id="18dbe-131">Header</span></span><br/> | <dl> <span data-ttu-id="18dbe-132"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18dbe-132"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18dbe-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18dbe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18dbe-134">**IWMDMDevice3:: getformatcapability**</span><span class="sxs-lookup"><span data-stu-id="18dbe-134">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="18dbe-135">**\_ \_ \_ Formular für gültige \_ Werte \_ für WMDM-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="18dbe-135">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="18dbe-136">**WMDM- \_ Format \_ Funktion**</span><span class="sxs-lookup"><span data-stu-id="18dbe-136">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="18dbe-137">**WMDM- \_ Prop- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="18dbe-137">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="18dbe-138">**WMDM- \_ Prop \_ Values- \_ Enumeration**</span><span class="sxs-lookup"><span data-stu-id="18dbe-138">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="18dbe-139">**Bereich der WMDM- \_ Prop- \_ Werte \_**</span><span class="sxs-lookup"><span data-stu-id="18dbe-139">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="18dbe-140">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="18dbe-140">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





