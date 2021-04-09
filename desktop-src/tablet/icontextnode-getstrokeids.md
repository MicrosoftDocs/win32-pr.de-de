---
description: Ruft ein Array von bezeichern für die Striche innerhalb des icontextnode-Objekts ab.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'Icontextnode:: GetStrokeIds-Methode (iacom. h)'
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
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129500"
---
# <a name="icontextnodegetstrokeids-method"></a>Icontextnode:: GetStrokeIds-Methode

Ruft ein Array von bezeichern für die Striche innerhalb des [**icontextnode**](icontextnode.md) -Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulstrokeidscount* \[ in, out\]
</dt> <dd>

Die Anzahl der Striche. Der Wert, der an die Übergabe erfolgt, wird nicht verwendet.

</dd> <dt>

*pplstrokes* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das Array von Strich Bezeichners für dieses [**icontextnode**](icontextnode.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher aus \* *pplstrokes* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

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

[**Icontextnode:: getstrokeid**](icontextnode-getstrokeid.md)
</dt> <dt>

[**Icontextnode:: getstrokecount**](icontextnode-getstrokecount.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

