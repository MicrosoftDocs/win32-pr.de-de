---
description: 'IInkAnalyzer::Search-Methode: Bietet eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen, die erkannte Typen haben.'
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: IInkAnalyzer::Search-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a5ebbec010d84f510d9bd2786b20fee1deaa34039720d842df77cbe0f1ca9825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091498"
---
# <a name="iinkanalyzersearch-method"></a>IInkAnalyzer::Search-Methode

Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Unterstützung der Groß-/Kleinschreibung zur Unterstützung von Strichen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrPhraseToMatch* \[ In\]
</dt> <dd>

Der Ausdruck, der in den Alternativen für die derzeit analysierten Striche gefunden wird.

</dd> <dt>

*pulSearchResultCount* \[ in, out\]
</dt> <dd>

Die maximale Anzahl von Ergebnissen, die von der Suche zurückgegeben werden.

</dd> <dt>

*ppulStrokeCountPerResult* \[ out\]
</dt> <dd>

Zeiger auf ein Array der Anzahl von Strichen in jedem Suchergebnis.

</dd> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Die Anzahl der Strich-IDs in *ppulStrokeIds.*

</dd> <dt>

*ppulStrokeIds* \[ out\]
</dt> <dd>

Zeiger auf ein Array von Strich-IDs, die einen Satz von Strichen darstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Bei dieser Suche werden Teilzeichenfolgen mit mehreren Wörtern und einzelnen Wörtern gefunden. Sowohl alternative Erkennungsergebnisse als auch alternative Segmentierungen werden durchsucht.

Alle eingehenden Zeichenfolgen werden für den Vergleich mithilfe der LCID des aktuellen Threads in eine einzelne Zeichenfolge konvertiert, um diese Konvertierung zur Einhaltung von Kulturfallkonventionen zu ermöglichen.

Die übergebene Zeichenfolge wird als Ausdruck behandelt. Wörter und Zeichen müssen in den Alterantes für die Striche in der angegebenen Reihenfolge angezeigt werden. Das erste und das letzte Wort des Ausdrucks können als Teilzeichenfolgen übereinstimmen (das erste Wort, das am Ende eines alternativen Worts und das letzte Wort, das beim Umhügen eines Worts angezeigt wird), aber alle anderen Wörter (die innerhalb des Ausdrucks) müssen als ganze Wörter angezeigt werden.

Wenn die übergebene Zeichenfolge keine Leerzeichen zwischen Zeichen enthält, kann die Teilzeichenfolge an einer beliebigen Stelle innerhalb eines einzelnen Worts in einem alternativen Gefunden werden.

Nur das Vorhandensein oder Fehlen von Leerzeichen zwischen Zeichen ändert die Ergebnisse der Suche. Leerzeichen, die nicht von Zeichen umgeben sind, werden ignoriert. Der Typ des Leerraums wird ignoriert (eine Registerkarte oder ein Leerzeichen zwischen Zeichen führt zu demselben Ergebnis). Die Menge an Leerzeichen spielt keine Rolle. Ein oder zwei Leerzeichen zwischen Zeichen führen zu demselben Ergebnis.

Die Suche generiert keine PopulateContextNode-Ereignisse. Nur die Striche, die bereits aufgefüllt wurden, werden durchsucht.

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
</dt> </dl>

 

 




