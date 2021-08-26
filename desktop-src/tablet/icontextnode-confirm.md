---
description: Ändert den Bestätigungstyp, der steuert, was das IInkAnalyzer-Objekt über den IContextNode ändern kann.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: IContextNode::Confirm-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 248eb78f364f7e938d78846c3e830cc170587961b81dfedcc046e10c59e4fd18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008450"
---
# <a name="icontextnodeconfirm-method"></a>IContextNode::Confirm-Methode

Ändert den Bestätigungstyp, der steuert, was das [**IInkAnalyzer-Objekt**](iinkanalyzer.md) über den [**IContextNode**](icontextnode.md)ändern kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*confirmedType* \[ In\]
</dt> <dd>

Der [**ConfirmationType,**](confirmationtype.md) der auf den Knoten angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, damit der Endbenutzer bestätigen kann, dass [**IInkAnalyzer**](iinkanalyzer.md) die Striche ordnungsgemäß analysiert hat. Nachdem **IContextNode::Confirm** aufgerufen wurde, ändert **IInkAnalyzer** die [**IContextNode-Objekte**](icontextnode.md) für diese Striche während der späteren Analyse nicht.

Verwenden Sie **IContextNode::Confirm,** wenn der Benutzer die Analyseergebnisse bestätigt hat und [**IInkAnalyzer**](iinkanalyzer.md) während der späteren Analyse keinen [**IContextNode**](icontextnode.md) ändern soll. Wenn der Benutzer beispielsweise das Wort "to" schreibt und dann die Anwendung [**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)aufruft, generiert das Freihandanalyseprogramm einen InkWord-Knoten mit dem Wert "to". Wenn der Benutzer dann "me" nach "to" als ein Wort hinzufügt und die Anwendung die **IInkAnalyzer::Analyze-Methode** erneut aufruft, entfernt die Freihandanalyse möglicherweise den vorherigen InkWord-Knoten und erstellt einen neuen InkWord-Knoten mit dem Wert "tome". Wenn die Anwendung jedoch nach dem ersten Aufruf der **IInkAnalyzer::Analyze-Methode** **IContextNode::Confirm** auf dem InkWord-Knoten für "to" mit dem [**ConfirmationType-Wert**](confirmationtype.md) **NodeTypeAndProperties** aufruft, bevor der Benutzer das "me" hinzufügt, entfernt oder ändert das Ink-Analyzer den Knoten "to", wenn die Anwendung **die IInkAnalyzer::Analyze-Methode** aufruft. Stattdessen erkennt das Ink-Analyseprogramm möglicherweise zwei InkWord-Knoten für "to" und "me".

[**IContextNode**](icontextnode.md) kann nur Objekte vom Typ InkWord und InkDrawing bestätigen (siehe [Kontextknotentypen](context-node-types.md)). **IContextNode::Confirm** gibt **E \_ INVALIDARG** zurück, wenn der Knoten kein Blattknoten ist.

[**IInkAnalyzer::RemoveStroke-Methode**](iinkanalyzer-removestroke.md) und [**IInkAnalyzer::RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md) bestätigen jeden Knoten, aus dem Strichdaten entfernt werden.

[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md)und [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) geben **CORE E \_ \_ INVALIDOPERATION** zurück, wenn das [**IContextNode-Objekt**](icontextnode.md) bereits bestätigt wurde.

[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) gibt einen Fehler zurück, wenn der Quell- oder Zielknoten bestätigt wird.

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

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




