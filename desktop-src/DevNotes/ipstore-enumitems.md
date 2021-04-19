---
description: Gibt den Schnittstellen Zeiger eines Untertyps zum Aufzählen von Elementen in der geschützten Speicher Datenbank zurück.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: 'Ipstore:: tumitems-Methode (pstore. h)'
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
ms.openlocfilehash: 9b44ee41a7daa4a75a19ca0f7045d69f5b380c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369630"
---
# <a name="ipstoreenumitems-method"></a>Ipstore:: endms-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Gibt den Schnittstellen Zeiger eines Untertyps zum Aufzählen von Elementen in der geschützten Speicher Datenbank zurück.

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

Ein Zeiger auf eine **GUID** , die den Datentyp des aufzuzählenden Elements identifiziert.

</dd> <dt>

*pitemsubtype* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **GUID** , die den Daten Untertyp des aufzuzählenden Elements identifiziert.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Reserviert: muss auf 0 (null) festgelegt werden.

</dd> <dt>

*ppum* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**iumumpstoreitems**](ienumpstoreitems.md) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipstore**](ipstore.md)
</dt> </dl>

 

 
