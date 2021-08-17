---
description: Legt den Sicherheitsdeskriptor fest, der der DDE-Freigabe zugeordnet ist.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: NDdeSetShareSecurity-Funktion (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 00e6d8c4b235e8f7d02ba22e737fc4de9bf4a739864afb1464e6f84c620faa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481824"
---
# <a name="nddesetsharesecurity-function"></a>NDdeSetShareSecurity-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NICHT \_ IMPLEMENTIERT zurück.\]

Legt den Sicherheitsdeskriptor fest, der der DDE-Freigabe zugeordnet ist. Dies erfolgt in der Regel nach dem Bearbeiten der DACL, die der DDE-Freigabe zugewiesen ist.

## <a name="syntax"></a>Syntax


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszServer* \[ In\]
</dt> <dd>

Der Name des Servers, dessen DSDM geändert werden soll.

</dd> <dt>

*lpszShareName* \[ In\]
</dt> <dd>

Der Name der Freigabe, deren Sicherheitsbeschreibung geändert werden soll. Dieser Parameter darf nicht **NULL sein.**

</dd> <dt>

*si* \[ In\]
</dt> <dd>

Ein [**SECURITY \_ INFORMATION-Wert,**](/windows/desktop/SecAuthZ/security-information) der die abzurufenden Sicherheitsinformationen identifiziert.

</dd> <dt>

*pSD* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**SECURITY \_ DESCRIPTOR-Struktur,**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) die Sicherheitsinformationen enthält. Dieser Parameter darf nicht **NULL sein** und sollte auf einen gültigen Sicherheitsdeskriptor verweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NDDE \_ NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch Aufrufen von [**NDdeGetErrorString**](nddegeterrorstring.md)in eine Textfehlermeldung übersetzt werden kann.

## <a name="remarks"></a>Hinweise

Um den [**\_ SICHERHEITS-DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) zu ändern, der einer DDE-Freigabe im DSDM zugeordnet ist, muss der Benutzer über entsprechende Berechtigungen verfügen. Der Freigabeersteller verfügt über diese Berechtigung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeSetShareSecurityW** (Unicode) und **NDdeSetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht dynamische Daten Exchange Netzwerksicherheit](network-dynamic-data-exchange.md)
</dt> <dt>

[DDE-Netzwerkfunktionen](network-dde-functions.md)
</dt> <dt>

[**\_SICHERHEITSINFORMATIONEN**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeGetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 

