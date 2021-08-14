---
description: Erstellt die anwendungsspezifischen und internen Eigenschaftsdaten für ein Bytearray neu, das zuvor mit IContextNode::SavePropertiesData erstellt wurde.
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: IContextNode::LoadPropertiesData-Methode (IACom.h)
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
ms.openlocfilehash: 8d58c37dc91fac9704221fae13505f5e32c6e48d097133e3aad9154f5f2ec3e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719674"
---
# <a name="icontextnodeloadpropertiesdata-method"></a>IContextNode::LoadPropertiesData-Methode

Erstellt die anwendungsspezifischen und internen Eigenschaftsdaten für ein Bytearray neu, das zuvor mit [**IContextNode::SavePropertiesData erstellt wurde.**](icontextnode-savepropertiesdata.md)

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

*cbPropertiesDataSize* \[ In\]
</dt> <dd>

Die Größe des Eigenschaftendatenarrays.

</dd> <dt>

*pbPropertiesData* \[ In\]
</dt> <dd>

Das 8-Bit-Ganzzahlarray ohne Vorzeichen, das zu ladende Eigenschaftsinformationen enthält.

</dd> <dt>

*pfSuccessful* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn die Eigenschaftsdaten erfolgreich geladen wurden; andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




