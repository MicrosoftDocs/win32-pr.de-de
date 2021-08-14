---
description: Ruft die Einer DDE-Freigabe zugeordneten Optionen ab, die in der Liste der Serverbenutzer mit vertrauenswürdigen Freigaben enthalten sind.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: NDdeGetTrustedShare-Funktion (Nddeapi.h)
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
ms.openlocfilehash: 117178118f59c4f8830cab8aee6afc263d169bf58bac5ac81d3e33305b7db9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481930"
---
# <a name="nddegettrustedshare-function"></a>NDdeGetTrustedShare-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NOT \_ IMPLEMENTED zurück.\]

Ruft die Einer DDE-Freigabe zugeordneten Optionen ab, die in der Liste der vertrauenswürdigen Freigaben des Serverbenutzers enthalten sind.

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

*lpszServer* \[ In\]
</dt> <dd>

Der Name des Servers, auf dem sich das DSDM befindet.

</dd> <dt>

*lpszShareName* \[ In\]
</dt> <dd>

Der Freigabename, dessen vertrauenswürdiger Status abgefragt wird. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*lpdwTrustOptions* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Vertrauensoptionen empfängt. Dieser Parameter darf nicht **NULL** sein. Die folgenden Vertrauensstellungsoptionen sind verfügbar.



| Wert                                                                                                                                                                                                                                                       | Bedeutung                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ SHOW \_ MASK**</dt> <dt>0x0000FFFFL</dt> </dl>             | Maske, die verwendet wird, um den Wert abzurufen, der verwendet wird, um den DDE-Freigabe-Showzustand zu überschreiben, wenn NDDE \_ TRUST \_ CMD \_ SHOW festgelegt ist.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ TRUST \_ CMD \_ SHOW**</dt> <dt>0x10000000L</dt> </dl>          | Überschreiben Sie den im DDE-Freigabe-DSDM angegebenen Showzustand.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ TRUST \_ SHARE \_ DEL**</dt> <dt>0x20000000L</dt> </dl>       | Entfernen Sie den vertrauenswürdigen Status der Freigabe.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ TRUST \_ SHARE \_ INIT**</dt> <dt>0x40000000L</dt> </dl>    | Lassen Sie zu, dass ein Client die Anwendung initiiert, wenn sie bereits im Kontext des Benutzers ausgeführt wird.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ TRUST \_ SHARE \_ START**</dt> <dt>0x80000000L</dt> </dl> | Lassen Sie zu, dass die Anwendung im Kontext des Benutzers gestartet wird.<br/>                                                 |



 

</dd> <dt>

*lpdwShareModId0* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den ersten Teil des vertrauenswürdigen Freigabe-Änderungsbezeichners empfängt. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*lpdwShareModId1* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den zweiten Teil des vertrauenswürdigen Freigabe-Änderungsbezeichners empfängt. Dieser Parameter darf nicht **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert NDDE \_ NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch Aufrufen von [**NDdeGetErrorString**](nddegeterrorstring.md)in eine Textfehlermeldung übersetzt werden kann.

## <a name="remarks"></a>Hinweise

Der Änderungsbezeichner der vertrauenswürdigen Freigabe spiegelt die Version der DDE-Freigabe im DSDM zum Zeitpunkt der anfänglichen Gewährung des vertrauenswürdigen Status der DDE-Freigabe wider. Der vertrauenswürdige Freigabe-Änderungsbezeichner wird hauptsächlich verwendet, um veraltete vertrauenswürdige Freigaben zu entfernen. Der Benutzer muss jedoch keine veralteten vertrauenswürdigen Freigaben entfernen. Der Netzwerk-DDE-Agent entfernt veraltete Freigaben im Namen des Benutzers.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeGetTrustedShareW** (Unicode) und **NDdeGetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Network dynamische Daten Exchange Overview (Übersicht über Netzwerk-dynamische Daten Exchange)](network-dynamic-data-exchange.md)
</dt> <dt>

[Netzwerk-DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

 




