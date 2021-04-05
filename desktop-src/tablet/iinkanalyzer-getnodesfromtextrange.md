---
description: Ruft eine Auflistung von icontextnode-Objekten ab, die für den angegebenen Textbereich für die angegebenen Kontext Knoten relevant sind.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'Iinkanalyzer:: GetNodesFromTextRange-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751809"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a>Iinkanalyzer:: GetNodesFromTextRange-Methode

Ruft eine Auflistung von [**icontextnode**](icontextnode.md) -Objekten ab, die für den angegebenen Textbereich für die angegebenen Kontext Knoten relevant sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plstart* \[ in, out\]
</dt> <dd>

Ein Verweis auf den Anfang des Text Bereichs im *pnoentstosearch* -Teil der erkannten Zeichenfolge.

</dd> <dt>

*pllength* \[ in, out\]
</dt> <dd>

Ein Verweis auf die Länge des Text Bereichs im *pnoentstosearch* -Teil der erkannten Zeichenfolge.

</dd> <dt>

*ppcontextnodes* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die [**icontextnode**](icontextnode.md) -Objekte, die für den angegebenen Textbereich für die angegebenen Kontext Knoten relevant sind.

</dd> <dt>

*pnodebug Search* \[ in\]
</dt> <dd>

Die [**icontextnode**](icontextnode.md) -Objekte, auf die die Suche beschränkt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Der angegebene Textbereich muss relativ zum " *pnodebug Search* "-Teil der erkannten Zeichenfolge des " [**iinkanalyzer**](iinkanalyzer.md)" und nicht zur erkannten Zeichenfolge des gesamten " **iinkanalyzer**" sein.

Diese Methode ändert die Werte der *plstart* -und *pllength* -Parameter, indem der Textbereich auf die nächstgelegenen Wortgrenzen erweitert wird.

Wenn die erkannte Zeichenfolge z. b. "I am late" lautet und Sie diese Methode mit den Parameterwerten 6 für *plstart* und 1 für *pllength* aufrufen, was dem Buchstaben "a" in "Late" entspricht, gibt diese Methode eine Auflistung mit einem einzelnen [**icontextnode**](icontextnode.md), dem InkWord oder textword zurück, das dem Wort "Late" entspricht. In diesem Beispiel ändert diese Methode auch den Wert von *plstart* in 5 und den Wert von *pllength* in 4, was dem Wort "Late" entspricht.

> [!Note]  
> Der *plstart* -Parameter ist relativ zur erkannten Zeichenfolge des *pnodebug Search* -Parameters.

 

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

 

 




