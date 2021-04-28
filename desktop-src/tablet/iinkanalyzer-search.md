---
description: 'IInkAnalyzer::Search-Methode: Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Unterstützung der Groß-/Kleinschreibung zur Lage.'
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
ms.openlocfilehash: 94ccdebf8c8a134a845ff3df3017d710d1da93f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113728"
---
# <a name="iinkanalyzersearch-method"></a>IInkAnalyzer::Search-Methode

Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Unterstützung der Groß-/Kleinschreibung zur Lage.

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

Die Anzahl der Strich-IDs in *ppulStrokeIds*.

</dd> <dt>

*ppulStrokeIds* \[ out\]
</dt> <dd>

Zeiger auf ein Array von Strich-IDs, die einen Satz von Strichen darstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Bei dieser Suche werden Teilzeichenfolgen mit mehreren Wörtern und einzelnen Wörtern gefunden. Sowohl alternative Erkennungsergebnisse als auch alternative Segmentierungen werden durchsucht.

Alle eingehenden Zeichenfolgen werden für den Vergleich mithilfe der LCID des aktuellen Threads in eine einzelne Zeichenfolge konvertiert, um diese Konvertierung zur Einhaltung von Kulturfallkonventionen zu ermöglichen.

Die übergebene Zeichenfolge wird als Ausdruck behandelt. Wörter und Zeichen müssen in den Alterantes für die Striche in der angegebenen Reihenfolge angezeigt werden. Die ersten und letzten Wörter des Ausdrucks können als Teilzeichenfolgen abgeglichen werden (das erste Wort, das am Ende eines alternativen und das letzte Wort beim Umbetten eines worts angezeigt wird), aber alle anderen Wörter (innerhalb des Ausdrucks) müssen als ganze Wörter angezeigt werden.

Wenn die übergebene Zeichenfolge keine Leerzeichen zwischen Zeichen enthält, kann die Teilzeichenfolge an einer beliebigen Stelle innerhalb eines einzelnen Worts in einer alternativen Zeichenfolge gefunden werden.

Nur das Vorhandensein oder Fehlen von Leerzeichen zwischen Zeichen ändert die Ergebnisse der Suche. Leerzeichen, die nicht von Zeichen umgeben sind, werden ignoriert. Der Typ des Leerraums wird ignoriert (eine Registerkarte oder ein Leerzeichen zwischen Zeichen führt zum gleichen Ergebnis). Die Leerraummenge spielt keine Rolle. Ein leerzeichen oder zwei Leerzeichen zwischen Zeichen ergeben das gleiche Ergebnis.

Die Suche generiert keine PopulateContextNode-Ereignisse. Nur die Striche, die bereits aufgefüllt wurden, werden durchsucht.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




