---
description: Ändert den Wert, der angibt, ob dieser icontextnode teilweise oder vollständig ausgefüllt ist.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'Icontextnode:: setpartiallygefüllte-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041764"
---
# <a name="icontextnodesetpartiallypopulated-method"></a>Icontextnode:: setpartiallygefüllte-Methode

Ändert den Wert, der angibt, ob dieser [**icontextnode**](icontextnode.md) teilweise oder vollständig ausgefüllt ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

nicht aufgefüllt  \[ in\]
</dt> <dd>

**Variant \_ TRUE** , wenn dieser [**icontextnode**](icontextnode.md) teilweise aufgefüllt ist. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Weitere Informationen finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

Wenn Sie die Dokumentstruktur virtualisieren, achten Sie darauf, den PropertyGuidsForContextNodes. rotatedboundingbox-Wert (mithilfe von ContextNode. addpropertyvalue) für alle ContextNode-Objekte festzulegen. Die rotatedboundingbox-Eigenschaft wird vom InkAnalyzer berechnet und sollte standardmäßig für alle geschriebenen ContextNodes lauten. Wenn Ihre Anwendung jedoch die Analyseergebnisse durch Festlegen der Eigenschaft partiallyaufgefüllt durch Festlegen der Eigenschaft PopulateContextNode verarbeitet, achten Sie darauf, die rotatedboundingbox-Eigenschaft aufzufüllen. Wenn die rotatedboundingbox-Eigenschaft nicht festgelegt wird, werden möglicherweise mehr Dokument Daten im aktuellen Analyse Vorgang verwendet.

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

[**\_Ianalysisproxyevents::P opulatecontextnode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[**Icontextnode:: kreatepartiallypopulatedsubnode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**Icontextnode:: getpartiallyaufgefüllt**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




