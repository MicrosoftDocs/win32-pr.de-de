---
title: Idwrite Test fontfallback-mapcharacter-Methode
description: Bestimmt eine entsprechende Schriftart, die zum Rendering des Anfangs Bereichs von Text verwendet werden soll.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Mapcharacters-Methode, direktes Schreiben
- Mapcharacters-Methode direkt schreiben, idwrite-fontfallback-Schnittstelle
- Idwrite-fontfallback-Schnittstelle Direct Write, mapcharacters-Methode
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340837"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>Idschreitefontfallback:: mapcharacters-Methode

Bestimmt eine entsprechende Schriftart, die zum Rendering des Anfangs Bereichs von Text verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Quelle* 
</dt> <dd>

Typ: **[**idschreitetextanalysissource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _

Die Textquellen Implementierung enthält den Text und das Gebiets Schema.

</dd> <dt>

_textPosition * 
</dt> <dd>

Typ: **UInt32**

Startposition, die analysiert werden soll.

</dd> <dt>

*TextLength* 
</dt> <dd>

Typ: **UInt32**

Die Länge des zu analysierenden Texts.

</dd> <dt>

*basefontcollection* \[ in, optional\]
</dt> <dd>

Typ: **[**idschreitefontcollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _

Die zu verwendende Standard Schriftart Auflistung.

</dd> <dt>

_baseFamilyName * \[ in, optional\]
</dt> <dd>

Typ: * Konstante *WCHAR \_ t \** _

Der Familienname der Basis Schriftart. Wenn Sie NULL übergeben, erfolgt keine Übereinstimmung mit der Familie.

</dd> <dt>

_baseWeight * 
</dt> <dd>

Type: **[ **dwrite \_ Schriftart \_ Weight**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

Die gewünschte Gewichtung.

</dd> <dt>

*BaseStyle* 
</dt> <dd>

Type: **[ **dwrite- \_ Schriftart \_ Stil**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

Der gewünschte Stil.

</dd> <dt>

*basestretch* 
</dt> <dd>

Typ: **[ **dwrite- \_ Schriftart \_ Streckung**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

Die gewünschte Streckung.

</dd> <dt>

*mappedlength* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32 \** _

Länge des Texts, der der zugeordneten Schriftart zugeordnet ist. Diese ist immer kleiner oder gleich der Textlänge und größer als 0 (wenn die Textlänge ungleich NULL ist), sodass der Aufrufer mindestens ein Zeichen verschiebt.

</dd> <dt>

_mappedFont * \[ out\]
</dt> <dd>

Typ: **[ **idschreiteschriftart**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

Die Schriftart, die verwendet werden soll, um die ersten *mappedlength* -Zeichen des Texts zu erzeugen. Wenn NULL zurückgegeben wird, bedeutet dies, dass der Text von keiner Schriftart gerendert werden kann, und *mappedlength* die Anzahl der zu über springenden Zeichen (mit einem fehlenden Symbol gerendert).

</dd> <dt>

*skalieren* \[ vorgenommen\]
</dt> <dd>

Typ: **float \** _

Skalierungsfaktor, um die Geviert Größe der zurückgegebenen Schriftart zu multiplizieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitefontfallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

