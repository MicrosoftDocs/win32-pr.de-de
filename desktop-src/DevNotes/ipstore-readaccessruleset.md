---
description: Liest die Zugriffsregeln für einen bestimmten Typ.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: IPStore::ReadAccessRuleSet-Methode (Pstore.h)
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
ms.openlocfilehash: d22f56c14df4d11a8979065ede81ab8418909033ffd816a233a18c51af7f66c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749750"
---
# <a name="ipstorereadaccessruleset-method"></a>IPStore::ReadAccessRuleSet-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

\[Diese Methode ist nicht implementiert.\]

Liest die Zugriffsregeln für einen bestimmten Typ.

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

*ppRules* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Aufrufe dieser Methode schlagen immer fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
