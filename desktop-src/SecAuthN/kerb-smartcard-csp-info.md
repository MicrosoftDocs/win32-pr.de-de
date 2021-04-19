---
description: Enthält Informationen zu einem Smartcard-Kryptografiedienstanbieter (CSP).
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: KERB_SMARTCARD_CSP_INFO Struktur
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
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363524"
---
# <a name="kerb_smartcard_csp_info-structure"></a>KERB \_ Smartcard- \_ CSP- \_ Informationsstruktur

Die **Info Struktur der KERB \_ Smartcard- \_ CSP \_** enthält Informationen zu einem Smartcard- [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP).

Diese Struktur ist nicht in einem öffentlichen Header deklariert.

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

**dwcspinfolen**
</dt> <dd>

Die Größe der-Struktur in Bytes, einschließlich angefügter Daten.

</dd> <dt>

**MessageType**
</dt> <dd>

Der Typ der Nachricht, die übermittelt wird. Dieser Member muss auf 1 festgelegt werden.

</dd> <dt>

**ContextInformation**
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

Der private Schlüssel, der aus dem Schlüssel Container verwendet werden soll, der im Puffer- **BBuffer** angegeben ist. Der Schlüssel kann einer der folgenden Werte sein, die in Wincrypt. h definiert sind.



| Wert                                                                                                                                                                                                                   | Bedeutung                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**Um \_ Keyexchange**</dt> <dt>1</dt> </dl> | Der Schlüssel ist ein Schlüsselaustausch Schlüssel.<br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**Um \_ Signatur**</dt> <dt>2</dt> </dl>       | Der Schlüssel ist ein Signatur Schlüssel.<br/>    |



 

</dd> <dt>

**ncardnameoffset**
</dt> <dd>

Die Anzahl der Zeichen im **BBuffer** -Puffer, die dem Namen der Smartcard in diesem Puffer vorangestellt sind.

> [!IMPORTANT]
> Wenn der Name der Smartcard nicht angegeben wird, muss der Puffer eine leere Zeichenfolge enthalten.

 

</dd> <dt>

**nreadernameoffset**
</dt> <dd>

Die Anzahl der Zeichen im **BBuffer** -Puffer, die dem Namen des smartcardreaders in diesem Puffer vorangestellt sind.

> [!IMPORTANT]
> Wenn der Name des smartcardreaders nicht angegeben wird, muss der Puffer eine leere Zeichenfolge enthalten.

 

</dd> <dt>

**ncontainernameoffset**
</dt> <dd>

Die Anzahl der Zeichen im **BBuffer** -Puffer, die dem Namen des Schlüssel Containers in diesem Puffer vorangestellt sind. Diese Zeichenfolge darf nicht leer sein.

</dd> <dt>

**ncspnameoffset**
</dt> <dd>

Die Anzahl der Zeichen im **BBuffer** -Puffer, die dem Namen des CSP in diesem Puffer vorangestellt sind.

</dd> <dt>

**BBuffer**
</dt> <dd>

Ein Array von Zeichen, die auf eine Länge von initialisiert werden `sizeof(DWORD)` . Dieser Puffer enthält die Namen, auf die durch die Member **ncardnameoffset**, **nreadernameoffset**, **ncontainernameoffset** und **ncspnameoffset** verwiesen wird, sowie alle zusätzlichen Daten, die vom CSP bereitgestellt werden.

Alle Namen, die nicht bereitgestellt werden, müssen in diesem Puffer durch leere Zeichen folgen dargestellt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn diese Struktur serialisiert wird, müssen die Strukturmember an Grenzen ausgerichtet werden, die ein Vielfaches von 2 Bytes sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**KERB \_ Zertifikat \_ Anmeldung**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
