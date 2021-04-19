---
description: Legt die Sicherheits Beschreibung fest, die der DDE-Freigabe zugeordnet ist.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Nddebug-sharesecurity-Funktion (nddecoapi. h)
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
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349360"
---
# <a name="nddesetsharesecurity-function"></a>Ndde setsharesecurity-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Legt die Sicherheits Beschreibung fest, die der DDE-Freigabe zugeordnet ist. Dies erfolgt in der Regel nach dem Bearbeiten der der DDE-Freigabe zugewiesenen DACL.

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

*lpszserver* \[ in\]
</dt> <dd>

Der Name des Servers, dessen DSDM geändert werden soll.

</dd> <dt>

*lpszsharename* \[ in\]
</dt> <dd>

Der Name der Freigabe, deren Sicherheits Beschreibung geändert werden soll. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*Si* \[ in\]
</dt> <dd>

Ein [**Sicherheits \_ Informations**](/windows/desktop/SecAuthZ/security-information) Wert, der die abzurufenden Sicherheitsinformationen identifiziert.

</dd> <dt>

*pSD* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die Sicherheitsinformationen enthält. Dieser Parameter darf nicht **null** sein und muss auf eine gültige Sicherheits Beschreibung zeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.

## <a name="remarks"></a>Bemerkungen

Zum Ändern der [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die einer DDE-Freigabe in der DSDM zugeordnet ist, muss der Benutzer über die entsprechenden Berechtigungen verfügen. der Freigabe Ersteller verfügt über diese Berechtigung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Nddebug-sharesecurityw** (Unicode) und **nddebug** (ANSI)<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**Sicherheits \_ Informationen**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**Ndde GetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 

