---
description: Ändert den Typ des angegebenen Strichs.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: IInkAnalyzer::SetStrokeType-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6d65c01ba3618bad563ee2b8c8a9c4fee3479a12c796b2f2f570832fac1d826c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709030"
---
# <a name="iinkanalyzersetstroketype-method"></a>IInkAnalyzer::SetStrokeType-Methode

Ändert den Typ des angegebenen Strichs.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lStrokeId* \[ In\]
</dt> <dd>

Der Strichbezeichner des Strichs, dem *StrokeType* zugewiesen werden soll.

</dd> <dt>

*StrokeType* \[ In\]
</dt> <dd>

Der [**StrokeType-Wert,**](stroketype.md) der dem Strich zugewiesen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Wenn der Typ des Strichs der [**StrokeType-Wert StrokeType**](stroketype.md) **\_ Unclassified** ist, klassifiziert [**IInkAnalyzer**](iinkanalyzer.md) den Strich während der Freihandanalyse. Andernfalls verwendet **IInkAnalyzer** den für den Strich festgelegten Typ.

[**IInkAnalyzer**](iinkanalyzer.md) legt den Strichtypwert nicht als Teil der Freihandanalyse fest. Verwenden Sie zum Angeben oder Ändern des Strichtyps die **IInkAnalyzer::SetStrokeType-Methode** oder [**die IInkAnalyzer::SetStrokesType-Methode.**](iinkanalyzer-setstrokestype.md)

Wenn ein Strich einem [**IContextNode**](icontextnode.md) zugeordnet ist, der kein nicht klassifizierter Freihandknoten ist (siehe [**IContextNode::GetType),**](icontextnode-gettype.md)verschiebt diese Methode den Strich in einen nicht klassifizierten Freihandknoten, der Striche derselben Sprache enthält. Wenn kein solcher Kontextknoten vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten Ink-Knoten und fügt ihm den Strich hinzu. Ein nicht klassifizierter Freihandknoten ist ein **IContextNode** vom Typ UnclassifiedInk.

Wenn diese Methode einen Strich aus einem [**IContextNode**](icontextnode.md) verschiebt, der kein nicht klassifizierter Freihandknoten ist, fügt diese Methode auch das umgebende Feld des Strichs dem geänderten Bereich des Freihandanalysetools hinzu (siehe [**IInkAnalyzer::GetDirtyRegion-Methode).**](iinkanalyzer-getdirtyregion.md)

Diese Methode bewegt keinen Strich, wenn der *StrokeType-Parameter* mit dem aktuellen Typ des Strichs übereinstimmt.

Wenn Sie den Strichtyp für Striche festlegen, die einem ContextNode zugeordnet sind, für den NodeTypeAndProperties bestätigt wurde, wird eine InvalidOperationException ausgelöst.

Wenn der angegebene Strich nicht dem [**IInkAnalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne den **IInkAnalyzer** zu aktualisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::GetStrokeType-Methode**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokesType-Methode**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




