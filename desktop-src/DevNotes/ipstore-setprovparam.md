---
description: Legt die angegebenen Parameterinformationen fest.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'Ipstore:: setprovparam-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: edbbb7bd2f5d889568623390d805659e1cf840f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358235"
---
# <a name="ipstoresetprovparam-method"></a>Ipstore:: setprovparam-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Legt die angegebenen Parameterinformationen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwparam* \[ in\]
</dt> <dd>

Enthält den PST-ping- **\_ \_ \_ PW- \_ Cache** , um den Benutzer Kenn Wort Cache zu leeren.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Die Länge des Kennworts im Puffer.

</dd> <dt>

*pbData* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der das Kennwort des Benutzers enthält. Diese muss auf **null** festgelegt werden.

</dd> <dt>

*dwFlags* 
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
</dt> </dl>

 

 
