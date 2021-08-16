---
description: Die ExpertGetStartupInfo-Funktion ruft die Startkonfigurationsinformationen für den Experten ab.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: ExpertGetStartupInfo-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7e4327965dce1c4bca07846a818609e555c16a3a27b0a19204a9971eaf9d642e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366882"
---
# <a name="expertgetstartupinfo-function"></a>ExpertGetStartupInfo-Funktion

Die **ExpertGetStartupInfo-Funktion** ruft die Startkonfigurationsinformationen für den Experten ab.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hExpertKey* \[ In\]
</dt> <dd>

Eindeutiger Expertenbezeichner. Netzwerkmonitor übergibt *hExpertKey* an den Experten, wenn er die [Run-Funktion](run.md) aufruft.

</dd> <dt>

*pExpertStartupInfo* \[ out\]
</dt> <dd>

Zeiger auf eine [EXPERTSTARTUPINFO-Struktur,](expertstartupinfo.md) die Startinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, lautet der Rückgabewert NMERR.

## <a name="remarks"></a>Hinweise

Die **ExpertGetStartupInfo-Funktion** wird verwendet, wenn der Experte die verwendeten Startinformationen bestimmen muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




