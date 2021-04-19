---
description: Öffnet ein Element für mehrere Zugriffe.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'Ipstore:: OpenItem-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353798"
---
# <a name="ipstoreopenitem-method"></a>Ipstore:: OpenItem-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Öffnet ein Element für mehrere Zugriffe.

## <a name="syntax"></a>Syntax


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Gibt an, ob der Typ auf dem Computer lokal ist oder nur dem erstellerstellerbenutzer zugeordnet ist.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt> </dl>    | Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt> </dl> | Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.<br/> |



 

</dd> <dt>

*pitemtype* \[ in\]
</dt> <dd>

Ein Zeiger auf eine GUID, die den Datentyp des zu öffnenden Elements identifiziert.

</dd> <dt>

*pitemsubtype* \[ in\]
</dt> <dd>

Ein Zeiger auf eine GUID, die den zu öffnenden Element Untertyp angibt.

</dd> <dt>

" *szitemname* \[ " in\]
</dt> <dd>

Eine Zeichenfolge, die den Namen des zu öffnenden Elements enthält.

</dd> <dt>

*Modeflags* \[ in\]
</dt> <dd>

Beschreibt die Zugriffs Modi, auf die sich ein angegebener Satz von Zugriffs Klauseln bezieht. Weitere Informationen finden Sie unter [**pstore-Typen**](pstore-types.md).



| Wert                                                                                                                                                                                                         | Bedeutung                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_ Lesen**</dt> von <dt>0x0001</dt> </dl>    | Lese Zugriffsmodus.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_ Schreiben**</dt> von <dt>0x0002</dt> </dl> | Schreibzugriffs Modus.<br/> |



 

</dd> <dt>

*pproomptinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**PST- \_ promptinfo**](pst-promptinfo.md) -Struktur.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Reserviert: muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT** -Wert. Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein Element in der geschützten Speicher Datenbank mithilfe von **OpenItem** öffnen, muss es schließlich mithilfe von [**ipstore:: closeitem**](ipstore-closeitem.md) geschlossen werden, um einen Speicherplatz zu verhindern.

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

 

 
