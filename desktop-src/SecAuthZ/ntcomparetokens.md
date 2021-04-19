---
description: Vergleicht zwei Zugriffs Token und bestimmt, ob Sie hinsichtlich eines Aufrufens der AccessCheck-Funktion äquivalent sind.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Ntcomparetokens-Funktion (ntabapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362410"
---
# <a name="ntcomparetokens-function"></a>Ntcomparetokens-Funktion

Die **ntcomparetokens** -Funktion vergleicht zwei [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) und bestimmt, ob Sie hinsichtlich eines Aufrufens der [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) -Funktion äquivalent sind.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Firsttokenhandle* \[ in\]
</dt> <dd>

Ein Handle für das erste zu vergleichende Zugriffs Token. Das Token muss für den **\_ tokenabfragezugriff** geöffnet sein.

</dd> <dt>

*Secondtokenhandle* \[ in\]
</dt> <dd>

Ein Handle für das zweite zu vergleichende Zugriffs Token. Das Token muss für den **\_ tokenabfragezugriff** geöffnet sein.

</dd> <dt>

*Gleich* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Wert empfängt, der angibt, ob die von den Parametern *firsttokenhandle* und *secondtokenhandle* dargestellten Token gleichwertig sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion Status \_ Erfolg zurück.

Wenn die Funktion fehlschlägt, wird ein **NTSTATUS** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Zwei Zugriffs Steuerungs Token werden als äquivalent betrachtet, wenn alle der folgenden Bedingungen zutreffen:

-   Jede [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID), die in einem der beiden Token vorhanden ist, ist auch im anderen Token vorhanden.
-   Keines oder beide Token sind beschränkt.
-   Wenn beide Token eingeschränkt sind, wird jede sid, die in einem Token eingeschränkt ist, auch im anderen Token eingeschränkt.
-   Alle in beiden Token vorhandenen Berechtigungen sind ebenfalls im anderen Token vorhanden.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NT*-API. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

