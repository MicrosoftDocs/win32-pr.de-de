---
description: Erstellt eine neue DDE-Freigabe und fügt Sie dem DDE-Freigabe Datenbank-Manager (DSDM) hinzu.
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Ndenshareadd-Funktion (nddecoapi. h)
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
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352263"
---
# <a name="nddeshareadd-function"></a>Ndde shareadd-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Erstellt eine neue DDE-Freigabe und fügt Sie dem DDE-Freigabe Datenbank-Manager (DSDM) hinzu.

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

*lpszserver* \[ in\]
</dt> <dd>

Der Name des Servers, dessen DSDM geändert werden soll.

</dd> <dt>

*Nlevel* \[ in\]
</dt> <dd>

Die Informationsebene. Dieser Parameter muss 2 sein.

</dd> <dt>

*pSD* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Sicherheits \_ beschreibungstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die dieser Freigabe zugeordnet werden soll, und für die Zugriffs Überprüfungen für nachfolgende initiierte Aktionen dieser Freigabe ausgeführt werden. Dieser Parameter kann **null** sein. in diesem Fall erstellt die DSDM eine Standard Sicherheits Beschreibung, die dem Besitzer "Vollzugriff" gewährt und allen Benutzern "lesen und verknüpfen" ermöglicht.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Ein Zeiger auf die [**nddeshareingefo**](nddeshareinfo-str.md) -Struktur, die die applicationtopic-Liste definiert, die der erstellten DDE-Freigabe und anderen Parametern zugeordnet ist. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*cbubsize* \[ in\]
</dt> <dd>

Die Größe der *lpBuffer* -Struktur in Bytes. Dieser Parameter darf nicht NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.

## <a name="remarks"></a>Bemerkungen

Bevor ein Client eine Verbindung mit der DDE-Freigabe herstellen kann, muss er mit [**ndbesettrustedshare**](nddesettrustedshare.md)als vertrauenswürdig eingestuft werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Ndde shareaddw** (Unicode) und **nddebug**<br/>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**Nddebug-Info**](nddeshareinfo-str.md)
</dt> <dt>

[**Ndabsettrustedshare**](nddesettrustedshare.md)
</dt> </dl>

 

