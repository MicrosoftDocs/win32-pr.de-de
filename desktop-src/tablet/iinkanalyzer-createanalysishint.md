---
description: Fügt dem iinkanalyzer einen neuen Analyse Hinweis Knoten mit einem unendlichen Bereich hinzu.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'Iinkanalyzer:: feateanalysishint-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343708"
---
# <a name="iinkanalyzercreateanalysishint-method"></a>Iinkanalyzer:: feateanalysishint-Methode

Fügt dem [**iinkanalyzer**](iinkanalyzer.md)einen neuen Analyse Hinweis Knoten mit einem unendlichen Bereich hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppanalysishint* \[ vorgenommen\]
</dt> <dd>

Der neue Analyse Hinweis Knoten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md) .

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppanalysishint* aufrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Um zusätzliche Kontextinformationen für [**iinkanalyzer**](iinkanalyzer.md)bereitzustellen, können Sie der Ink Analyzer Analyse Hinweise hinzufügen. Analyse Hinweise können die Erkennungsgenauigkeit verbessern. Beispielsweise können Sie die Informationen zu "Faktoid" und "Guide" für Felder in einer Formular Anwendung hinzufügen.

Diese Methode erstellt einen neuen [**icontextnode**](icontextnode.md) mit dem Kontext Knotentyp AnalysisHint (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)) und fügt den neuen Hinweis als untergeordneten Knoten des Stamm Knotens des [**iinkanalyzer**](iinkanalyzer.md) -Objekts hinzu (siehe [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) und [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)).

Wenn Sie dem Hinweis Kontextinformationen hinzufügen möchten, verwenden Sie [**icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md) mit dem Parameter *ppropertydataid* , der auf eine der Eigenschaften Konstanten von [Analysis Hint](analysis-hint-properties.md) festgelegt ist.

Wenn ein Hinweis einem unendlichen Bereich zugewiesen wird, der als globaler Hinweis bezeichnet wird, wendet [**iinkanalyzer**](iinkanalyzer.md) den Kontext des Hinweises auf alle frei Hand Eingaben an, die sich nicht im Bereich eines anderen Hinweises befinden. An einen einzelnen **iinkanalyzer** können mehrere Hinweise angefügt werden. Es kann jedoch nur ein globaler Hinweis an einen einzelnen Ink Analyzer angefügt werden, und es können keine nicht globalen Hinweise überlappen. Weitere Informationen zu den Typen von Kontextinformationen, die von einem Hinweis bereitgestellt werden können, finden Sie unter [Analysis Hint Properties](analysis-hint-properties.md).

Durch das Hinzufügen eines Analyse Hinweises wird der Bereich des Hinweises für die erneute Analyse nicht markiert. Um den Bereich innerhalb des Hinweises für die erneute Analyse zu markieren, verwenden Sie die [**iinkanalyzer:: setdirtyregion-Methode**](iinkanalyzer-setdirtyregion.md) , um den geänderten Bereich auf die Vereinigung des aktuellen geänderten Bereichs und Bereichs des Analyse Hinweises festzulegen.

Wenn Sie Hinweise für eine Formular Anwendung verwenden, sollte die Anwendung die Mischung aus Text Kontext und Freihand in Formularen vermeiden. Dies bedeutet beispielsweise, dass Text Feldnamen nicht in der Analyse Struktur erstellt werden sollten. Hinweise dienen dazu, die frei Hand Eingaben den Bereichen auf Seiten zuzuordnen. Jeder Text Kontext beeinträchtigt diese Ink-to-Hint-Zuordnung. Der Analyse Vorgang kann die frei Hand Eingabe und den Text Kontext in demselben Schreibbereich zusammenführen, wodurch verhindert wird, dass die frei Hand Eingaben dem Hinweis Bereich zugeordnet werden.

Weitere Informationen zur frei Hand Analyse finden Sie unter Übersicht über die Handschrift [Analyse](ink-analysis-overview.md).

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

[**Icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**Iinkanalyzer::D eleteanalysishint-Methode**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**Iinkanalyzer:: GetAnalysisHints-Methode**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**Iinkanalyzer:: getanalysishintsbyname-Methode**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Eigenschaften des Analyse Hinweises](analysis-hint-properties.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

