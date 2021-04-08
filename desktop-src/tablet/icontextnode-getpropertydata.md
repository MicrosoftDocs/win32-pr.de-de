---
description: Ruft anwendungsspezifische Daten oder andere Eigenschafts Daten für den angegebenen Bezeichner ab.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'Icontextnode:: GetPropertyData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751848"
---
# <a name="icontextnodegetpropertydata-method"></a>Icontextnode:: GetPropertyData-Methode

Ruft anwendungsspezifische Daten oder andere Eigenschafts Daten für den angegebenen Bezeichner ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppropertydataid* \[ in\]
</dt> <dd>

Der Bezeichner für die Daten.

</dd> <dt>

*pulpropertydatasize* \[ in, out\]
</dt> <dd>

Die Größe der Daten in Bytes. Der Wert, der an die Übergabe erfolgt, wird nicht verwendet.

</dd> <dt>

*ppbpropertydata* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von 8-Bit-Ganzzahlen ohne Vorzeichen, das die Eigenschaften Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherfehler zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppbpropertydata* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Zusätzlich zum Abrufen von anwendungsspezifischen Daten, die mit [**icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md)hinzugefügt wurden, wird diese Methode verwendet, um allgemeine Eigenschaften abzurufen, die von den [Eigenschaften Konstanten für Kontext Knoten](context-node-properties.md) beschrieben werden.

Zu den Eigenschaften vom Typ "String" gehören:

-   GUID \_ CNP \_ erkenzedstring
-   GUID \_ CNP \_ Shapename
-   GUID \_ AHP \_ analysishintname
-   GUID \_ AHP \_ PrefixText
-   GUID- \_ AHP- \_ SuffixText
-   GUID- \_ AHP- \_ Faktoid

Der Rückgabewert ist **WCHAR \**_. Wenn Sie den Parameter \_ *ppbpropertydata* in **\* WCHAR* umwandeln,_ ist die zurückgegebene Länge `(length of the string + 1) _ sizeof(WCHAR)` .

Die Eigenschaften des booleschen Typs umfassen Folgendes:

-   GUID \_ AHP \_ overridelta anguageid
-   GUID \_ AHP \_ coercetofaktoid
-   GUID- \_ AHP- \_ wordmode

Der Rückgabewert ist **Variant \_ bool**. Wenn Sie den Parameter \* *ppbpropertydata* in **Variant \_ \* bool* _ umwandeln, ist die zurückgegebene Länge `sizeof(VARIANT_BOOL)` .

Der GUID- \_ AHP \_ -Leitfaden ist eine Eigenschaft vom Typ "Guide". Der Rückgabewert ist _*inkanalysiserkentionguide \**_. Wenn Sie den Parameter \_ *ppbpropertydata* in **inkanalysiserkentionguide \** _ umwandeln, ist die zurückgegebene Länge `sizeof(InkAnalysisRecognitionGuide)` .

Eigenschaften vom Typ "Integer" umfassen Folgendes:

-   GUID \_ CNP \_ LineNumber
-   GUID \_ CNP \_ PointsPerInch
-   GUID \_ CNP \_ conficelevel
-   GUID \_ CNP- \_ Bestätigung
-   GUID \_ CNP \_ MaximumStrokeCount
-   GUID \_ CNP- \_ Segmentierung
-   GUID \_ CNP \_ alignmentlevel

Der Rückgabewert ist _*Long \**_. Wenn Sie den \_ *ppbpropertydata* -Parameter in **Long \** _ umwandeln, ist die zurückgegebene Länge `sizeof(LONG)` .

Linienmetriken: Typeigenschaften:

-   GUID \_ CNP-Vorgänger \_
-   GUID \_ CNP-Nachfolger \_
-   GUID \_ CNP- \_ Baseline
-   GUID \_ CNP- \_ Mittellinie

Der Rückgabewert ist _*Long \**_. Wenn Sie den Parameter " \_ *ppbpropertydata* " in "**Long \** _" umwandeln, ist die zurückgegebene Länge `sizeof(LONG)_4` . Dies bedeutet, dass (x, y) Werte für die Anfangspunkte, gefolgt von den (x, y)-Werten für die Endpunkte, dargestellt werden.

GUID \_ CNP \_ textrecognizerid ist eine **GUID** -Eigenschaft. Der Rückgabewert ist **GUID \**_. Wenn Sie den Parameter \_ *ppbpropertydata* in **\* GUID* umwandeln,_ ist die zurückgegebene Länge `sizeof(GUID)` .

GUID \_ CNP \_ rotatedboundingbox ist eine gedrehte Begrenzungsfeld Eigenschaft. Der Rückgabewert ist _*Long \**_. Beim Umwandeln des \_ *ppbpropertydata* -Parameters in ** \* Long* _ ist die zurückgegebene Länge `sizeof(LONG)_8` . Dies bedeutet, dass (x, y) Werte für die vier Ecken des Felds gekennzeichnet werden.

Der GUID \_ CNP- \_ Hotpoint ist eine Hot Point-Eigenschaft. Der Rückgabewert ist **Long \**_. Wenn Sie den \_ *ppbpropertydata* -Parameter in *\** *_ zurück umwandeln, ist die zurückgegebene Länge `sizeof(LONG)_2` , die die (x, y)-Werte für den Punkt bezeichnet.

GUID \_ AHP \_ WordList ist eine Word-Listen Eigenschaft. Der Rückgabewert ist **WCHAR \**_. Wenn Sie den Parameter \_ *ppbpropertydata* in **\* WCHAR*_ umwandeln, ist die zurückgegebene Länge `n _ sizeof(WCHAR)` , wobei `n` die Summe der Zeichen folgen Längen der Anzahl von Zeichen folgen in der Liste plus 1 für jedes **null** -Beendigungs Zeichen für jede Zeichenfolge ist.

## <a name="examples"></a>Beispiele

Dieses Beispiel zeigt eine Methode, die auf die alignmentlevel-Kontext Knoten Eigenschaft eines Absatz Kontext-Knoten Typs zugreift.


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**Icontextnode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Icontextnode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**Icontextnode:: loadpropertiesdata**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**Icontextnode:: savepropertiesdata**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

