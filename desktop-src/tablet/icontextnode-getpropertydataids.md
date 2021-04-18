---
description: Ruft die Bezeichner ab, für die Eigenschafts Daten vorhanden sind.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'Icontextnode:: GetPropertyDataIds-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cdbc0ec0a613feccb4064a88f4723538439f4532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343694"
---
# <a name="icontextnodegetpropertydataids-method"></a>Icontextnode:: GetPropertyDataIds-Methode

Ruft die Bezeichner ab, für die Eigenschafts Daten vorhanden sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulguidcount* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Eigenschaften.

</dd> <dt>

*ppguids* \[ vorgenommen\]
</dt> <dd>

Die Bezeichner, für die Eigenschafts Daten vorhanden sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppguids* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Diese Methode gibt die anwendungsspezifischen Bezeichner für Eigenschaften Daten zurück, die hinzugefügt wurden. Außerdem werden die Bezeichner für die internen Eigenschaften Daten zurückgegeben, die von den Eigenschaften Konstanten für [Kontext Knoten](context-node-properties.md) beschrieben werden.

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

[**Icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Icontextnode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**Icontextnode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

