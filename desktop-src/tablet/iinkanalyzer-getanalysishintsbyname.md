---
description: Ruft alle IContextNode-Analysehinweisobjekte ab, die an IInkAnalyzer angefügt sind und den angegebenen Namen aufweisen.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: IInkAnalyzer::GetAnalysisHintsByName-Methode (IACom.h)
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
ms.openlocfilehash: 24c69cd1dd321b5f142fe07b7463941fc0944a2206f1f8d6baf0ebbe8459b6ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719192"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a>IInkAnalyzer::GetAnalysisHintsByName-Methode

Ruft alle [**IContextNode-Analysehinweisobjekte**](icontextnode.md) ab, die an [**IInkAnalyzer**](iinkanalyzer.md) angefügt sind und den angegebenen Namen aufweisen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hintName* \[ In\]
</dt> <dd>

Der Name des Hinweises, nach dem gesucht werden soll.

</dd> <dt>

*ppAnalysisHints* \[ out\]
</dt> <dd>

Der Analysehinweis [**IContextNode-Objekte**](icontextnode.md) im [**IInkAnalyzer**](iinkanalyzer.md) mit dem angegebenen Namen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse](classes-and-interfaces---ink-analysis.md) der Rückgabewerte.

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppAnalysisHints* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Diese Methode gibt eine leere Auflistung zurück, wenn keine solchen Analysehinweisknoten an den [**IInkAnalyzer**](iinkanalyzer.md)angefügt sind.

Ein Analysehinweisknoten ist ein [**IContextNode**](icontextnode.md) mit dem Kontextknotentyp AnalysisHint (siehe [**IContextNode::GetType**](icontextnode-gettype.md) und [Kontextknotentypen).](context-node-types.md)

Um dem Hinweis Kontextinformationen hinzuzufügen, verwenden Sie [**IContextNode::AddPropertyData,**](icontextnode-addpropertydata.md) wobei der *Parameter pPropertyDataId* auf einen der GUIDs (Globally Unique Identifiers) in den Konstanten der [Analysis Hint-Eigenschaften](analysis-hint-properties.md) festgelegt ist.

Verwenden Sie [**IContextNode::GetPropertyDataIds,**](icontextnode-getpropertydataids.md)um zu ermitteln, welche Eigenschaftswerte auf einem Kontextknoten festgelegt sind. Um den Wert einer Eigenschaft zu suchen, verwenden [**Sie IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::CreateAnalysisHint-Methode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::D eleteAnalysisHint-Methode**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::GetAnalysisHints-Methode**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

