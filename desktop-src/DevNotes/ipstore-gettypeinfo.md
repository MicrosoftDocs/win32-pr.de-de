---
description: Ruft Informationen ab, die einem-Typ zugeordnet sind.
ms.assetid: 27a283a5-8924-4a2f-8f58-e673a424e28a
title: 'Ipstore:: GetTypeInfo-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetTypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: c533c30268bf8b8e879e937359471da8cd7af8b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373905"
---
# <a name="ipstoregettypeinfo-method"></a>Ipstore:: GetTypeInfo-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Ruft Informationen ab, die einem-Typ zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
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

*pType* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **GUID** , die den Datentyp des Speichers identifiziert.

</dd> <dt>

*ppinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**PST- \_ TypeInfo**](pst-typeinfo.md) -Struktur, die den Namen des Datentyps enthält.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Reserviert: muss auf 0 (null) festgelegt werden.

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

[**PST- \_ Typeingabe Info**](pst-typeinfo.md)
</dt> </dl>

 

 
