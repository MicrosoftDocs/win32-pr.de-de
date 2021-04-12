---
title: Itsremoteprogram serverstartprogram-Methode
description: Gibt ein RemoteApp-Programm an, das in der Remote Sitzung gestartet werden soll.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Serverstartprogram-Methode Remotedesktopdienste
- Serverstartprogram-Methode Remotedesktopdienste, itsremoteprogram-Schnittstelle
- Itsremoteprogram-Schnittstelle Remotedesktopdienste, serverstartprogram-Methode
- Serverstartprogram-Methode Remotedesktopdienste, ITSRemoteProgram2-Schnittstelle
- ITSRemoteProgram2 Interface Remotedesktopdienste, serverstartprogram-Methode
- Serverstartprogram-Methode Remotedesktopdienste, ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3 Interface Remotedesktopdienste, serverstartprogram-Methode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518044"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>Itsremoteprogram:: serverstartprogram-Methode

Gibt ein RemoteApp-Programm an, das in der Remote Sitzung gestartet werden soll. Diese Funktion muss für eine verbundene Sitzung aufgerufen werden (nachdem die Benachrichtigung über die Sitzungs Verbindung auf dem Client empfangen wurde). Eine beliebige Anzahl von RemoteApp-Programmen kann in einer Sitzung gestartet werden. Bei einer RemoteApp-Sitzung tritt ein Timeout auf, wenn innerhalb der Sitzung innerhalb des Timeout Limits kein RemoteApp-Programm gestartet wird. Dies ist zwei Minuten für Windows Server 2008.

## <a name="syntax"></a>Syntax


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrexecutablepath* \[ in\]
</dt> <dd>

Der Pfad der ausführbaren Datei des RemoteApp-Programms auf dem Server.

</dd> <dt>

*bstraufilepath* \[ in\]
</dt> <dd>

Der Pfad einer Datei, die über eine Datei Zuordnung auf dem Server geöffnet werden soll, z. b. "C: \\ \\ Documents \\ \\MyReport.docx". Wenn Sie *bstraufilepath* angeben, sollten Sie den *bstrexecutablepath* -Parameter nicht angeben und umgekehrt. Sie sollten nur einen der Parameter angeben.

</dd> <dt>

*bstrauworkingdirectory* \[ in\]
</dt> <dd>

Das Arbeitsverzeichnis auf dem Server für das RemoteApp-Programm.

</dd> <dt>

*vbexpandeinvvarinworkingdirector yonserver* \[ in\]
</dt> <dd>

Gibt an, ob der Server Umgebungsvariablen im Pfad des Arbeitsverzeichnisses erweitern soll. Legen Sie diesen Parameter auf **Variant \_ true** fest, wenn der Arbeitsverzeichnis Pfad Umgebungsvariablen enthält, oder **Variant \_ false** , wenn der Arbeitsverzeichnis Pfad keine Umgebungsvariablen enthält.

</dd> <dt>

*bstrauarguments* \[ in\]
</dt> <dd>

Die Befehlszeilenargumente für das RemoteApp-Programm, die in *bstrexecutablepath* angegeben sind. Legen Sie diese Einstellung auf **null** fest, wenn *bstrexecutablepath* nicht angegeben ist.

</dd> <dt>

*vbexpandeinvvarinargumentsonserver* \[ in\]
</dt> <dd>

Gibt an, ob der Server Umgebungsvariablen in den Befehlszeilen Argumenten erweitern soll. Legen Sie diesen Parameter auf **Variant \_ true** fest, wenn die Argumente Umgebungsvariablen enthalten, oder **Variant \_ false** , wenn die Argumente keine Umgebungsvariablen enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ itsremoteprogram ist als FDD029F9-467A-4c49-8529-64B521DBD1B4 definiert.<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**Itsremoteprogram**](itsremoteprogram.md)
</dt> </dl>

 

 





