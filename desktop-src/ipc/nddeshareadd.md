---
description: Erstellt eine neue DDE-Freigabe und fügt sie dem DDE-Freigabedatenbank-Manager (DSDM) hinzu.
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: NDdeShareAdd-Funktion (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 0a02381fad8412c7ada0c337c21e633ffa6793887a720ec504f1dfa3d78d9ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602140"
---
# <a name="nddeshareadd-function"></a>NDdeShareAdd-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NOT \_ IMPLEMENTED zurück.\]

Erstellt eine neue DDE-Freigabe und fügt sie dem DDE-Freigabedatenbank-Manager (DSDM) hinzu.

## <a name="syntax"></a>Syntax


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszServer* \[ In\]
</dt> <dd>

Der Name des Servers, dessen DSDM geändert werden soll.

</dd> <dt>

*nLevel* \[ In\]
</dt> <dd>

Die Informationsebene. Dieser Parameter muss 2 sein.

</dd> <dt>

*pSD* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**SECURITY \_ DESCRIPTOR-Struktur,**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) die dieser Freigabe zugeordnet werden soll und für die Zugriffsüberprüfungen bei nachfolgenden Initiierten dieser Freigabe ausgeführt werden. Dieser Parameter kann **NULL** sein. In diesem Fall erstellt das DSDM einen Standardsicherheitsdeskriptor, der dem Besitzer "Vollsteuerung" und "Lesen und Verknüpfen" für alle Benutzer gewährt.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Ein Zeiger auf die [**NDDESHAREINFO-Struktur,**](nddeshareinfo-str.md) die die ApplicationTopic-Liste definiert, die der erstellten DDE-Freigabe sowie anderen Parametern zugeordnet ist. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*cBufSize* \[ In\]
</dt> <dd>

Die Größe der *lpBuffer-Struktur* in Bytes. Dieser Parameter darf nicht 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert NDDE \_ NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch Aufrufen von [**NDdeGetErrorString**](nddegeterrorstring.md)in eine Textfehlermeldung übersetzt werden kann.

## <a name="remarks"></a>Hinweise

Bevor ein Client eine Verbindung mit der DDE-Freigabe herstellen kann, muss er mit [**NDdeSetTrustedShare als vertrauenswürdig**](nddesettrustedshare.md)eingestuft werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeShareAddW** (Unicode) und **NDdeShareAddA** (ANSI)<br/>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Network dynamische Daten Exchange Overview (Übersicht über Netzwerk-dynamische Daten Exchange)](network-dynamic-data-exchange.md)
</dt> <dt>

[Netzwerk-DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

