---
description: Ändert den Wert, der angibt, ob dieser IContextNode teilweise oder vollständig aufgefüllt ist.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: IContextNode::SetPartiallyPopulated-Methode (IACom.h)
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
ms.openlocfilehash: 6df87085a82117a694b48d08c3e6e1f8500c8959060052f553a53f1a285d9707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713465"
---
# <a name="icontextnodesetpartiallypopulated-method"></a>IContextNode::SetPartiallyPopulated-Methode

Ändert den Wert, der angibt, ob [**dieser IContextNode**](icontextnode.md) teilweise oder vollständig aufgefüllt ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fPartiallyPopulated* \[ In\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn [**dieser IContextNode**](icontextnode.md) teilweise aufgefüllt ist; andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, wenn Ihre Anwendung eine eigene Datenstruktur verwaltet, die mit der von [**IInkAnalyzer synchronisiert wird.**](iinkanalyzer.md) Weitere Informationen finden Sie unter [Datenproxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

Stellen Sie beim Virtualisieren der Dokumentstruktur sicher, dass Sie den PropertyGuidsForContextNodes.RotatedBoundingBox-Wert (mit ContextNode.AddPropertyValue) für alle ContextNode-Objekte festlegen. Die RotatedBoundingBox-Eigenschaft wird vom InkAnalyzer berechnet und sollte standardmäßig für alle schreibenden ContextNodes verwendet werden. Wenn Ihre Anwendung die Analyseergebnisse jedoch virtualisiert, indem die PartiallyPopulated-Eigenschaft gesetzt wird, stellen Sie beim Behandeln des PopulateContextNode-Ereignisses sicher, dass Sie die RotatedBoundingBox-Eigenschaft auffüllen. Wenn die RotatedBoundingBox-Eigenschaft nicht festgelegt wird, werden möglicherweise mehr Dokumentdaten im aktuellen Analysevorgang verwendet.

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

[**\_IAnalysisProxyEvents::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




