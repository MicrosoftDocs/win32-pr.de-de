---
description: Ruft die Optionen ab, die einer DDE-Freigabe in der Liste Server Benutzer vertrauenswürdiger Freigaben zugeordnet sind.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Ndbegettrustedshare-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345469"
---
# <a name="nddegettrustedshare-function"></a>Nddebug Share-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Ruft die einer DDE-Freigabe zugeordneten Optionen ab, die sich in der Liste der vertrauenswürdigen Freigaben des Server Benutzers befinden.

## <a name="syntax"></a>Syntax


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
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

Der Freigabe Name, dessen vertrauenswürdiger Status abgefragt wird. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*lpdwtrustoptions* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Vertrauensstellungs Optionen empfängt. Dieser Parameter darf nicht **null** sein. Die folgenden Vertrauensstellungs Optionen sind verfügbar.



| Wert                                                                                                                                                                                                                                                       | Bedeutung                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**Ndde \_ Cmd \_ Show \_ Mask**</dt> <dt>0x0000ffffl</dt> </dl>             | Maske, die zum Abrufen des Werts verwendet wird, mit dem der Status der DDE-Freigabe angezeigt wird, wenn ndde \_ Trust \_ cmd \_ Show festgelegt ist.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**Ndde \_ Trust \_ cmd \_ Show**</dt> <dt>0x10000000l</dt> </dl>          | Überschreiben Sie den Anzeige Zustand, der in der DDE-Freigabe DSDM angegeben ist.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**Ndde \_ Trust- \_ Freigabe \_ del**</dt> <dt>0x20000000l</dt> </dl>       | Entfernen Sie den vertrauenswürdigen Status der Freigabe.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**Ndde \_ Vertrauens \_ Freigabe \_ Init**</dt> <dt>0x40000000l</dt> </dl>    | Ermöglicht einem Client das Initiieren der Anwendung, wenn Sie bereits im Kontext des Benutzers ausgeführt wird.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**Ndde \_ Vertrauens \_ Freigabe \_ Start**</dt> <dt>0x80000000l</dt> </dl> | Ermöglicht das Starten der Anwendung im Kontext des Benutzers.<br/>                                                 |



 

</dd> <dt>

*lpdwShareModId0* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den ersten Teil des Bezeichner der vertrauenswürdigen Freigabe Änderung empfängt. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*lpdwShareModId1* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den zweiten Teil des Bezeichner der vertrauenswürdigen Freigabe Änderung empfängt. Dieser Parameter darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.

## <a name="remarks"></a>Bemerkungen

Der Bezeichner der vertrauenswürdigen Freigabe Änderung gibt die Version der DDE-Freigabe in der DSDM zum Zeitpunkt an, zu dem die DDE-Freigabe anfänglich den vertrauenswürdigen Status erhalten hat. Der Bezeichner der vertrauenswürdigen Freigabe Änderung wird hauptsächlich zum Entfernen veralteter vertrauenswürdiger Freigaben verwendet Der Benutzer muss jedoch keine veralteten vertrauenswürdigen Freigaben Entfernen. Der Netzwerk-DDE-Agent entfernt veraltete Freigaben im Auftrag des Benutzers.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Nddebug** (Unicode) und **ndde gettrustedsharea** (ANSI)<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**Ndabsettrustedshare**](nddesettrustedshare.md)
</dt> </dl>

 

 




