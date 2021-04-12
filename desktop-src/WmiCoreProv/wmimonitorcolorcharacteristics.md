---
description: Stellt die Farbmerkmale der International Commission on Illumination (CIE) eines Computermonitors dar.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Wmimonitorcolorcharacteristics-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346508"
---
# <a name="wmimonitorcolorcharacteristics-class"></a><span data-ttu-id="1d413-103">Wmimonitorcolorcharacteristics-Klasse</span><span class="sxs-lookup"><span data-stu-id="1d413-103">WmiMonitorColorCharacteristics class</span></span>

<span data-ttu-id="1d413-104">Die **wmimonitorcolorcharacteristics** -Klasse stellt die Farbmerkmale der International Commission on Illumination (CIE) eines Computermonitors dar.</span><span class="sxs-lookup"><span data-stu-id="1d413-104">The **WmiMonitorColorCharacteristics** class represents the International Commission on Illumination (CIE) color characteristics of a computer monitor.</span></span> <span data-ttu-id="1d413-105">Die Daten entsprechen den Daten im Block Color Characteristics der "Video Electronics Standard Association (VESA) Enhanced Enhanced Display Identification Data (E-EDID)"-Struktur.</span><span class="sxs-lookup"><span data-stu-id="1d413-105">The data corresponds to data in the Color Characteristics block of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d413-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d413-106">Syntax</span></span>

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a><span data-ttu-id="1d413-107">Member</span><span class="sxs-lookup"><span data-stu-id="1d413-107">Members</span></span>

<span data-ttu-id="1d413-108">Die **wmimonitorcolorcharacteristics** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1d413-108">The **WmiMonitorColorCharacteristics** class has these types of members:</span></span>

-   [<span data-ttu-id="1d413-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d413-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d413-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d413-110">Properties</span></span>

<span data-ttu-id="1d413-111">Die **wmimonitorcolorproperties** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d413-111">The **WmiMonitorColorCharacteristics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d413-112">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="1d413-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d413-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1d413-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d413-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d413-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d413-115">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="1d413-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="1d413-116">**Blau**</span><span class="sxs-lookup"><span data-stu-id="1d413-116">**Blue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d413-117">Datentyp: **[ **xyzincie**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="1d413-117">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1d413-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d413-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d413-119">CIE-Koordinaten für blau, dargestellt durch eine Instanz der [**xyzincie**](xyzincie.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="1d413-119">CIE coordinates for blue, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1d413-120">**Defaultweiß**</span><span class="sxs-lookup"><span data-stu-id="1d413-120">**DefaultWhite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d413-121">Datentyp: **[ **xyzincie**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="1d413-121">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1d413-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d413-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d413-123">Standardmäßige weiße CIE-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="1d413-123">Default white CIE coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="1d413-124">**Grün**</span><span class="sxs-lookup"><span data-stu-id="1d413-124">**Green**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d413-125">Datentyp: **[ **xyzincie**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="1d413-125">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1d413-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d413-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d413-127">CIE-Koordinaten für Grün, dargestellt durch eine Instanz der [**xyzincie**](xyzincie.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="1d413-127">CIE coordinates for green, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1d413-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1d413-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d413-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d413-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d413-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d413-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d413-131">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1d413-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1d413-132">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="1d413-132">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="1d413-133">**Rot**</span><span class="sxs-lookup"><span data-stu-id="1d413-133">**Red**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d413-134">Datentyp: **[ **xyzincie**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="1d413-134">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1d413-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d413-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d413-136">CIE-Koordinaten für Rot, dargestellt durch eine Instanz der [**xyzincie**](xyzincie.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="1d413-136">CIE coordinates for red, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d413-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d413-137">Remarks</span></span>

<span data-ttu-id="1d413-138">Die Werte von "Chromaticity" und "White Point" werden mithilfe eines Codierungs Formats als Bruchzahlen ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="1d413-138">The chromaticity and white point values are expressed as fractional numbers using an encoding format.</span></span> <span data-ttu-id="1d413-139">Dieses Format ist mit dem Tausendstel der Länge von 10 Bits genau.</span><span class="sxs-lookup"><span data-stu-id="1d413-139">This format is accurate to the thousandth place, which is 10 bits in length.</span></span> <span data-ttu-id="1d413-140">Das signifikanteste Bit (MSB) repräsentiert 2 ^-1, und das unwichtigste Bit (LSB) stellt 2 ^-10 Koeffizienten dar.</span><span class="sxs-lookup"><span data-stu-id="1d413-140">The most significant bit (MSB) represents 2^-1 and the least significant bit (LSB) represents 2^-10 coefficients, respectively.</span></span> <span data-ttu-id="1d413-141">Die Genauigkeit der gespeicherten Werte in der E-EDID v1. x-Struktur sollte auf +/-0,005 des tatsächlichen Werts zutreffen.</span><span class="sxs-lookup"><span data-stu-id="1d413-141">Precision of the stored values in the E-EDID v1.x structure should be accurate to +/- 0.005 of the actual value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d413-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d413-142">Requirements</span></span>



| <span data-ttu-id="1d413-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d413-143">Requirement</span></span> | <span data-ttu-id="1d413-144">Wert</span><span class="sxs-lookup"><span data-stu-id="1d413-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d413-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d413-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1d413-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d413-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1d413-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d413-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1d413-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d413-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1d413-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d413-149">Namespace</span></span><br/>                | <span data-ttu-id="1d413-150">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="1d413-150">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1d413-151">MOF</span><span class="sxs-lookup"><span data-stu-id="1d413-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d413-152"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1d413-152"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d413-153">DLL</span><span class="sxs-lookup"><span data-stu-id="1d413-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d413-154"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d413-154"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d413-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d413-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d413-156">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="1d413-156">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




