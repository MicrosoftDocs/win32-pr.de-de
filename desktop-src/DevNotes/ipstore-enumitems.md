---
description: Gibt den Schnittstellenzeiger eines Untertyps zum Aufzählen von Elementen in der geschützten Speicherdatenbank zurück.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: IPStore::EnumItems-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0b0ea4976dcfdfe2a099362e9a937ac69144bd678965c6a308cb96fed2a3c88b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001510"
---
# <a name="ipstoreenumitems-method"></a>IPStore::EnumItems-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

Gibt den Schnittstellenzeiger eines Untertyps zum Aufzählen von Elementen in der geschützten Speicherdatenbank zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
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

Ein Zeiger auf eine **GUID,** die den Datentyp des aufzählten Elements identifiziert.

</dd> <dt>

*pItemSubtype* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **GUID,** die den Datenuntertyp des aufzählenden Elements identifiziert.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Reserviert: Muss auf 0 (null) festgelegt werden.

</dd> <dt>

*ppenum* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IEnumPStoreItems-Schnittstelle.**](ienumpstoreitems.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert **PST E OK gibt \_ \_ an,** dass die Funktion erfolgreich war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
