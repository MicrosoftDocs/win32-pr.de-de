---
description: Gibt an, ob ein Strich als Teil einer Zeichnung oder als Teil des Schreibens analysiert werden soll.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: StrokeType-Enumeration (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 4b02a05582d675f04ad4458b1cb21c6d4a1797bacf15baf5d0851804d1a95d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589580"
---
# <a name="stroketype-enumeration"></a>StrokeType-Enumeration

Gibt an, ob ein Strich als Teil einer Zeichnung oder als Teil des Schreibens analysiert werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType \_ Unclassified**
</dt> <dd>

Der Strich kann entweder Teil einer Zeichnung oder Teil des Schreibens sein.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType \_ Writing**
</dt> <dd>

Der Strich ist Teil des Schreibens.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType \_ Drawing**
</dt> <dd>

Der Strich ist Teil einer Zeichnung.

</dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt einen Teil eines Strichereignishandlers, der ähnlich wie das [C++-Ereignissenkenbeispiel implementiert ist.](c---event-sinks-sample.md) Der hinzugefügte Strich wird überprüft, um zu überprüfen, ob der obere Rand des Begrenzungsfelds unterhalb eines Rands gezeichnet `drawingMargin` wurde. Wenn ja, wird das [**IInkAnalyzer-Objekt**](iinkanalyzer.md) so festgelegt, dass der Strich nicht als Handschriftstrich, sondern als `m_spInkAnalyzer` Zeichnungsstrich analysiert wird. `CheckHResult`ist eine Funktion, die eine und eine Zeichenfolge verwendet und eine Ausnahme auslöst, die mit der Zeichenfolge erstellt wird, wenn nicht `HRESULT` `HRESULT` SUCCESS **ist.**


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalyzer::SetStrokeType-Methode**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




