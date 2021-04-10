---
description: Ruft alle Analysis Hint-icontextnode-Objekte ab, die an iinkanalyzer angefügt sind und den angegebenen Namen aufweisen.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'Iinkanalyzer:: getanalysishintsbyname-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214662"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a>Iinkanalyzer:: getanalysishintsbyname-Methode

Ruft alle Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte ab, die an [**iinkanalyzer**](iinkanalyzer.md) angefügt sind und den angegebenen Namen aufweisen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hintname* \[ in\]
</dt> <dd>

Der Hinweis Name, nach dem gesucht werden soll.

</dd> <dt>

*ppanalysishints* \[ vorgenommen\]
</dt> <dd>

Der Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte in [**iinkanalyzer**](iinkanalyzer.md) mit dem angegebenen Namen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md) die Rückgabewerte.

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppanalysishints* aufrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Diese Methode gibt eine leere Auflistung zurück, wenn keine derartigen Analyse Hinweis Knoten an [**iinkanalyzer**](iinkanalyzer.md)angefügt sind.

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

[**Iinkanalyzer:: GetAnalysisHints-Methode**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

