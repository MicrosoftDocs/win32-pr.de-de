---
description: Schreibt die Zugriffsregeln für den angegebenen Typ.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: IPStore::WriteAccessRuleset-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: a21fac6df5ab4d87e55d71e45f5698251ca4f82b6c93de1072c2ae5bcd7236aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955899"
---
# <a name="ipstorewriteaccessruleset-method"></a>IPStore::WriteAccessRuleset-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

\[Diese Methode ist nicht implementiert.\]

Schreibt die Zugriffsregeln für den angegebenen Typ.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*pType* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*pSubtype* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*pInfo* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*pRules* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Aufrufe dieser Methode führen immer zu Einem Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
