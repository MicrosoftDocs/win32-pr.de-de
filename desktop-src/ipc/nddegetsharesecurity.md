---
description: Ruft den Sicherheitsdeskriptor ab, der der DDE-Freigabe zugeordnet ist. Dies erfolgt in der Regel für die Bearbeitung.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: NDdeGetShareSecurity-Funktion (Nddeapi.h)
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
ms.openlocfilehash: 101767516e8bd726ebf1a64ad83cfd924b3696a56d810895b4d9a9ed9a1e0ef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829340"
---
# <a name="nddegetsharesecurity-function"></a>NDdeGetShareSecurity-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NICHT \_ IMPLEMENTIERT zurück.\]

Ruft den Sicherheitsdeskriptor ab, der der DDE-Freigabe zugeordnet ist. Dies erfolgt in der Regel für die Bearbeitung.

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

*lpszServer* \[ In\]
</dt> <dd>

Der Name des Servers, auf dem sich das DSDM befindet.

</dd> <dt>

*lpszShareName* \[ In\]
</dt> <dd>

Der Name der Freigabe, deren Sicherheitsbeschreibung aus dem DSDM abgerufen werden soll. Dieser Parameter darf nicht **NULL sein.**

</dd> <dt>

*si* \[ In\]
</dt> <dd>

Ein [**SECURITY \_ INFORMATION-Wert,**](/windows/desktop/SecAuthZ/security-information) der die Sicherheitsinformationen angibt, die aus dem der Freigabe zugeordneten Sicherheitsdeskriptor abgerufen werden sollen.

</dd> <dt>

*pSD* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**SECURITY \_ DESCRIPTOR-Struktur,**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) die den selbst relativen Sicherheitsdeskriptor empfängt. Dieser Parameter kann **NULL** sein. Wenn dieser Parameter **NULL** ist, bestimmt das DSDM die Größe der angeforderten Sicherheitsinformationen und gibt die Anzahl der Bytes zurück, die im *lpcbsdRequired-Parameter* zusammen mit dem NDDE BUF TOO SMALL-Fehlercode benötigt \_ \_ \_ werden.

</dd> <dt>

*cbSD* \[ In\]
</dt> <dd>

Die Größe des *pSD-Puffers.* Dieser Parameter muss 0 (null) sein, *wenn pSD* **NULL ist.**

</dd> <dt>

*lpcbsdRequired* \[ out\]
</dt> <dd>

Ein Zeiger auf die Variable, die die tatsächliche Größe des abgerufenen Sicherheitsdeskriptors empfängt. Dieser Parameter darf nicht **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NDDE \_ NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch Aufrufen von [**NDdeGetErrorString**](nddegeterrorstring.md)in eine Textfehlermeldung übersetzt werden kann. Wenn der *pSD-Parameter* **NULL war,** wird NDDE \_ BUF \_ TOO SMALL \_ zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeGetShareSecurityW** (Unicode) und **NDdeGetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht dynamische Daten Exchange Netzwerksicherheit](network-dynamic-data-exchange.md)
</dt> <dt>

[DDE-Netzwerkfunktionen](network-dde-functions.md)
</dt> <dt>

[**\_SICHERHEITSINFORMATIONEN**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> </dl>

 

