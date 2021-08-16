---
description: Vergleicht zwei Zugriffstoken und bestimmt, ob sie in Bezug auf einen Aufruf der AccessCheck-Funktion äquivalent sind.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: NtCompareTokens-Funktion (Ntseapi.h)
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
ms.openlocfilehash: a763f6f4238632c3bcc736ebacbd2ff133b1955da673a0397ba9a95ebb87c2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780562"
---
# <a name="ntcomparetokens-function"></a>NtCompareTokens-Funktion

Die **NtCompareTokens-Funktion** vergleicht zwei [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly) und bestimmt, ob sie in Bezug auf einen Aufruf der [**AccessCheck-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) äquivalent sind.

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

*FirstTokenHandle* \[ In\]
</dt> <dd>

Ein Handle für das erste zu vergleichende Zugriffstoken. Das Token muss für den **TOKEN \_ QUERY-Zugriff** geöffnet sein.

</dd> <dt>

*SecondTokenHandle* \[ In\]
</dt> <dd>

Ein Handle für das zweite zu vergleichende Zugriffstoken. Das Token muss für den **TOKEN \_ QUERY-Zugriff** geöffnet sein.

</dd> <dt>

*Gleich* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Wert empfängt, der angibt, ob die durch die Parameter *FirstTokenHandle* und *SecondTokenHandle dargestellten* Token gleichwertig sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion STATUS \_ SUCCESS zurück.

Wenn die Funktion fehlschlägt, wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Zwei Zugriffssteuerungstoken gelten als gleichwertig, wenn alle der folgenden Bedingungen zutreffen:

-   Jede [*Sicherheits-ID*](/windows/desktop/SecGloss/s-gly) (SID), die in beiden Token vorhanden ist, ist auch im anderen Token vorhanden.
-   Weder noch beide Token sind eingeschränkt.
-   Wenn beide Token eingeschränkt sind, wird jede SID, die in einem Token eingeschränkt ist, auch im anderen Token eingeschränkt.
-   Jede Berechtigung, die in beiden Token vorhanden ist, ist auch im anderen Token vorhanden.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Ntseapi.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

