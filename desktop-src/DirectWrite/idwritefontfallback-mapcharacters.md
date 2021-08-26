---
title: IDWriteFontFallback MapCharacters-Methode
description: Bestimmt eine geeignete Schriftart, die zum Rendern des Anfangsbereichs von Text verwendet werden soll.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- MapCharacters-Methode – Direkter Schreibzugriff
- MapCharacters-Methode Direct Write, IDWriteFontFallback-Schnittstelle
- IDWriteFontFallback-Schnittstelle Direct Write , MapCharacters-Methode
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
ms.openlocfilehash: 99f18932121d44f61d67c8124faa2d26638035bdcff473ad26c4222ceea9a85b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048790"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>IDWriteFontFallback::MapCharacters-Methode

Bestimmt eine geeignete Schriftart, die zum Rendern des Anfangsbereichs von Text verwendet werden soll.

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

*source* 
</dt> <dd>

Typ: **[ **IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\***

Die Textquellenimplementierung enthält den Text und das Locale.

</dd> <dt>

*textPosition* 
</dt> <dd>

Typ: **UINT32**

Startposition, die analysiert werden soll.

</dd> <dt>

*textLength* 
</dt> <dd>

Typ: **UINT32**

Länge des zu analysierenden Texts.

</dd> <dt>

*baseFontCollection* \[ in, optional\]
</dt> <dd>

Typ: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\***

Zu verwendende Standardschriftartauf auflistung.

</dd> <dt>

*baseFamilyName* \[ in, optional\]
</dt> <dd>

Typ: **const wchar \_ t \***

Der Familienname der Basisschriftart. Wenn Sie NULL übergeben, wird keine Übereinstimmung mit der Familie durchgeführt.

</dd> <dt>

*baseWeight* 
</dt> <dd>

Typ: **[ **SCHRIFTGRAD "DWRITE" \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

Die gewünschte Gewichtung.

</dd> <dt>

*baseStyle* 
</dt> <dd>

Typ: **[ **DWRITE-SCHRIFTSCHNITT \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

Der gewünschte Stil.

</dd> <dt>

*baseStretch* 
</dt> <dd>

Typ: **[ **DWRITE \_ FONT \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

Die gewünschte Streckung.

</dd> <dt>

*mappedLength* \[ out\]
</dt> <dd>

Typ: **UINT32 \***

Länge des Texts, der der zugeordneten Schriftart zugeordnet ist. Dies ist immer kleiner oder gleich der Textlänge und größer als 0 (null), sodass der Aufrufer mindestens ein Zeichen vorangestellt wird.

</dd> <dt>

*mappedFont* \[ out\]
</dt> <dd>

Typ: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

Die Schriftart, die zum Rendern der ersten *mappedLength-Zeichen* des Texts verwendet werden soll. Wenn NULL zurückgegeben wird, bedeutet dies, dass keine Schriftart den Text rendern kann, und *mappedLength* ist die Anzahl der zu überspringenden Zeichen (gerendert mit einem fehlenden Glyphen).

</dd> <dt>

*Scale (Skalieren* \[ out\]
</dt> <dd>

Typ: **\* FLOAT**

Skalierungsfaktor zum Multiplizieren der Ge em-Größe der zurückgegebenen Schriftart mit .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

