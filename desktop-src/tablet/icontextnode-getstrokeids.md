---
description: Ruft ein Array von Bezeichnern für die Striche im IContextNode-Objekt ab.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: IContextNode::GetStrokeIds-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ebe66d514b20fc558adce39c013cf559fbc63bb38f772bff73b0819c10426960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967370"
---
# <a name="icontextnodegetstrokeids-method"></a>IContextNode::GetStrokeIds-Methode

Ruft ein Array von Bezeichnern für die Striche im [**IContextNode-Objekt**](icontextnode.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Die Anzahl der Striche. Der übergebene Wert wird nicht verwendet.

</dd> <dt>

*pplStrokes* \[ out\]
</dt> <dd>

Ein Zeiger auf das Array von Strichbezeichnern für dieses [**IContextNode-Objekt.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, verwenden Sie [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher von \* *pplStrokes* frei zu geben, wenn Sie die Informationen nicht mehr benötigen.

 

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

[**IContextNode::GetStrokeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**IContextNode::GetStrokeCount**](icontextnode-getstrokecount.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

