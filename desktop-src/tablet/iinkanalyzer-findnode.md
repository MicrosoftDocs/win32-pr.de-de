---
description: Ruft das IContextNode-Objekt für einen angegebenen guiD (Globally Unique Identifier) ab.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: IInkAnalyzer::FindNode-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3d7e6cd4b24b2cb0977284d62b2bad9e26a8d8944ebc653e22d97d0455d883f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967269"
---
# <a name="iinkanalyzerfindnode-method"></a>IInkAnalyzer::FindNode-Methode

Ruft das [**IContextNode-Objekt**](icontextnode.md) für einen angegebenen guiD (Globally Unique Identifier) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pId* \[ In\]
</dt> <dd>

Der Bezeichner für das [**IContextNode-Objekt.**](icontextnode.md)

</dd> <dt>

*ppContextNodeFound* \[ out\]
</dt> <dd>

Ein Zeiger auf das [**IContextNode-Objekt**](icontextnode.md) mit dem *pId-Bezeichner.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppContextNodeFound* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Wenn kein solches [**IContextNode-Objekt**](icontextnode.md) als Nachfolger des [**IInkAnalyzer-Stammknotens**](iinkanalyzer.md) vorhanden ist, wird **NULL** zurückgegeben.

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

[**IInkAnalyzer::FindInkLeafNodes-Methode**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**IInkAnalyzer::FindInkLeafNodesForStrokes-Methode**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindLeafNodes-Methode**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeForStrokes-Methode**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeInSubTree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBack-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBackInSubTree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

