---
description: Ruft alle Analysis Hint-icontextnode-Objekte ab, die an iinkanalyzer angefügt sind.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'Iinkanalyzer:: GetAnalysisHints-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129456"
---
# <a name="iinkanalyzergetanalysishints-method"></a>Iinkanalyzer:: GetAnalysisHints-Methode

Ruft alle Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte ab, die an [**iinkanalyzer**](iinkanalyzer.md)angefügt sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppanalysishints* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf alle Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte in [**iinkanalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppanalysishints* aufrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Diese Methode gibt eine leere Auflistung zurück, wenn keine Analyse Hinweis Knoten an [**iinkanalyzer**](iinkanalyzer.md)angefügt sind.

Ein Analyse Hinweis Knoten ist ein [**icontextnode**](icontextnode.md) mit dem Kontext Knotentyp AnalysisHint (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) und [Kontext Knoten Typen](context-node-types.md)).

Wenn Sie dem Hinweis Kontextinformationen hinzufügen möchten, verwenden Sie [**icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md) mit dem Parameter *ppropertydataid* , der auf einen der global eindeutigen Bezeichner (GUIDs) in den Eigenschaften Konstanten von [Analysis Hint](analysis-hint-properties.md) festgelegt ist.

Um zu ermitteln, welche Eigenschaftswerte für einen Kontext Knoten festgelegt werden, verwenden Sie [**icontextnode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md). Um den Wert einer Eigenschaft zu suchen, verwenden Sie [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Iinkanalyzer:: feateanalysishint-Methode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Iinkanalyzer::D eleteanalysishint-Methode**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**Iinkanalyzer:: getanalysishintsbyname-Methode**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

