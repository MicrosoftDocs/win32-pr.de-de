---
description: Löscht einen angegebenen Typ aus der geschützten Speicherdatenbank.
ms.assetid: 5e3a08eb-e16b-4d9f-82be-241eb3137d17
title: IPStore::D eleteType-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 719918c980717784a680d462500295e916adf4f86d605db2c4f555cf77e10d67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667423"
---
# <a name="ipstoredeletetype-method"></a>IPStore::D eleteType-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Löscht einen angegebenen Typ aus der geschützten Speicherdatenbank.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteType(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Gibt an, ob der Typ lokal auf dem Computer ist oder nur dem erstellenden Benutzer zugeordnet ist.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ KEY \_ CURRENT \_ USER**</dt> <dt>0x00000000</dt> </dl>    | Der Speicher wird im aktuellen Benutzerabschnitt der Registrierung verwaltet.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ KEY \_ LOCAL \_ MACHINE**</dt> <dt>0x00000001</dt> </dl> | Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.<br/> |



 

</dd> <dt>

*pType* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **GUID,** die den Datentyp des Speichers identifiziert.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Reserviert: Muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT-Wert.** Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
