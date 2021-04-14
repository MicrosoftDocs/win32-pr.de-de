---
description: Bestimmt, ob das icontextnode-Objektdaten enthält, die unter dem angegebenen Bezeichner gespeichert sind.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'Icontextnode:: ContainsPropertyData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485115"
---
# <a name="icontextnodecontainspropertydata-method"></a>Icontextnode:: ContainsPropertyData-Methode

Bestimmt, ob das [**icontextnode**](icontextnode.md) -Objektdaten enthält, die unter dem angegebenen Bezeichner gespeichert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppropertydataid* \[ in\]
</dt> <dd>

Der Bezeichner für die Daten.

</dd> <dt>

*pbenthält* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn das [**icontextnode**](icontextnode.md) -Objektdaten enthält, die unter dem angegebenen Bezeichner gespeichert sind. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den anwendungsspezifischen Daten können Sie mit dieser Methode auch bestimmen, ob dieser [**icontextnode**](icontextnode.md) andere interne Daten enthält (siehe Eigenschaften des [Analysis-Hinweises](analysis-hint-properties.md) und [Kontext Knoten Eigenschaften](context-node-properties.md)).

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

[**Icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Icontextnode:: loadpropertiesdata**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**Icontextnode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Icontextnode:: savepropertiesdata**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




