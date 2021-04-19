---
description: Erstellt den angegebenen Untertyp innerhalb des angegebenen Typs.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'Ipstore:: kreatesubtype-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352863"
---
# <a name="ipstorecreatesubtype-method"></a>Ipstore:: kreatesubtype-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Erstellt den angegebenen Untertyp innerhalb des angegebenen Typs.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSubtype(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Gibt den Speicherbereich des Anbieters an.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt> </dl>    | Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt> </dl> | Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.<br/> |



 

</dd> <dt>

*pType* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **GUID** , die den Datentyp des Speichers identifiziert.

</dd> <dt>

*psubtype* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **GUID** , die den Daten Untertyp des Speichers identifiziert.

</dd> <dt>

*pinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**PST- \_ TypInfo**](pst-typeinfo.md) -Struktur.

</dd> <dt>

*prules* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**PST- \_ accessruleset**](pst-accessruleset.md) -Struktur.

**Windows XP:** Dieser Parameter wird ignoriert.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Bleiben muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT** -Wert. Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipstore**](ipstore.md)
</dt> <dt>

[**PST- \_ accessruleset**](pst-accessruleset.md)
</dt> <dt>

[**PST- \_ Typeingabe Info**](pst-typeinfo.md)
</dt> </dl>

 

 
