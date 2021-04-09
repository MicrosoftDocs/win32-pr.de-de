---
description: Stellt eine Fuzzysuche, bei der die Groß-/Kleinschreibung beachtet wird, nach analysierten Schreibvorgängen und analysierten Zeichnungs Strichen mit erkannten Typen bereit.
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'Iinkanalyzer:: Search-Methode (iacom. h)'
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
ms.openlocfilehash: ea9755c0f2836b363b967a3d6bfdc5d64a1305b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129441"
---
# <a name="iinkanalyzersearch-method"></a>Iinkanalyzer:: Search-Methode

Stellt eine Fuzzysuche, bei der die Groß-/Kleinschreibung beachtet wird, nach analysierten Schreibvorgängen und analysierten Zeichnungs Strichen mit erkannten Typen bereit.

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

*bstrauphrattomatch* \[ in\]
</dt> <dd>

Der Ausdruck, der in den Alternativen für die aktuell analysierten Striche zu finden ist.

</dd> <dt>

*pulsearchresultcount* \[ in, out\]
</dt> <dd>

Die maximale Anzahl von Ergebnissen, die von der Suche zurückgegeben werden.

</dd> <dt>

*ppulstrokezähltperresult* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array mit der Anzahl der Striche in jedem Suchergebnis.

</dd> <dt>

*pulstrokeidscount* \[ in, out\]
</dt> <dd>

Die Anzahl der Strich-IDs in *ppulstrokeids*.

</dd> <dt>

*ppulstrokeids* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von Strich-IDs, das einen Satz von Strichen darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Bei dieser Suche werden Teil Zeichenfolgen mit mehreren Wörtern und einzelnen Wörtern gefunden. Sowohl alternative Erkennungsergebnisse als auch alternative Segmentationen werden durchsucht.

Alle eingehenden Zeichen folgen werden für Vergleiche in eine einzelne Schreibweise konvertiert, wobei die LCID des aktuellen Threads verwendet wird, um diese Konvertierung durchzuführen, um kulturelle Fälle zu berücksichtigen.

Die Übergabe Zeichenfolge wird als Ausdruck behandelt. Wörter und Zeichen müssen in alterantes für die Striche in der angegebenen Reihenfolge angezeigt werden. Das erste und das letzte Wort des Ausdrucks können als Teil Zeichenfolgen abgeglichen werden (das erste Wort, das am Ende einer alternativen angezeigt wird, und das letzte Wort, das bei der beginginging-Darstellung auftritt), aber alle anderen Wörter (die innerhalb des Ausdrucks) müssen als ganze Wörter angezeigt werden.

Wenn die übergebene Zeichenfolge keine Leerzeichen zwischen Zeichen enthält, kann die Teil Zeichenfolge an einer beliebigen Stelle innerhalb eines einzelnen Worts in einer alternativen gefunden werden.

Die Ergebnisse der Suche werden nur durch das vorhanden sein oder Fehlen von Leerzeichen zwischen Zeichen geändert. Leerzeichen, die nicht von Zeichen umgeben sind, werden ignoriert. Der Typ des Leerraums wird ignoriert (ein Tabstopp-oder Leerzeichen zwischen Zeichen gibt das gleiche Ergebnis aus). Die Menge an Leerzeichen ist nicht von Bedeutung-ein Leerzeichen oder zwei Leerzeichen zwischen Zeichen haben das gleiche Ergebnis.

Die Suche generiert keine Ereignisse von "PopulateContextNode". Nur die Striche, die bereits aufgefüllt wurden, werden durchsucht.

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
</dt> </dl>

 

 




