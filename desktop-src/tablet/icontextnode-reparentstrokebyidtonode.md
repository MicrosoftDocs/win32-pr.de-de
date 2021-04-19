---
description: Verschiebt die Strich Daten aus diesem icontextnode in den angegebenen icontextnode.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'Icontextnode:: Analyse-strokebyidtonode-Methode (iacom. h)'
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
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360053"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>Icontextnode:: Analyse-strokebyidtonode-Methode

Verschiebt die Strich Daten aus diesem [**icontextnode**](icontextnode.md) in den angegebenen **icontextnode**.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lstrokeid* \[ in\]
</dt> <dd>

Der Bezeichner des zu verschiebenden Strichs.

</dd> <dt>

*pcontextnode Destination* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, in das die Strich Daten verschoben werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Das angegebene [**icontextnode**](icontextnode.md) -Objekt muss einer der folgenden Typen aus den [Kontext Knoten Typen](context-node-types.md) Konstanten sein: **InkWord**, **InkDrawing**, **InkBullet** oder **unclassimeedink**. Der Versuch, einen Strich in einen anderen Typ von **icontextnode** -Objekten zu verschieben, führt zu einem Rückgabewert von **E \_ invalidArg**.

Diese Methode kann von einem beliebigen [**icontextnode**](icontextnode.md) -Objekt aus aufgerufen werden, einschließlich nicht frei Hand Blatts **icontextnode** -Objekten. Auf den angegebenen Strich muss von einem der nachfolgenden Elemente dieses **icontextnode** -Objekts verwiesen werden, oder **E \_ invalidArg** wird zurückgegeben.

Wenn entweder dieser [**icontextnode**](icontextnode.md) oder der **icontextnode** in *pcontextnodebug-Ziel* bestätigt wird, wird **E \_ invalidArg** zurückgegeben (siehe [**icontextnode:: isconfirmed**](icontextnode-isconfirmed.md)).

Leere Kontext Knoten werden von der frei Hand Analyse nicht als Antwort auf diese Methode aus der Ergebnis Struktur gelöscht.

-   Ein frei Hand Blattknoten, der nicht auf hubdaten verweist, ist ein leerer Knoten.
-   Ein Container Knoten, der nicht auf untergeordnete Knoten verweist, ist ein leerer Knoten.

Ein leerer Knoten generiert Fehler, wenn er während eines frei Hand Analyse Vorgangs in der Struktur ist. Um einen Knoten aus der Struktur der Ink Analyzer zu entfernen, müssen Sie die [**icontextnode::D eletesubnode**](icontextnode-deletesubnode.md) -Methode des übergeordneten Knotens aufrufen (siehe [**icontextnode:: getParser Node**](icontextnode-getparentnode.md)).

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

[**Icontextnode:: setstrokes**](icontextnode-setstrokes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




