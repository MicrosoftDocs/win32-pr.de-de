---
title: IDWriteFontFallbackBuilder AddMapping-Methode
description: Fügt eine einzelne Zuordnung an die Liste an. Rufen Sie dies einmal für jede zusätzliche Zuordnung auf.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- AddMapping-Methode " Direct Write"
- AddMapping-Methode Direct Write , IDWriteFontFallbackBuilder-Schnittstelle
- IDWriteFontFallbackBuilder-Schnittstelle Direct Write , AddMapping-Methode
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b6496ac9ef9bdfa574cc2c4710ed4620fd855dbf5eff2b22885b32bf343d141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650440"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>IDWriteFontFallbackBuilder::AddMapping-Methode

Fügt eine einzelne Zuordnung an die Liste an. Rufen Sie dies einmal für jede zusätzliche Zuordnung auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Bereiche* 
</dt> <dd>

Typ: **[ **DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\***

Unicode-Bereiche, die für diese Zuordnung gelten.

</dd> <dt>

*rangesCount* 
</dt> <dd>

Typ: **UINT32**

Anzahl der Unicode-Bereiche.

</dd> <dt>

*targetFamilyNames* \[ In\]
</dt> <dd>

Typ: **const \* \* WCHAR**

Liste der Zeichenfolgen für Zielfamiliennamen.

</dd> <dt>

*targetFamilyNamesCount* 
</dt> <dd>

Typ: **UINT32**

Anzahl der Zielfamiliennamen.

</dd> <dt>

*fontCollection* \[ in, optional\]
</dt> <dd>

Typ: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Optionale explizite Schriftartauflistung für diese Zuordnung.

</dd> <dt>

*localeName* \[ in, optional\]
</dt> <dd>

Typ: **const \* WCHAR**

Gebietsschema des Kontexts.

</dd> <dt>

*baseFamilyName* \[ in, optional\]
</dt> <dd>

Typ: **const \* WCHAR**

Basisfamilienname, mit dem ggf. eine Übereinstimmung besteht.

</dd> <dt>

*scale* 
</dt> <dd>

Typ: **FLOAT**

Skalierungsfaktor zum Multiplizieren der Zielschriftart des Ergebnisses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

