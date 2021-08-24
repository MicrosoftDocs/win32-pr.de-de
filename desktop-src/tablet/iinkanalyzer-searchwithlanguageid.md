---
description: 'IInkAnalyzer::SearchWithLanguageId-Methode: Stellt eine ausdrucksbasierte Fuzzysuche bereit, bei der die Groß-/Kleinschreibung nicht beachtet wird, um analysierte Schreibstriche und analysierte Zeichnungsstriche mit erkannten Typen zu suchen.'
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
ms.openlocfilehash: 922cbd2110149ac27041be41ccd24a601e87b5355351e0774a80eb636461c21f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590350"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a>IInkAnalyzer::SearchWithLanguageId-Methode

Stellt eine ausdrucksbasierte Fuzzysuche bereit, bei der die Groß-/Kleinschreibung nicht beachtet wird, um analysierte Schreibstriche und analysierte Zeichnungsstriche mit erkannten Typen zu suchen.

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

Die LCID, die der übergebenen Zeichenfolge zugeordnet ist. Wird verwendet, um die Groß-/Kleinschreibung intern zu konvertieren, um Vergleiche ohne Unterscheidung von Groß-/Kleinschreibung zu unterstützen.

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

Zeiger auf ein Array von Strich-IDs, die eine Gruppe von Strichen darstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Bei dieser Suche werden Teilzeichenfolgen mit mehreren Wörtern und einzelnen Wörtern gesucht. Sowohl alternative Erkennungsergebnisse als auch alternative Segmentierungen werden durchsucht.

Alle eingehenden Zeichenfolgen werden für den Vergleich mithilfe der LCID des aktuellen Threads in eine einzelne Groß-/Kleinschreibung konvertiert, um diese Konvertierung unter Beachtung von Kulturfallkonventionen durchführen zu können.

Die übergebene Zeichenfolge wird als Ausdruck behandelt. Wörter und Zeichen müssen in den Alterantes für die Striche in der angegebenen Reihenfolge angezeigt werden. Die ersten und letzten Wörter des Ausdrucks können als Teilzeichenfolgen abgeglichen werden (das erste Wort, das am Ende eines alternativen und das letzte Wort beim Umbetten eines worts angezeigt wird), aber alle anderen Wörter (innerhalb des Ausdrucks) müssen als ganze Wörter angezeigt werden.

Wenn die übergebene Zeichenfolge keine Leerzeichen zwischen Zeichen enthält, befindet sich die Teilzeichenfolge möglicherweise an einer beliebigen Stelle innerhalb eines einzelnen Worts in einer alternativen Zeichenfolge.

Nur das Vorhandensein oder Fehlen von Leerzeichen zwischen Zeichen ändert die Ergebnisse der Suche. Leerzeichen, die nicht von Zeichen umgeben sind, werden ignoriert. Der Typ des Leerraums wird ignoriert (eine Registerkarte oder ein Leerzeichen zwischen Zeichen führt zum gleichen Ergebnis). Die Leerraummenge spielt keine Rolle. Ein oder zwei Leerzeichen zwischen Zeichen führen zum gleichen Ergebnis.

Die Suche generiert keine PopulateContextNode-Ereignisse. Nur die Striche, die bereits aufgefüllt wurden, werden durchsucht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




