---
description: Legt die angegebenen Parameterinformationen fest.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: IPStore::SetProvParam-Methode (Pstore.h)
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
ms.openlocfilehash: 9ec106cd4558ddab7fd8bc430088f1bd7d721d7122f77166dfe0da7de35f1787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749720"
---
# <a name="ipstoresetprovparam-method"></a>IPStore::SetProvParam-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

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

*dwParam* \[ In\]
</dt> <dd>

Enthält **PST PP FLUSH PW \_ \_ \_ \_ CACHE** zum Leeren des Benutzerkennwortcaches.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Die Länge des Kennworts im Puffer.

</dd> <dt>

*pbData* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der das Kennwort des Benutzers enthält. Dieser muss auf NULL **festgelegt werden.**

</dd> <dt>

*dwFlags* 
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
