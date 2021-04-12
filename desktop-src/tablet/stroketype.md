---
description: Gibt an, ob ein Strich im Rahmen einer Zeichnung oder beim Schreiben analysiert werden soll.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: StrokeType-Enumeration (iacom. h)
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
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217200"
---
# <a name="stroketype-enumeration"></a>StrokeType-Enumeration

Gibt an, ob ein Strich im Rahmen einer Zeichnung oder beim Schreiben analysiert werden soll.

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

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType \_ nicht klassifiziert**
</dt> <dd>

Der Strich kann entweder Teil einer Zeichnung oder eines Teils eines Schreibvorgangs sein.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Schreiben von StrokeType \_**
</dt> <dd>

Der Strich ist Teil des Schreibens.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType- \_ Zeichnung**
</dt> <dd>

Der Strich ist Teil einer Zeichnung.

</dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt einen Teil eines Stroke-Ereignis Handlers, der in ähnlicher Weise wie das [C++ Event Sinks-Beispiel](c---event-sinks-sample.md)implementiert wird. Der hinzugefügte Strich wird geprüft, um festzustellen, ob der obere Rand seines umgebenden Felds unterhalb eines Rands gezeichnet wurde `drawingMargin` . Wenn dies der Fall ist, wird das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, `m_spInkAnalyzer` , so festgelegt, dass der Strich als Zeichen Strich analysiert wird, anstatt als Handschrift Strich. `CheckHResult` eine Funktion, die eine `HRESULT` -und eine-Zeichenfolge annimmt und eine mit der-Zeichenfolge erstellte Ausnahme auslöst, wenn der `HRESULT` nicht **erfolgreich** ist.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer:: SetStrokeType-Methode**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




