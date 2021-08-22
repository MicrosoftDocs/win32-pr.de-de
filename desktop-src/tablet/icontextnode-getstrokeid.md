---
description: Ruft den Strichbezeichner für den Strich ab, auf den ein Indexwert innerhalb des IContextNode-Objekts verweist.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: IContextNode::GetStrokeId-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f3eb5408ff9f6d2b98acebc3f6e936165ea46132fa1fdda252da8797b864c8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590720"
---
# <a name="icontextnodegetstrokeid-method"></a>IContextNode::GetStrokeId-Methode

Ruft den Strichbezeichner für den Strich ab, auf den ein Indexwert innerhalb des [**IContextNode-Objekts**](icontextnode.md) verweist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulIndex* \[ In\]
</dt> <dd>

Der Index des zurückzugebenden Strichs.

</dd> <dt>

*plStrokeId* \[ out\]
</dt> <dd>

Der Strichbezeichner für den Strich, auf den der *ulIndex-Parameter* innerhalb des aktuellen [**IContextNode-Objekts**](icontextnode.md) verweist.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[**IContextNode::GetStrokeCount**](icontextnode-getstrokecount.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




