---
title: DODownloadPropertyEx-Enumeration
description: Gibt die ID erweiterter Eigenschaften für den Do-Downloadvorgang an.
keywords:
- DODownloadPropertyEx-Enumeration, DODownloadPropertyEx
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
ms.openlocfilehash: f5ec26d845fd6df2bfe0e84fffed0979c39e1971244788c9dfe5ddd3a0c0beca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990380"
---
# <a name="dodownloadpropertyex-enumeration"></a>DODownloadPropertyEx-Enumeration

> [!IMPORTANT]
> Die **DODownloadPropertyEx-Enumeration** ist veraltet. Verwenden Sie stattdessen die [DODownloadProperty-Enumeration](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) mit [IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) und [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).

Die **DODownloadPropertyEx-Enumeration** gibt die ID der erweiterten Eigenschaften für den DO-Downloadvorgang an. Diese Enumeration wird von der **IDODownloadInternal-Schnittstelle** verwendet, und ein **VARIANT-Wert** wird verwendet, um den Eigenschaftswert zu erhalten und zu festlegen.

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
| DODownloadPropertyEx_CorrelationVector | Optional. Legt einen bestimmten Korrelationsvektor für Telemetriezwecke fest. Der VARIANT-Typ VT_BSTR. |
| DODownloadPropertyEx_DecryptionInfo | Reserviert. Darf nicht verwendet werden. |
| DODownloadPropertyEx_IntegrityCheckInfo | Optionaler Schreibzugriff. Legt den Speicherort der Hashdatei (Piece Hash File, PHF) fest, der von DO verwendet wird, um Laufzeitintegritätsprüfungen für den heruntergeladenen Inhalt durchzuführen. Der VARIANT-Typ VT_BSTR. |
| DODownloadPropertyEx_IntegrityCheckMandatory | Optional. Legt ein boolesches Flag fest, das angibt, ob die Verwendung der Stückhashdatei (PHF) obligatorisch ist. Wenn VARIANT_TRUE, wird der Download abgebrochen, sobald die Integritätsprüfung fehlgeschlagen ist. Der VARIANT-Typ VT_BOOL. |
| DODownloadPropertyEx_TotalSizeBytes | Reserviert. Darf nicht verwendet werden. |
| DODownloadPropertyEx_TempLocalFileUsage | Reserviert. Darf nicht verwendet werden. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, version 1809 Win32 applications only (Nur \[ Win32-Anwendungen der Version 1809)\] |
| **Header** | DODownloadInternal.h |
