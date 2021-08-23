---
description: Ruft anwendungsspezifische Daten oder andere Eigenschaftsdaten für den angegebenen Bezeichner ab.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: IContextNode::GetPropertyData-Methode (IACom.h)
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
ms.openlocfilehash: 89e7ab9fb5213b41d53695b516b95b47193e8d803b207efd09216c743085927e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660720"
---
# <a name="icontextnodegetpropertydata-method"></a>IContextNode::GetPropertyData-Methode

Ruft anwendungsspezifische Daten oder andere Eigenschaftsdaten für den angegebenen Bezeichner ab.

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

*pPropertyDataId* \[ In\]
</dt> <dd>

Der Bezeichner für die Daten.

</dd> <dt>

*pulPropertyDataSize* \[ in, out\]
</dt> <dd>

Die Größe der Daten in Bytes. Der übergebene Wert wird nicht verwendet.

</dd> <dt>

*ppbPropertyData* \[ out\]
</dt> <dd>

Ein Zeiger auf ein 8-Bit-Ganzzahlarray ohne Vorzeichen, das die Eigenschaftsdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, verwenden Sie [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher aus \* *ppbPropertyData* frei zu geben, wenn Sie die Informationen nicht mehr benötigen.

 

Zusätzlich zum Abrufen anwendungsspezifischer Daten, die mit [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)hinzugefügt wurden, wird diese Methode [](context-node-properties.md) verwendet, um allgemeine Eigenschaften abzurufen, die von den Konstanten der Kontextknoteneigenschaften beschrieben werden.

Zu den Zeichenfolgentypeigenschaften gehören:

-   GUID \_ CNP \_ RECOGNIZEDSTRING
-   GUID \_ CNP \_ SHAPENAME
-   GUID \_ AHP \_ ANALYSISHINTNAME
-   GUID \_ AHP \_ PREFIXTEXT
-   \_GUID-AHP-SUFFIXTEXT \_
-   \_ \_ GUID-AHP-FACTOID

Der Rückgabewert ist **WCHAR \**_. Wenn Sie den \_ *ppbPropertyData-Parameter* in **WCHAR \* casten,*_ ist die zurückgegebene Länge `(length of the string + 1) _ sizeof(WCHAR)` .

Zu den Eigenschaften des booleschen Typs gehören:

-   GUID \_ AHP \_ OVERRIDELANGUAGEID
-   GUID \_ AHP \_ COERCETOFACTOID
-   GUID \_ AHP \_ WORDMODE

Der Rückgabewert ist **VARIANT \_ BOOL.** Wenn Sie den \* *ppbPropertyData-Parameter* in **VARIANT \_ BOOL \*** umbenennen, ist die zurückgegebene Länge `sizeof(VARIANT_BOOL)` .

GUID \_ AHP \_ GUIDE ist eine Guide-Type-Eigenschaft. Der Rückgabewert ist **InkAnalysisRecognitionGuide \** _. Wenn Sie den \_ *ppbPropertyData-Parameter* **in \* InkAnalysisRecognitionGuide** casten, ist die zurückgegebene Länge `sizeof(InkAnalysisRecognitionGuide)` .

Eigenschaften vom Typ "Integer" umfassen Folgendes:

-   GUID \_ CNP \_ LINENUMBER
-   GUID \_ CNP \_ POINTSPERINCH
-   GUID \_ CNP \_ CONFIDENCELEVEL
-   \_GUID-CNP-BESTÄTIGUNG \_
-   GUID \_ CNP \_ MAXIMUMSTROKECOUNT
-   \_GUID-CNP-SEGMENTIERUNG \_
-   GUID \_ CNP \_ ALIGNMENTLEVEL

Der Rückgabewert ist **LONG \** _. Wenn Sie den \_ *ppbPropertyData-Parameter* in LONG umbenennen, **\*** ist die zurückgegebene Länge `sizeof(LONG)` .

Eigenschaften vom Typ "Zeilenmetriken" umfassen Folgendes:

-   GUID \_ CNP \_ ASCENDERS
-   GUID \_ CNP \_ DESCENDERS
-   \_GUID-CNP-BASELINE \_
-   GUID \_ CNP \_ MIDLINE

Der Rückgabewert ist **LONG \**_. Wenn Sie den \_ *ppbPropertyData-Parameter* *\**_ in * LONG umstellen, ist die zurückgegebene Länge , was die (x, y)-Werte für die Ausgangspunkte angibt, gefolgt von `sizeof(LONG)_4` den (x, y)-Werten für die Endpunkte.

GUID \_ CNP \_ TEXTRECOGNIZERID ist eine **GUID-Eigenschaft.** Der Rückgabewert ist **GUID \** _. Wenn Sie den \_ *ppbPropertyData-Parameter in* **GUID \* umwanden,** ist die zurückgegebene Länge `sizeof(GUID)` .

GUID \_ CNP \_ ROTATEDBOUNDINGBOX ist eine gedrehte Begrenzungsfeldeigenschaft. Der Rückgabewert ist **LONG \**_. Wenn Sie den \_ *ppbPropertyData-Parameter* *\**_ in * LONG umschreiben, ist die zurückgegebene Länge , was die Werte (x, y) für die vier Ecken des `sizeof(LONG)_8` Felds angibt.

GUID \_ CNP \_ HOTPOINT ist eine Hot Point-Eigenschaft. Der Rückgabewert ist **LONG \**_. Wenn Sie den \_ *ppbPropertyData-Parameter* *\**_ in * LONG umschreiben, ist die zurückgegebene Länge , was die `sizeof(LONG)_2` (x, y)-Werte für den Punkt angibt.

GUID \_ AHP \_ WORDLIST ist eine Wortlisteneigenschaft. Der Rückgabewert ist **WCHAR \**_. Wenn Sie den \_ *ppbPropertyData-Parameter* in **WCHAR \**_ casten, ist die zurückgegebene Länge , wobei die Summe der Zeichenfolgenlängen der Anzahl von Zeichenfolgen in der Liste plus 1 für jedes `n _ sizeof(WCHAR)` `n` NULL-Beendigungszeichen  für jede Zeichenfolge ist.

## <a name="examples"></a>Beispiele

Dieses Beispiel zeigt eine Methode, die auf die AlignmentLevel-Kontextknoteneigenschaft eines Paragraph-Kontextknotentyps zusteuert.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

