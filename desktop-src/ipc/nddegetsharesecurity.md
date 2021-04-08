---
description: Ruft die Sicherheits Beschreibung ab, die der DDE-Freigabe zugeordnet ist. Dies erfolgt in der Regel zur Bearbeitung.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Nddebug-sharesecurity-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868352"
---
# <a name="nddegetsharesecurity-function"></a>Ndde GetShareSecurity-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Ruft die Sicherheits Beschreibung ab, die der DDE-Freigabe zugeordnet ist. Dies erfolgt in der Regel zur Bearbeitung.

## <a name="syntax"></a>Syntax


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszserver* \[ in\]
</dt> <dd>

Der Name des Servers, auf dem sich die DSDM befindet.

</dd> <dt>

*lpszsharename* \[ in\]
</dt> <dd>

Der Name der Freigabe, deren Sicherheits Beschreibung von der DSDM abgerufen werden soll. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*Si* \[ in\]
</dt> <dd>

Ein [**Sicherheits \_ Informations**](/windows/desktop/SecAuthZ/security-information) Wert, der die Sicherheitsinformationen angibt, die aus der Sicherheits Beschreibung abgerufen werden sollen, die der Freigabe zugeordnet ist.

</dd> <dt>

*pSD* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die die selbst relative Sicherheits Beschreibung empfängt. Dieser Parameter kann **NULL** sein. Wenn dieser Parameter **null** ist, bestimmt die DSDM die Größe der angeforderten Sicherheitsinformationen und gibt die Anzahl der Bytes zurück, die im *lpcbsdrequired* -Parameter benötigt werden, sowie den \_ zu kleinen ndde buf- \_ \_ Fehlercode.

</dd> <dt>

*cbsd* \[ in\]
</dt> <dd>

Die Größe des *pSD* -Puffers. Dieser Parameter muss NULL sein, wenn das *pSD* **null** ist.

</dd> <dt>

*lpcbsdrequired* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Variable, die die tatsächliche Größe der abgerufenen Sicherheits Beschreibung empfängt. Dieser Parameter darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann. Wenn der *pSD* -Parameter **null** war, wird ndde \_ buf \_ zu \_ klein zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Nddebug-sharesecurityw** (Unicode) und **nddebug** -Freigabe (ANSI)<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**Sicherheits \_ Informationen**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**Ndde setsharesecurity**](nddesetsharesecurity.md)
</dt> </dl>

 

