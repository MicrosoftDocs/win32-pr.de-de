---
description: Ordnet ein angegebenes untergeordnetes icontextnode-Objekt an den angegebenen Index zurück.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'Icontextnode:: muvesubnodetoposition-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343315"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>Icontextnode:: muvesubnodetoposition-Methode

Ordnet ein angegebenes untergeordnetes [**icontextnode**](icontextnode.md) -Objekt an den angegebenen Index zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psubnoabtomove* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, das verschoben werden soll.

</dd> <dt>

*ulnetwindex* \[ in\]
</dt> <dd>

Der Index für die neue Position des unter Knotens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Gibt " **E \_ invalidArg** " zurück, wenn " *psubnoenttomove* " kein untergeordneter Knoten dieses [**icontextnode**](icontextnode.md)ist.

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

[**Icontextnode:: "kreatesubnode"**](icontextnode-createsubnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




