---
description: Ändert den bestäalisierungstyp, der steuert, was das iinkanalyzer-Objekt über den icontextnode ändern kann.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'Icontextnode:: Confirm-Methode (iacom. h)'
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
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345080"
---
# <a name="icontextnodeconfirm-method"></a>Icontextnode:: Confirm-Methode

Ändert den bestäalisierungstyp, der steuert, was das [**iinkanalyzer**](iinkanalyzer.md) -Objekt über den [**icontextnode**](icontextnode.md)ändern kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*confirmedtype* \[ in\]
</dt> <dd>

Der [**ConfirmationType**](confirmationtype.md) , der auf den Knoten angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um dem Endbenutzer zu ermöglichen, zu bestätigen, dass die Striche von [**iinkanalyzer**](iinkanalyzer.md) ordnungsgemäß analysiert wurden. Nachdem **icontextnode:: Confirm** aufgerufen wurde, werden die [**icontextnode**](icontextnode.md) -Objekte für diese Striche von **iinkanalyzer** während der späteren Analyse nicht geändert.

Verwenden Sie **icontextnode:: Confirm** , wenn der Benutzer die Analyseergebnisse bestätigt hat und nicht möchten, dass [**iinkanalyzer**](iinkanalyzer.md) einen [**icontextnode**](icontextnode.md) während der späteren Analyse ändert. Wenn der Benutzer z. b. das Wort "in" schreibt und die Anwendung die [**iinkanalyzer::**](iinkanalyzer-analyze.md)Analytics-Methode aufruft, generiert die Ink Analyzer einen inkWord-Knoten mit dem Wert "to". Wenn der Benutzer dann "Me" nach "to" als ein Wort hinzufügt und die Anwendung die **iinkanalyzer:: Analysis-Methode** erneut aufruft, kann der Ink Analyzer den vorherigen "InkWord"-Knoten entfernen und einen neuen inkWord-Knoten mit dem Wert "Tome" erstellen. Wenn jedoch nach dem ersten **iinkanalyzer**-Ansichts Befehl: Analysemethode: die Anwendung ruft **icontextnode:: Confirm** für den inkWord-Knoten für "to" mit dem [**ConfirmationType**](confirmationtype.md) -Wert **NodeTypeAndProperties** auf, bevor der Benutzer "Me" hinzufügt. wenn die Anwendung die **iinkanalyzer::** Analytics-Methode aufruft, wird der "to"-Knoten von der Ink Analyzer nicht entfernt oder geändert. Stattdessen erkennt der Ink Analyzer möglicherweise zwei inkWord-Knoten für "to" und "Me".

[**Icontextnode**](icontextnode.md) kann nur Objekte des Typs InkWord und InkDrawing bestätigen (siehe [Kontext Knoten Typen](context-node-types.md)). **Icontextnode:: Confirm** gibt **E \_ invalidArg** zurück, wenn der Knoten kein Blattknoten ist.

Die [**iinkanalyzer:: RemoveStroke-Methode**](iinkanalyzer-removestroke.md) und die [**iinkanalyzer:: RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md) löschen jeden Knoten, von dem Sie die Strich Daten entfernen.

[**Icontextnode:: setstrokes**](icontextnode-setstrokes.md), [**iinkanalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md)und [**iinkanalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) geben **Core \_ E \_ InvalidOperation** zurück, wenn das [**icontextnode**](icontextnode.md) -Objekt bereits bestätigt ist.

[**Icontextnode::**](icontextnode-reparentstrokebyidtonode.md) Analyse Name gibt einen Fehler zurück, wenn der Quell-oder Zielknoten bestätigt ist.

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

[**Icontextnode:: isconfirmed**](icontextnode-isconfirmed.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




