---
description: Stellt die unformatierten Daten aus einer durch VESA erweiterten, erweiterten Display Identification Data (E-EDID)-Struktur dar.
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: WmiMonitorRawEEdidV1Block-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359124"
---
# <a name="wmimonitorraweedidv1block-class"></a><span data-ttu-id="4b7c5-103">WmiMonitorRawEEdidV1Block-Klasse</span><span class="sxs-lookup"><span data-stu-id="4b7c5-103">WmiMonitorRawEEdidV1Block class</span></span>

<span data-ttu-id="4b7c5-104">Die **WmiMonitorRawEEdidV1Block** -WMI-Klasse stellt die unformatierten Daten aus einer durch VESA verbesserten, erweiterten Display Identification Data (E-EDID)-Struktur dar.</span><span class="sxs-lookup"><span data-stu-id="4b7c5-104">The **WmiMonitorRawEEdidV1Block** WMI class represents the raw data from a Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span> <span data-ttu-id="4b7c5-105">Diese 128-Byte-Datenstruktur enthält Informationen, die die optimale Konfiguration für eine Anzeige beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4b7c5-105">This 128-byte data structure contains information that describes the optimal configuration for a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b7c5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b7c5-106">Syntax</span></span>

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a><span data-ttu-id="4b7c5-107">Member</span><span class="sxs-lookup"><span data-stu-id="4b7c5-107">Members</span></span>

<span data-ttu-id="4b7c5-108">Die **WmiMonitorRawEEdidV1Block** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4b7c5-108">The **WmiMonitorRawEEdidV1Block** class has these types of members:</span></span>

-   [<span data-ttu-id="4b7c5-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b7c5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b7c5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b7c5-110">Properties</span></span>

<span data-ttu-id="4b7c5-111">Die **WmiMonitorRawEEdidV1Block** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4b7c5-111">The **WmiMonitorRawEEdidV1Block** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b7c5-112">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b7c5-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4b7c5-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4b7c5-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4b7c5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b7c5-115">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="4b7c5-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="4b7c5-116">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-116">**Content**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b7c5-117">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="4b7c5-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4b7c5-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4b7c5-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b7c5-119">128 Bytearray, das den Rohdaten Block Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="4b7c5-119">128 byte array that contains the raw block content.</span></span>

</dd> <dt>

<span data-ttu-id="4b7c5-120">**Id**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-120">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b7c5-121">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4b7c5-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4b7c5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b7c5-123">Die Identität des Datenblocks.</span><span class="sxs-lookup"><span data-stu-id="4b7c5-123">Identity of the data block.</span></span>

</dd> <dt>

<span data-ttu-id="4b7c5-124">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-124">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b7c5-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b7c5-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4b7c5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b7c5-127">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-127">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4b7c5-128">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="4b7c5-128">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="4b7c5-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-129">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b7c5-130">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-130">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4b7c5-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4b7c5-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b7c5-132">Der Typ des Datenblocks.</span><span class="sxs-lookup"><span data-stu-id="4b7c5-132">Type of data block.</span></span> <span data-ttu-id="4b7c5-133">In der folgenden Tabelle sind mögliche Werte aufgeführt, die zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="4b7c5-133">The following table lists possible values that can be returned.</span></span>



| <span data-ttu-id="4b7c5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4b7c5-134">Value</span></span>                                                                                 | <span data-ttu-id="4b7c5-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4b7c5-135">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="4b7c5-136"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4b7c5-136"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="4b7c5-137">Uninitialized</span><span class="sxs-lookup"><span data-stu-id="4b7c5-137">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="4b7c5-138"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="4b7c5-138"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="4b7c5-139">EDID-Basisblock</span><span class="sxs-lookup"><span data-stu-id="4b7c5-139">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="4b7c5-140"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="4b7c5-140"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="4b7c5-141">EDID-Block Zuordnung</span><span class="sxs-lookup"><span data-stu-id="4b7c5-141">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="4b7c5-142"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="4b7c5-142"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="4b7c5-143">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="4b7c5-143">Other</span></span><br/>           |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b7c5-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b7c5-144">Requirements</span></span>



| <span data-ttu-id="4b7c5-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b7c5-145">Requirement</span></span> | <span data-ttu-id="4b7c5-146">Wert</span><span class="sxs-lookup"><span data-stu-id="4b7c5-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b7c5-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b7c5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4b7c5-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b7c5-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4b7c5-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b7c5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4b7c5-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b7c5-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4b7c5-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b7c5-151">Namespace</span></span><br/>                | <span data-ttu-id="4b7c5-152">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="4b7c5-152">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="4b7c5-153">MOF</span><span class="sxs-lookup"><span data-stu-id="4b7c5-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b7c5-154"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4b7c5-154"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b7c5-155">DLL</span><span class="sxs-lookup"><span data-stu-id="4b7c5-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b7c5-156"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b7c5-156"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b7c5-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b7c5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b7c5-158">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-158">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="4b7c5-159">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="4b7c5-159">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




