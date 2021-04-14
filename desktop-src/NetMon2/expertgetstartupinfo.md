---
description: Die Funktion "expertgetstartupinfo" Ruft die Start Konfigurationsinformationen für den Experten ab.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Expertgetstartupinfo-Funktion (Netmon. h)
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
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393414"
---
# <a name="expertgetstartupinfo-function"></a>Expertgetstartupinfo-Funktion

Die Funktion " **expertgetstartupinfo** " Ruft die Start Konfigurationsinformationen für den Experten ab.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexpertkey* \[ in\]
</dt> <dd>

Eindeutige expertenkennung. Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.

</dd> <dt>

*pexpertstartupinfo* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine " [expertstartupinfo](expertstartupinfo.md) "-Struktur, die Startinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert nmerr.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **expertgetstartupinfo** " wird verwendet, wenn der Experte die verwendeten Startinformationen bestimmen muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




