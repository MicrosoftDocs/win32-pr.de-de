---
description: Gibt eine Schnittstelle zum Aufzählen von Typen zurück, die derzeit in der geschützten Datenbank registriert sind.
ms.assetid: 0c0c2ad7-90b0-4fc0-8972-82eb159653be
title: IPStore::EnumTypes-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: c44429b4145158bc54e52d700546a29caf3e9665d38e51679e596adbdec6c3b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827113"
---
# <a name="ipstoreenumtypes-method"></a>IPStore::EnumTypes-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Gibt eine Schnittstelle zum Aufzählen von Typen zurück, die derzeit in der geschützten Datenbank registriert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumTypes(
  [in] PST_KEY          Key,
  [in] DWORD            dwFlags,
  [in] IEnumPStoreTypes **ppenum
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

*dwFlags* \[ In\]
</dt> <dd>

Reserviert: Muss auf 0 (null) festgelegt werden.

</dd> <dt>

*ppenum* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**IEnumPStoreTypes-Schnittstelle,**](ienumpstoretypes.md) die zum Ausführen der Enumerationsaufgaben verwendet wird.

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

 

 
