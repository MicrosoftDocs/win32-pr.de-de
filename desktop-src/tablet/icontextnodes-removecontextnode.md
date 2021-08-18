---
description: Entfernt ein IContextNode-Objekt aus dieser Auflistung.
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: IContextNodes::RemoveContextNode-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8fa1fd222e671dfd87f15862108ea66df3b99e530d453cf4614b7572d31b275c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092301"
---
# <a name="icontextnodesremovecontextnode-method"></a>IContextNodes::RemoveContextNode-Methode

Entfernt ein [**IContextNode-Objekt**](icontextnode.md) aus dieser Auflistung.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContextNode* \[ In\]
</dt> <dd>

Das zu entfernende [**IContextNode-Objekt.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




