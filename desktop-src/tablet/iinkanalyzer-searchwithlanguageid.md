---
description: 'IInkAnalyzer::SearchWithLanguageId-Methode: Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Kenntnis.'
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: IInkAnalyzer::SearchWithLanguageId-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 201469933da10b0d68a4d3a50e63c42f8d01d2dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083658"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a>IInkAnalyzer::SearchWithLanguageId-Methode

Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Unterstützung der Groß-/Kleinschreibung zur Lage.

## <a name="syntax"></a>Syntax


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
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

*lSearchStringLanguageId* \[ In\]
</dt> <dd>

Die LCID, die der übergebenen Zeichenfolge zugeordnet ist. Wird verwendet, um die Groß-/Kleinschreibung intern zu konvertieren, um Vergleiche ohne Unterscheidung nach Groß-/Kleinschreibung zu unterstützen.

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

Die übergebene Zeichenfolge wird als Ausdruck behandelt. Wörter und Zeichen müssen in den Alterantes für die Striche in der angegebenen Reihenfolge angezeigt werden. Das erste und das letzte Wort des Ausdrucks können als Teilzeichenfolgen übereinstimmen (das erste Wort, das am Ende eines alternativen Worts und das letzte Wort, das beim Umhügen eines Worts angezeigt wird), aber alle anderen Wörter (die innerhalb des Ausdrucks) müssen als ganze Wörter angezeigt werden.

Wenn die übergebene Zeichenfolge keine Leerzeichen zwischen Zeichen enthält, kann die Teilzeichenfolge an einer beliebigen Stelle innerhalb eines einzelnen Worts in einem alternativen Gefunden werden.

Nur das Vorhandensein oder Fehlen von Leerzeichen zwischen Zeichen ändert die Ergebnisse der Suche. Leerzeichen, die nicht von Zeichen umgeben sind, werden ignoriert. Der Typ des Leerraums wird ignoriert (eine Registerkarte oder ein Leerzeichen zwischen Zeichen führt zu demselben Ergebnis). Die Menge an Leerzeichen spielt keine Rolle. Ein oder zwei Leerzeichen zwischen Zeichen führen zu demselben Ergebnis.

Die Suche generiert keine PopulateContextNode-Ereignisse. Nur die Striche, die bereits aufgefüllt wurden, werden durchsucht.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




