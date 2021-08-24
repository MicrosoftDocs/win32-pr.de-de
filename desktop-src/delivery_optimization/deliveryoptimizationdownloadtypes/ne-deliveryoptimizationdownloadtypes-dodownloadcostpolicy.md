---
title: DODownloadCostPolicy-Enumeration
description: Gibt die ID der Kostenrichtlinienoptionen an, die der **eigenschaft DODownloadProperty_CostPolicy** zugeordnet sind.
keywords:
- DODownloadCostPolicy-Enumeration, DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 763042ed6d0df6fa287fbe66d23528a199a73041cb3500c6a2812e6db86cb698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677880"
---
# <a name="dodownloadcostpolicy-enumeration"></a>DODownloadCostPolicy-Enumeration

Die **DODownloadCostPolicy-Enumeration** gibt die ID der Kostenrichtlinienoptionen an, die der **eigenschaft DODownloadProperty_CostPolicy** zugeordnet sind.

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a>Konstanten

| Anforderung | Wert |
|-|-|
| DODownloadCostPolicy_Always | Der Download wird unabhängig von den Kosten ausgeführt. |
| DODownloadCostPolicy_Unrestricted | Der Download wird ausgeführt, es sei denn, kosten- oder datenverkehrseinschränkungen. |
| DODownloadCostPolicy_Standard | Der Download wird ausgeführt, es sei denn, sie unterliegen weder einem Aufschlag noch einer nahezuen Erschöpfung. |
| DODownloadCostPolicy_NoRoaming | Der Download wird ausgeführt, es sei denn, diese Konnektivität unterliegt Roamingzuschlägen. |
| DODownloadCostPolicy_NoSurcharge | Der Download wird ausgeführt, es sei denn, es wird ein Aufschlag berechnet. |
| DODownloadCostPolicy_NoCellular | Der Download wird ausgeführt, es sei denn, das Netzwerk befindet sich im Mobilfunk. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | DeliveryOptimizationDownloadTypes.h |
