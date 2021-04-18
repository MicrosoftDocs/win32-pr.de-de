---
description: Liest die Zugriffsregeln für einen angegebenen Typ.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'Ipstore:: Read accessruleset-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371226"
---
# <a name="ipstorereadaccessruleset-method"></a>Ipstore:: Read accessruleset-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

\[Diese Methode ist nicht implementiert.\]

Liest die Zugriffsregeln für einen angegebenen Typ.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Reserviert.

</dd> <dt>

*pType* \[ in\]
</dt> <dd>

Reserviert.

</dd> <dt>

*psubtype* \[ in\]
</dt> <dd>

Reserviert.

</dd> <dt>

*pinfo* \[ in\]
</dt> <dd>

Reserviert.

</dd> <dt>

*pprules* \[ in\]
</dt> <dd>

Reserviert.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Aufrufen dieser Methode tritt immer ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipstore**](ipstore.md)
</dt> </dl>

 

 
