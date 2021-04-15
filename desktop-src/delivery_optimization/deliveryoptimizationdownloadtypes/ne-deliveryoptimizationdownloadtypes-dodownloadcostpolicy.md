---
title: Dodownloadcostpolicy-Enumeration
description: Gibt die ID der Kosten Richtlinien Optionen an, die mit der **DODownloadProperty_CostPolicy** Eigenschaft verknüpft sind.
keywords:
- Dodownloadcostpolicy-Enumeration, dodownloadcostpolicy
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
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391582"
---
# <a name="dodownloadcostpolicy-enumeration"></a>Dodownloadcostpolicy-Enumeration

Die **dodownloadcostpolicy** -Enumeration gibt die ID der Kosten Richtlinien Optionen an, die mit der **DODownloadProperty_CostPolicy** -Eigenschaft verknüpft sind.

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
| DODownloadCostPolicy_Unrestricted | Download Ausführungen, es sei denn, Sie erzwingen Kosten oder Datenverkehrs Limits |
| DODownloadCostPolicy_Standard | Der Download wird ausgeführt, es sei denn, es gibt keine Zuschläge und keine beinahe-Erschöpfung |
| DODownloadCostPolicy_NoRoaming | Download wird ausgeführt, es sei denn, die Konnektivität unterliegt roamingzuschläge |
| DODownloadCostPolicy_NoSurcharge | Download wird ausgeführt, es sei denn, es wird ein Zuschlag |
| DODownloadCostPolicy_NoCellular | Der Download wird ausgeführt, es sei denn, das Netzwerk ist |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Deliveryoptimizationdownloadtypes. h |
