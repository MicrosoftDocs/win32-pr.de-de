---
title: IMsTscAxEvents OnRemoteProgramResult-Methode
description: Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Clientsteuerprogramm zurückgibt.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- OnRemoteProgramResult-Remotedesktopdienste
- OnRemoteProgramResult-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnRemoteProgramResult-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807fbd49cc6222925f34a7e7c007fef54cbc9a3db2566f024ebc0188e9c95113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129662"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a>IMsTscAxEvents::OnRemoteProgramResult-Methode

Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Clientsteuerprogramm zurückgibt.

## <a name="syntax"></a>Syntax


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrRemoteProgram* \[ In\]
</dt> <dd>

Der Name des RemoteApp-Programms.

</dd> <dt>

*lError* \[ In\]
</dt> <dd>

Das Ergebnis des Versuchs, das RemoteApp-Programm zu starten.

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))


</dt> <dd>

Das RemoteApp-Programm wurde erfolgreich gestartet.

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))


</dt> <dd>

Die Remotesitzung ist gesperrt, und das RemoteApp-Programm kann nicht gestartet werden. Der Benutzer muss seine Anmeldeinformationen eingeben, um die Sitzung zu entsperren, und dann das RemoteApp-Programm starten.

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))


</dt> <dd>

Das RemoteApp-Programm hat einen Protokollfehler zurückgegeben.

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))


</dt> <dd>

Das RemoteApp-Programm ist nicht in der genehmigten Liste des RD-Sitzungshost enthalten.

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))


</dt> <dd>

Der Netzwerkpfad zum RemoteApp-Programm wurde verweigert.

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))


</dt> <dd>

Die RemoteApp-Programmdatei wurde nicht gefunden.

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))


</dt> <dd>

Das RemoteApp-Programm konnte nicht gestartet werden.

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))


</dt> <dd>

Das RemoteApp-Programm kann nicht gestartet werden, da die Sitzung derzeit den sicheren Desktop zeigt.

</dd> </dl> </dd> <dt>

*vbIsExecutable* \[ In\]
</dt> <dd>

Gibt an, ob das RemoteApp-Programm direkt, mit dem Namen der ausführbaren Datei oder indirekt mithilfe einer Dateiassoz gestartet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Implementieren Sie diese Methode in Ihrer Ereignissenke, um eine Benachrichtigung zu erhalten, dass ein RemoteApp-Programm ein Ergebnis zurückgegeben hat.

Diese Methode wird unmittelbar nach dem Versuch ActiveX RemoteApp aufgerufen, das RemoteApp-Programm zu starten, und der *lError-Parameter* gibt das Ergebnis des Versuchten an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





