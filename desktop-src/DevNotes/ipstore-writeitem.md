---
description: Schreibt ein Datenelement in den geschützten Speicher.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'Ipstore:: Write teitem-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370751"
---
# <a name="ipstorewriteitem-method"></a>Ipstore:: Write teitem-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Schreibt ein Datenelement in den geschützten Speicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Der Speicherbereich des Anbieters.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt> </dl>    | Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt> </dl> | Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.<br/> |



 

</dd> <dt>

*pitemtype* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **GUID** , die den Datentyp des Datenelements identifiziert, das geschrieben wird.

</dd> <dt>

*pitemsubtype* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **GUID** , die den Daten Untertyp des Datenelements identifiziert, das geschrieben wird.

</dd> <dt>

" *szitemname* \[ " in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen enthält, der dem gespeicherten Datenelement zugewiesen ist.

</dd> <dt>

*cbData* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein **DWORD** , das die Größe des Puffers angibt, der das gespeicherte Datenelement enthält.

</dd> <dt>

*ppbdata* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der das Datenelement enthält, das geschrieben wird.

</dd> <dt>

*pproomptinfo* \[ in\]
</dt> <dd>

Zeiger auf eine [**PST- \_ promptinfo**](pst-promptinfo.md) -Struktur.

</dd> <dt>

*dwdefaultconfirmationstyle* \[ in\]
</dt> <dd>

Der standardmäßige Bestätigungs Stil.



| Wert                                                                                                                                                                                                                             | Bedeutung                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**PST \_ CF \_ Standard**</dt> <dt>0x00000000</dt> </dl> | Ermöglicht es dem Benutzer, den Bestätigungs Stil auszuwählen. <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**PST \_ CF \_ None**</dt> <dt>0x00000001</dt> </dl>          | Erzwingt die Erstellung eines automatischen Elements. <br/>                      |



 

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Die Benutzeroberfläche und das Sicherheits Verhalten für den Schreibvorgang.



| Wert                                                                                                                                                                                                                                                              | Bedeutung                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**PST \_ Kein über \_ Schreiben**</dt> <dt>0x00000002</dt> </dl>                            | Gibt an, dass das Element im geschützten Speicher erstellt wird. Das Überschreiben eines vorhandenen Elements ist nicht zulässig.<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ Uneingeschränktes \_ ItemData**</dt> <dt>0x00000004</dt> </dl> | Gibt an, dass der Datenstrom nicht sicher ist. Standardmäßig sind Element Aufrufe sicher.<br/>                         |



 

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

[**PST \_ promptinfo**](pst-promptinfo.md)
</dt> </dl>

 

 
