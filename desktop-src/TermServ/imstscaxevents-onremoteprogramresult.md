---
title: Imstscaxevents onremoteprogramresult-Methode
description: Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Client Steuerelement zurückgibt.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- Onremoteprogramresult-Methode Remotedesktopdienste
- Onremoteprogramresult-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onremoteprogramresult-Methode
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
ms.openlocfilehash: 880e4fb3f6453114415f5bcc07a0afb9c176a1bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104313"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a>Imstscaxevents:: onremoteprogramresult-Methode

Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Client Steuerelement zurückgibt.

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

*bstrauremoteprogram* \[ in\]
</dt> <dd>

Der Name des RemoteApp-Programms.

</dd> <dt>

*lerror* \[ in\]
</dt> <dd>

Das Ergebnis des Versuchs, das RemoteApp-Programm zu starten.

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteappresultok** (0 (0x0))


</dt> <dd>

Das RemoteApp-Programm wurde erfolgreich gestartet.

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteappresultlocked** (1 (0x1))


</dt> <dd>

Die Remote Sitzung ist gesperrt, und das RemoteApp-Programm kann nicht gestartet werden. Der Benutzer muss seine Anmelde Informationen eingeben, um die Sitzung zu entsperren, und dann das RemoteApp-Programm starten.

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteappresultprotocolerror** (2 (0x2))


</dt> <dd>

Das RemoteApp-Programm hat einen Protokollfehler zurückgegeben.

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteappresultnotinwhitelist** (3 (0x3))


</dt> <dd>

Das RemoteApp-Programm ist nicht in der genehmigten Liste der RD-Sitzungshost Server enthalten.

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteappresultnetworkpathdenied** (4 (0x4))


</dt> <dd>

Der Netzwerkpfad zum RemoteApp-Programm wurde verweigert.

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteappresultfilename-found** (5 (0x5))


</dt> <dd>

Die RemoteApp-Programmdatei wurde nicht gefunden.

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteappresultfailure** (6 (0x6))


</dt> <dd>

Das RemoteApp-Programm konnte nicht gestartet werden.

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteappresulthooklotloaded** (7 (0x7))


</dt> <dd>

Das RemoteApp-Programm kann nicht gestartet werden, da die Sitzung aktuell den sicheren Desktop anzeigt.

</dd> </dl> </dd> <dt>

*vbisexecutable* \[ in\]
</dt> <dd>

Gibt an, ob das RemoteApp-Programm direkt mit dem Namen der ausführbaren Datei oder indirekt mithilfe einer Datei Zuordnung gestartet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Implementieren Sie diese Methode in der Ereignis Senke, um Benachrichtigungen zu erhalten, dass ein RemoteApp-Programm ein Ergebnis zurückgegeben hat.

Diese Methode wird unmittelbar nach dem Versuch des ActiveX-Steuer Elements aufgerufen, das RemoteApp-Programm zu starten, und der *lerror* -Parameter gibt das Ergebnis des Versuchs an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





