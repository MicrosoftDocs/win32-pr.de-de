---
description: Verschiebt dieses icontextnode-Objekt aus der Auflistung der untergeordneten Knoten des übergeordneten Kontext Knotens in die Auflistung der untergeordneten Knoten des angegebenen Kontext Knotens.
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'Icontextnode:: Analyse-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041766"
---
# <a name="icontextnodereparent-method"></a>Icontextnode:: Analyse-Methode

Verschiebt dieses [**icontextnode**](icontextnode.md) -Objekt aus der Auflistung der untergeordneten Knoten des übergeordneten Kontext Knotens in die Auflistung der untergeordneten Knoten des angegebenen Kontext Knotens.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnewparent* \[ in\]
</dt> <dd>

Der neue übergeordnete Knoten für dieses [**icontextnode**](icontextnode.md) -Objekt.

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

[**Icontextnode:: getparameentnode**](icontextnode-getparentnode.md)
</dt> <dt>

[**Icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




