---
description: Verschiebt Strichdaten aus diesem IContextNode in den angegebenen IContextNode.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: IContextNode::ReparentStrokeByIdToNode-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a915425900bccb15145546658d51d50dcaee14880f8f219bd1908efaa17bd3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008410"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>IContextNode::ReparentStrokeByIdToNode-Methode

Verschiebt Strichdaten aus diesem [**IContextNode**](icontextnode.md) in den angegebenen **IContextNode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lStrokeId* \[ In\]
</dt> <dd>

Der Bezeichner des zu verschiebenden Strichs.

</dd> <dt>

*pContextNodeDestination* \[ In\]
</dt> <dd>

Das [**IContextNode-Objekt,**](icontextnode.md) in das die Strichdaten verschoben werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Das angegebene [**IContextNode-Objekt**](icontextnode.md) muss einer der folgenden Typen aus den [Konstanten für Kontextknotentypen](context-node-types.md) sein: **InkWord,** **InkDrawing,** **InkBullet** oder **UnclassifiedInk**. Der Versuch, einen Strich in einen anderen **IContextNode-Objekttyp** zu verschieben, führt zu einem Rückgabewert von **E \_ INVALIDARG.**

Diese Methode kann von jedem [**IContextNode-Objekt**](icontextnode.md) aufgerufen werden, einschließlich **IContextNode-Objekten** ohne Ink-Blatt. Auf den angegebenen Strich muss von einem der Nachfolger dieses **IContextNode-Objekts** verwiesen werden, oder **E \_ INVALIDARG** wird zurückgegeben.

Wenn entweder dieser [**IContextNode**](icontextnode.md) oder der **IContextNode** in *pContextNodeDestination* bestätigt wird, wird **E \_ INVALIDARG** zurückgegeben (siehe [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).

Das Freihandanalyseprogramm löscht keine leeren Kontextknoten aus der Ergebnisstruktur als Reaktion auf diese Methode.

-   Ein Freihandblattknoten, der auf keine Strichdaten verweist, ist ein leerer Knoten.
-   Ein Containerknoten, der auf keine untergeordneten Knoten verweist, ist ein leerer Knoten.

Ein leerer Knoten generiert Fehler, wenn er sich während eines Freihandanalysevorgangs in der Struktur befindet. Um einen Knoten aus der Struktur des Freihandanalysetools zu entfernen, rufen Sie die [**IContextNode::D eleteSubNode-Methode**](icontextnode-deletesubnode.md) des übergeordneten Knotens auf (siehe [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)).

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

[**IContextNode::SetStrokes**](icontextnode-setstrokes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




