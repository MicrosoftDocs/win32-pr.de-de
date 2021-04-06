---
title: Dodownloadpropertyex-Enumeration
description: Gibt die ID der erweiterten Eigenschaften für den Downloadvorgang an.
keywords:
- Dodownloadpropertyex-Enumeration, dodownloadpropertyex
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858966"
---
# <a name="dodownloadpropertyex-enumeration"></a>Dodownloadpropertyex-Enumeration

> [!IMPORTANT]
> Die **dodownloadpropertyex** -Enumeration ist veraltet. Verwenden Sie stattdessen die [dodownloadproperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) -Enumeration mit [idodownload:: GetProperty](../do/nf-do-idodownload-getproperty.md) und [idodownload:: SetProperty](../do/nf-do-idodownload-setproperty.md).

Die **dodownloadpropertyex** -Enumeration gibt die ID der erweiterten Eigenschaften für den Downloadvorgang an. Diese Enumeration wird von der **idodownloadinternal** -Schnittstelle verwendet, und ein **Variant** -Wert wird verwendet, um den Eigenschafts Wert zu erhalten und festzulegen.

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a>Konstanten

| Anforderung | Wert |
|-|-|
| DODownloadPropertyEx_UpdateId | Reserviert. Darf nicht verwendet werden. |
| DODownloadPropertyEx_CorrelationVector | Dies ist optional. Legt einen spezifischen Korrelations Vektor für Telemetriezwecke fest. Der Varianttyp ist VT_BSTR. |
| DODownloadPropertyEx_DecryptionInfo | Reserviert. Darf nicht verwendet werden. |
| DODownloadPropertyEx_IntegrityCheckInfo | Optionaler Schreibzugriff. Legt den Speicherort der Teil Hash Datei (PHF) fest, der von Do verwendet wird, um Lauf Zeit Integritätsprüfungen für den heruntergeladenen Inhalt auszuführen. Der Varianttyp ist VT_BSTR. |
| DODownloadPropertyEx_IntegrityCheckMandatory | Dies ist optional. Legt ein boolesches Flag fest, das angibt, ob die Verwendung der Teil Hash Datei (PHF) obligatorisch ist. Wenn VARIANT_TRUE, wird der Download abgebrochen, sobald die Integritätsprüfung fehlgeschlagen ist. Der Varianttyp ist VT_BOOL. |
| DODownloadPropertyEx_TotalSizeBytes | Reserviert. Darf nicht verwendet werden. |
| DODownloadPropertyEx_TempLocalFileUsage | Reserviert. Darf nicht verwendet werden. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Dodownloadinternal. h |
