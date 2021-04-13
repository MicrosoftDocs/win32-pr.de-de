---
title: Idwrite-fontfallbackbuilder-AddMapping-Methode
description: Fügt eine einzelne Zuordnung an die Liste an. Dies wird einmal für jede weitere Zuordnung aufgerufen.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Direkte Schreibweise von AddMapping-Methode
- AddMapping-Methode Direct Write, idwrite Test fontfallbackbuilder-Schnittstelle
- Idwrite-fontfallbackbuilder-Schnittstelle Direct Write, AddMapping-Methode
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
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392043"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>Idschreitefontfallbackbuilder:: AddMapping-Methode

Fügt eine einzelne Zuordnung an die Liste an. Dies wird einmal für jede weitere Zuordnung aufgerufen.

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

*Ketten* 
</dt> <dd>

Typ: **[**dwrite- \_ Unicode- \_ Bereich**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range) \** _

Unicode-Bereiche, die für diese Zuordnung gelten.

</dd> <dt>

_rangesCount * 
</dt> <dd>

Typ: **UInt32**

Anzahl von Unicode-Bereichen.

</dd> <dt>

*targetfamilynames* \[ in\]
</dt> <dd>

Typ: Konstante **WCHAR \* \***

Liste der Ziel Familiennamen-Zeichen folgen.

</dd> <dt>

*targetfamilynamescount* 
</dt> <dd>

Typ: **UInt32**

Anzahl der Ziel Familiennamen.

</dd> <dt>

*FontCollection* \[ in, optional\]
</dt> <dd>

Typ: **[ **idschreitefontcollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Optionale explizite Schriftart Auflistung für diese Zuordnung.

</dd> <dt>

*localename* \[ in, optional\]
</dt> <dd>

Typ: * Konstante *WCHAR \** _

Das Gebiets Schema des Kontexts.

</dd> <dt>

_baseFamilyName * \[ in, optional\]
</dt> <dd>

Typ: * Konstante *WCHAR \** _

Der Basis Familienname für den Abgleich, falls zutreffend.

</dd> <dt>

_scale * 
</dt> <dd>

Typ: **float**

Der Skalierungsfaktor zum Multiplizieren der Ergebnisziel Schriftart.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitefontfallbackbuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

