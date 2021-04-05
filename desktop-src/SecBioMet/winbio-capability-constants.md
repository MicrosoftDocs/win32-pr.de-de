---
title: WINBIO_CAPABILITY Konstanten (winbio \_ types. h)
description: Untertypen von Fingerabdrucksensoren.
ms.assetid: D447273E-2A02-484E-B0E4-69FEADD15797
topic_type:
- apiref
api_name:
- WINBIO_CAPABILITY_SENSOR
- WINBIO_CAPABILITY_MATCHING
- WINBIO_CAPABILITY_DATABASE
- WINBIO_CAPABILITY_PROCESSING
- WINBIO_CAPABILITY_ENCRYPTION
- WINBIO_CAPABILITY_NAVIGATION
- WINBIO_CAPABILITY_INDICATOR
- WINBIO_CAPABILITY_VIRTUAL_SENSOR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16de3f496e5c3723722bb7aae22c81eb27c968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858918"
---
# <a name="winbio_capability-constants"></a><span data-ttu-id="8da82-103">Winbio-Funktions \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="8da82-103">WINBIO\_CAPABILITY Constants</span></span>

<span data-ttu-id="8da82-104">Die folgenden Untertypen der Fingerabdrucksensoren sind **winbio \_** -Funktions Werte, die als Bitmaske für den *Funktionsparameter* der [**winbio- \_ Einheiten \_ Schema**](winbio-unit-schema.md) Struktur verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8da82-104">The following fingerprint sensor sub types are **WINBIO\_CAPABILITIES** values that can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="8da82-105">Diese Informationen beziehen sich auf die Funktionen des integrierten Sensors.</span><span class="sxs-lookup"><span data-stu-id="8da82-105">These refer to the onboard sensor capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8da82-106">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="8da82-106">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8da82-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8da82-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_SENSOR"></span><span id="winbio_capability_sensor"></span><dl> <span data-ttu-id="8da82-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="8da82-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8da82-109">Der Sensor kann biometrische Daten erfassen.</span><span class="sxs-lookup"><span data-stu-id="8da82-109">The sensor can capture biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_MATCHING"></span><span id="winbio_capability_matching"></span><dl> <span data-ttu-id="8da82-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="8da82-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8da82-111">Der Sensor kann biometrische Daten mit einer Identität vergleichen.</span><span class="sxs-lookup"><span data-stu-id="8da82-111">The sensor can match biometric data to an identity.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_DATABASE"></span><span id="winbio_capability_database"></span><dl> <span data-ttu-id="8da82-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="8da82-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8da82-113">Der Sensor enthält eine integrierte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8da82-113">The sensor contains an onboard database.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_PROCESSING"></span><span id="winbio_capability_processing"></span><dl> <span data-ttu-id="8da82-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="8da82-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8da82-115">Der Sensor kann die biometrische Verarbeitung durchführen.</span><span class="sxs-lookup"><span data-stu-id="8da82-115">The sensor can perform biometric processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_ENCRYPTION"></span><span id="winbio_capability_encryption"></span><dl> <span data-ttu-id="8da82-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="8da82-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8da82-117">Der Sensor kann biometrische Daten verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="8da82-117">The sensor can encrypt biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_NAVIGATION"></span><span id="winbio_capability_navigation"></span><dl> <span data-ttu-id="8da82-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="8da82-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8da82-119">Der Sensor kann als Mauspad fungieren.</span><span class="sxs-lookup"><span data-stu-id="8da82-119">The sensor can act as a mouse pad.</span></span> <span data-ttu-id="8da82-120">Dies wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8da82-120">This is currently not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_INDICATOR"></span><span id="winbio_capability_indicator"></span><dl> <span data-ttu-id="8da82-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="8da82-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8da82-122">Der Sensor enthält ein Indikator Licht.</span><span class="sxs-lookup"><span data-stu-id="8da82-122">The sensor contains an indicator light.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_VIRTUAL_SENSOR"></span><span id="winbio_capability_virtual_sensor"></span><dl> <span data-ttu-id="8da82-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="8da82-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8da82-124">Der Sensor Adapter verwaltet seine eigene Verbindung mit der biometrischen Hardware.</span><span class="sxs-lookup"><span data-stu-id="8da82-124">The sensor adapter manages its own connection to the biometric hardware.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8da82-125">Diese Konstante gilt nur für Windows 10 und höher.</span><span class="sxs-lookup"><span data-stu-id="8da82-125">This constant applies only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="8da82-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8da82-126">Requirements</span></span>



| <span data-ttu-id="8da82-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8da82-127">Requirement</span></span> | <span data-ttu-id="8da82-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8da82-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8da82-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8da82-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8da82-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8da82-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="8da82-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8da82-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8da82-132">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8da82-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                  |
| <span data-ttu-id="8da82-133">Header</span><span class="sxs-lookup"><span data-stu-id="8da82-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8da82-134"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="8da82-134"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da82-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8da82-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da82-136">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="8da82-136">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="8da82-137">**winbio- \_ Einheits \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="8da82-137">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





