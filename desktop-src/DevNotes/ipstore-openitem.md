---
description: Öffnet ein Element für mehrere Zugriffe.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: IPStore::OpenItem-Methode (Pstore.h)
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
ms.openlocfilehash: 8817930f19e519083df083ac3a6d81bd5c48f8f649847c5ef9f86d3ff4cee9d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004210"
---
# <a name="ipstoreopenitem-method"></a>IPStore::OpenItem-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

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

*Schlüssel* \[ In\]
</dt> <dd>

Gibt an, ob der Typ für den Computer lokal ist oder nur dem erstellenden Benutzer zugeordnet ist.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ KEY \_ CURRENT \_ USER**</dt> <dt>0X00000000</dt> </dl>    | Der Speicher wird im aktuellen Benutzerabschnitt der Registrierung verwaltet.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ KEY \_ LOCAL \_ MACHINE**</dt> <dt>0X00000001</dt> </dl> | Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.<br/> |



 

</dd> <dt>

*pItemType* \[ In\]
</dt> <dd>

Ein Zeiger auf eine GUID, die den Datentyp des zu öffnenden Elements identifiziert.

</dd> <dt>

*pItemSubtype* \[ In\]
</dt> <dd>

Ein Zeiger auf eine GUID, die den zu öffnenden Elementuntertyp angibt.

</dd> <dt>

*szItemName* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die den Namen des zu öffnenden Elements enthält.

</dd> <dt>

*ModeFlags* \[ In\]
</dt> <dd>

Beschreibt die Zugriffsmodi, auf die sich ein angegebener Satz von Zugriffsklauseln bezieht. Weitere Informationen finden Sie unter [**PStore-Typen.**](pstore-types.md)



| Wert                                                                                                                                                                                                         | Bedeutung                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_ READ**</dt> <dt>0x0001</dt> </dl>    | Lesezugriffsmodus.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_ WRITE**</dt> <dt>0x0002</dt> </dl> | Schreibzugriffsmodus.<br/> |



 

</dd> <dt>

*pProomptInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**PST \_ PROMPTINFO-Struktur.**](pst-promptinfo.md)

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Reserviert: Muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT-Wert.** Der Wert **PST E OK gibt \_ \_ an,** dass die Funktion erfolgreich war.

## <a name="remarks"></a>Hinweise

Die **Verwendung von OpenItem** zum Öffnen eines Elements in der geschützten Speicherdatenbank erfordert, dass es schließlich mit [**IPStore::CloseItem**](ipstore-closeitem.md) geschlossen wird, um einen Speicherverlust zu verhindern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)
</dt> </dl>

 

 
