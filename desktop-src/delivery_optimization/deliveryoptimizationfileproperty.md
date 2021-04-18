---
title: Deliveryoptimizationfileproperty-Enumeration (deliveryoptimization. h)
description: Die deliveryoptimizationfileproperty-Enumeration gibt die ID einer optionalen Eigenschaft für die do-Datei an.
keywords:
- Deliveryoptimizationfileproperty-Enumeration
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340998"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a>Deliveryoptimizationfileproperty-Enumeration

Die deliveryoptimizationfileproperty-Enumeration gibt die ID einer optionalen Eigenschaft für die do-Datei an. Diese Enumeration wird in der IDeliveryOptimizationFile2-Schnittstelle verwendet, bei der der Eigenschafts Wert des Typs Variant überschritten wird.

## <a name="syntax"></a>Syntax

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a>Konstanten

<dl> <dt>

DOFilePropertyId_DecryptionInfo
</dt> <dd>

Mit der DOFilePropertyId_DecryptionInfo-Eigenschaften-ID werden Entschlüsselungs Informationen in Form einer JSON-Zeichenfolge festgelegt. DOFilePropertyId_DecryptionInfo ist eine schreibgeschützte Eigenschaft vom Typ VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckInfo
</dt> <dd>

Die DOFilePropertyId_IntegrityCheckInfo-Eigenschaften-ID legt den Speicherort der Stück Hash Datei (PHF) fest, der von Do verwendet wird, um Lauf Zeit Integritätsprüfungen für den heruntergeladenen Inhalt auszuführen. DOFilePropertyId_IntegrityCheckInfo ist eine schreibgeschützte Eigenschaft vom Typ VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckMandatory
</dt> <dd>

Mit der DOFilePropertyId_IntegrityCheckMandatory-Eigenschaften-ID wird ein boolesches Flag festgelegt, das angibt, ob die Verwendung der PHF obligatorisch ist. Wenn der Wert true ist, wird der Download abgebrochen, sobald die Integritätsprüfung fehlgeschlagen ist. DOFilePropertyId_IntegrityCheckMandatory ist eine Lese-/Schreibeigenschaft vom Typ VT_BOOL.

</dd> <dt>

DOFilePropertyId_DownloadSinkFilePath
</dt> <dd>

Mit der DOFilePropertyId_DownloadSinkFilePath-Eigenschaften-ID wird ein voll qualifizierter Dateisystem Speicherort festgelegt, in dem die heruntergeladenen Elemente gespeichert werden. DOFilePropertyId_DownloadSinkFilePath ist vom Typ VT_BSTR.

</dd> <dt>

DOFilePropertyId_DownloadSinkMemoryStream
</dt> <dd>

Die DOFilePropertyId_DownloadSinkMemoryStream-Eigenschaften-ID ist veraltet. Darf nicht verwendet werden.

</dd> <dt>

DOFilePropertyId_TotalSizeBytes
</dt> <dd>

Die DOFilePropertyId_TotalSizeBytes-Eigenschaften-ID gibt die Gesamtgröße des Downloads an. DOFilePropertyId_TotalSizeBytes ist vom Typ VT_UI8.
</dd> </dl>

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------|----------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1803, \[ nur Desktop-Apps\]<br/>      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>  |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
