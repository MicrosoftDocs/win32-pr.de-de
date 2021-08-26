---
description: Ruft die IContextNode-Objekte ab, die dieser Alternativen zugeordnet sind.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: IAnalysisAlternate::GetAlternateNodes-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fbaff3cea515c9636127ce2267b9f05e0c0a0006b96046a7f2474661b3b76f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935520"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>IAnalysisAlternate::GetAlternateNodes-Methode

Ruft die [**IContextNode-Objekte**](icontextnode.md) ab, die dieser Alternativen zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppAlternateNodes* \[ out\]
</dt> <dd>

Ein Zeiger auf die [**IContextNodes-Auflistung,**](icontextnodes.md) die [**IContextNode-Objekte**](icontextnode.md) enthält, die dieser Alternativen zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppAlternateNodes* auf, wenn Sie die Kontextknotenauflistung nicht mehr verwenden müssen.

 

Diese Methode gibt die Blattkontextknoten zurück, die dieser Alternativen zugeordnet sind. Beispiele für Blattknoten sind InkWord-, TextWord-, Image-, InkDrawing- und InkBullet-Kontextknoten. Weitere Informationen finden Sie unter [**IContextNode::GetType**](icontextnode-gettype.md) und [Kontextknotentypen.](context-node-types.md)

Da sie Alternativen entsprechen, sind diese [**IContextNode-Objekte**](icontextnode.md) keine Nachfolger des IInkAnalyzer-Stamm-IContextNode des [**Objekts**](iinkanalyzer.md) (siehe [**IInkAnalyzer::GetRootNode-Methode),**](iinkanalyzer-getrootnode.md)es sei denn, sie sind die oberste Alternative, die das erste Element in einer [**IAnalysisAlternates-Auflistung**](ianalysisalternates.md) ist. 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> <dt>

[System. Windows. Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

