---
description: Gewährt dem angegebenen Status "DDE-Freigabe vertrauenswürdig" im Kontext des aktuellen Benutzers.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: Ndabsettrustedshare-Funktion (ndbeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524953"
---
# <a name="nddesettrustedshare-function"></a>Ndabsettrustedshare-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Gewährt der angegebenen DDE-Freigabe den vertrauenswürdigen Status im Kontext des aktuellen Benutzers.

## <a name="syntax"></a>Syntax


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
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

Der Name der Freigabe, der der vertrauenswürdige Status zugewiesen werden soll. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*dwtrustoptions* \[ in\]
</dt> <dd>

Die Optionen, die sich auf den vertrauenswürdigen Status der DDE-Freigabe auswirken. Dieser Parameter kann einen der folgenden Werte annehmen.



| Option                                                                                                                                                                                                                                                      | Bedeutung                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**Ndde \_ Cmd \_ Show \_ Mask**</dt> <dt>0x0000ffffl</dt> </dl>             | Maske, die zum Abrufen des Werts verwendet wird, mit dem der Status der DDE-Freigabe angezeigt wird, wenn ndde \_ Trust \_ cmd \_ Show festgelegt ist.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**Ndde \_ Trust \_ cmd \_ Show**</dt> <dt>0x10000000l</dt> </dl>          | Überschreiben Sie den Anzeige Zustand, der in der DDE-Freigabe DSDM angegeben ist.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**Ndde \_ Trust- \_ Freigabe \_ del**</dt> <dt>0x20000000l</dt> </dl>       | Entfernen Sie den vertrauenswürdigen Status der Freigabe.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**Ndde \_ Vertrauens \_ Freigabe \_ Init**</dt> <dt>0x40000000l</dt> </dl>    | Ermöglicht einem Client das Initiieren der Anwendung, wenn Sie bereits im Kontext des Benutzers ausgeführt wird.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**Ndde \_ Vertrauens \_ Freigabe \_ Start**</dt> <dt>0x80000000l</dt> </dl> | Ermöglicht das Starten der Anwendung im Kontext des Benutzers.<br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.

## <a name="remarks"></a>Bemerkungen

Die DDE-Freigabe muss zunächst mit [**ndabshareadd**](nddeshareadd.md)erstellt werden.

Wenn **nddesettrustedshare** aufgerufen wird und *dwtrustoptions* auf NULL festgelegt ist, verliert die vertrauenswürdige Freigabe ihren vertrauenswürdigen Status.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Ndabsettrustedsharew** (Unicode) und **ndabsettrustedsharea** (ANSI)<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**Ndabshareadd**](nddeshareadd.md)
</dt> </dl>

 

 




