---
description: Löscht einen angegebenen Untertyp aus dem angegebenen Typ.
ms.assetid: 1c44a609-80af-4e28-b1b5-2b4faea143bd
title: IPStore::D eleteSubtype-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 88bb437c89073f3601050c1246f1e59b136a85955da4697d338077343a4d1bc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001610"
---
# <a name="ipstoredeletesubtype-method"></a>IPStore::D eleteSubtype-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

Löscht einen angegebenen Untertyp aus dem angegebenen Typ.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteSubtype(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in] const GUID    *pSubtype,
  [in]       DWORD   dwFlags
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

*pType* \[ In\]
</dt> <dd>

Ein Zeiger auf eine GUID, die den Datentyp des Speichers identifiziert.

</dd> <dt>

*pSubtype* \[ In\]
</dt> <dd>

Ein Zeiger auf eine GUID, die den Datenuntertyp des Speichers identifiziert.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Reserviert: Muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT-Wert.** Der Wert **PST E OK gibt \_ \_ an,** dass die Funktion erfolgreich war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
