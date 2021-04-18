---
description: 'Erstellt die anwendungsspezifischen und internen Eigenschaften Daten für ein Bytearray, das zuvor mit icontextnode:: savepropertiesdata erstellt wurde.'
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'Icontextnode:: loadpropertiesdata-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354501"
---
# <a name="icontextnodeloadpropertiesdata-method"></a>Icontextnode:: loadpropertiesdata-Methode

Erstellt die anwendungsspezifischen und internen Eigenschaften Daten für ein Bytearray, das zuvor mit [**icontextnode:: savepropertiesdata**](icontextnode-savepropertiesdata.md)erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cbpropertiesdatasize* \[ in\]
</dt> <dd>

Die Größe des Properties-Daten Arrays.

</dd> <dt>

*pbpropertiesdata* \[ in\]
</dt> <dd>

Das Array von 8-Bit-Ganzzahlen ohne Vorzeichen, das zu ladende Eigenschaften Informationen enthält.

</dd> <dt>

*pferfolgreich* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn die Eigenschaften Daten erfolgreich geladen wurden. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**Icontextnode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Icontextnode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Icontextnode:: savepropertiesdata**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




