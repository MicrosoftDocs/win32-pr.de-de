---
description: Löscht das angegebene Element aus dem geschützten Speicher.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: Ipstore::D eleteitem-Methode (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368681"
---
# <a name="ipstoredeleteitem-method"></a>Ipstore::D eleteitem-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Löscht das angegebene Element aus dem geschützten Speicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
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

Ein Zeiger auf eine **GUID** , die den Datentyp des zu löschenden Elements angibt.

</dd> <dt>

*pitemsubtype* \[ in\]
</dt> <dd>

Eine **GUID** , die den zu löschenden Element Untertyp angibt.

</dd> <dt>

" *szitemname* \[ " in\]
</dt> <dd>

Eine Zeichenfolge, die den Namen des zu löschenden Elements enthält.

</dd> <dt>

*ppromptinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**PST- \_ promptinfo**](pst-promptinfo.md) -Struktur.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Gibt die Benutzeroberfläche und das Sicherheits Verhalten für den Löschvorgang an.



| Wert                                                                                                                                                                                                                                             | Bedeutung                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ Keine \_ UI- \_ Migration**</dt> <dt>0x00000010</dt> </dl> | Zeigen Sie die Benutzeroberfläche nur an, wenn ein benutzerdefiniertes Kennwort erforderlich ist.<br/> |



 

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

 

 
