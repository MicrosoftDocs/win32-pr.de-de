---
description: Enthält Informationen zu einem Smartcard-Kryptografiedienstanbieter (CSP).
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: KERB_SMARTCARD_CSP_INFO-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190c3e770a50acb7363fb10c469a7400831bc7b512d2b8158d687c83403b6df9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127340"
---
# <a name="kerb_smartcard_csp_info-structure"></a>KERB \_ SMARTCARD \_ CSP \_ INFO-Struktur

Die **KERB \_ SMARTCARD \_ CSP \_ INFO-Struktur** enthält Informationen zu einem [*Smartcard-Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP).

Diese Struktur wird nicht in einem öffentlichen Header deklariert.

## <a name="syntax"></a>Syntax


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCspInfoLen**
</dt> <dd>

Die Größe dieser Struktur in Bytes, einschließlich aller angefügten Daten.

</dd> <dt>

**MessageType**
</dt> <dd>

Der Typ der übergebenen Nachricht. Dieser Member muss auf 1 festgelegt werden.

</dd> <dt>

**Contextinformation**
</dt> <dd>

Reserviert.

</dd> <dt>

**SpaceHolderForWow64**
</dt> <dd>

Reserviert.

</dd> <dt>

**flags**
</dt> <dd>

Reserviert.

</dd> <dt>

**KeySpec**
</dt> <dd>

Der private Schlüssel, der aus dem Im Puffer **bBuffer** angegebenen Schlüsselcontainer verwendet werden soll. Der Schlüssel kann einer der folgenden Werte sein, der in WinCrypt.h definiert ist.



| Wert                                                                                                                                                                                                                   | Bedeutung                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**AT \_ KEYEXCHANGE**</dt> <dt>1</dt> </dl> | Der Schlüssel ist ein Schlüsselaustauschschlüssel.<br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**AT \_ SIGNATURE**</dt> <dt>2</dt> </dl>       | Der Schlüssel ist ein Signaturschlüssel.<br/>    |



 

</dd> <dt>

**nCardNameOffset**
</dt> <dd>

Die Anzahl der Zeichen im **bBuffer-Puffer,** die dem Namen der Smartcard in diesem Puffer vorangestellt sind.

> [!IMPORTANT]
> Wenn der Name der Smartcard nicht angegeben wird, muss der Puffer eine leere Zeichenfolge enthalten.

 

</dd> <dt>

**nReaderNameOffset**
</dt> <dd>

Die Anzahl der Zeichen im **bBuffer-Puffer,** die dem Namen des Smartcardlesers in diesem Puffer vorangestellt sind.

> [!IMPORTANT]
> Wenn der Name des Smartcardlesers nicht angegeben wird, muss der Puffer eine leere Zeichenfolge enthalten.

 

</dd> <dt>

**nContainerNameOffset**
</dt> <dd>

Die Anzahl der Zeichen im **bBuffer-Puffer,** die dem Namen des Schlüsselcontainers in diesem Puffer vorangestellt sind. Diese Zeichenfolge darf nicht leer sein.

</dd> <dt>

**nCSPNameOffset**
</dt> <dd>

Die Anzahl der Zeichen im **bBuffer-Puffer,** die dem Namen des CSP in diesem Puffer vorangestellt sind.

</dd> <dt>

**bBuffer**
</dt> <dd>

Ein Array von Zeichen, die mit einer Länge von initialisiert `sizeof(DWORD)` werden. Dieser Puffer enthält die Namen, auf die von den **Membern nCardNameOffset,** **nReaderNameOffset,** **nContainerNameOffset** und **nCSPNameOffset** verwiesen wird, sowie alle zusätzlichen Daten, die vom CSP bereitgestellt werden.

Alle Namen, die nicht bereitgestellt werden, müssen in diesem Puffer durch leere Zeichenfolgen dargestellt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn diese Struktur serialisiert wird, müssen die Strukturmember an Begrenzungen ausgerichtet werden, die ein Vielfaches von 2 Bytes sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_KERB-ZERTIFIKATANMELDUNG \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
