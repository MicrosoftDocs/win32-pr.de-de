---
title: Session. identifigingmethode (WSManDisp. h)
description: Fragt einen Remote Computer ab, um zu bestimmen, ob das WS-Management Protokoll unterstützt wird.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Methoden Windows-Remoteverwaltung identifizieren
- Methoden Windows-Remoteverwaltung identifizieren, Sitzungs Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, identifizmethode
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342874"
---
# <a name="sessionidentify-method"></a>Session. identifizmethode

Die **Session. identifigingmethode** fragt einen Remote Computer ab, um zu bestimmen, ob das WS-Management Protokoll unterstützt wird. Weitere Informationen finden Sie [unter erkennen, ob ein Remote Computer WS-Management Protokoll unterstützt](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).

## <a name="syntax"></a>Syntax


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Um die Anforderung im authentifizierten Modus zu senden, verwenden Sie die Authentifizierungs Konstante aus der **wsmansessionflags** -Enumeration. Verwenden Sie zum Senden im nicht authentifizierten Modus **wsmanflagusenoauthentication**. Weitere Informationen finden Sie unter [**Authentifizierungs Konstanten**](authentication-constants.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine XML-Zeichenfolge, die die WS-Management Protokollversion, den Hersteller des Betriebssystems und, wenn die Anforderung authentifiziert wurde, die Betriebssystemversion angibt.

## <a name="remarks"></a>Bemerkungen

**Session. Identifizierung** basiert auf dem [WS-Management-Protokoll](ws-management-protocol.md) Vorgang, der als wsmanidentity definiert ist. Dies wird im SOAP-Paket wie folgt angegeben:


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a>Beispiele

Das folgende VBScript-Beispiel sendet eine nicht authentifizierte Identifizierungs Anforderung an den Remote Computer mit dem Namen Remote in derselben Domäne.


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzung**](session.md)
</dt> <dt>

[**Iwsmansession:: Identifizierung**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[WS-Verwaltungsprotokoll](ws-management-protocol.md)
</dt> </dl>

 

 





