---
title: ITSRemoteProgram-ServerStartProgram-Methode
description: Gibt ein RemoteApp-Programm an, das in der Remotesitzung gestartet werden soll.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- ServerStartProgram-Remotedesktopdienste
- ServerStartProgram-Methode Remotedesktopdienste , ITSRemoteProgram-Schnittstelle
- ITSRemoteProgram-Schnittstelle Remotedesktopdienste , ServerStartProgram-Methode
- ServerStartProgram-Remotedesktopdienste , ITSRemoteProgram2-Schnittstelle
- ITSRemoteProgram2-Schnittstelle Remotedesktopdienste , ServerStartProgram-Methode
- ServerStartProgram-Methode Remotedesktopdienste , ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3-Schnittstelle Remotedesktopdienste , ServerStartProgram-Methode
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
ms.openlocfilehash: c789a9963086128e93546415247cfb3db69afe59c67a445b851ee5cf3687d16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756856"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>ITSRemoteProgram::ServerStartProgram-Methode

Gibt ein RemoteApp-Programm an, das in der Remotesitzung gestartet werden soll. Diese Funktion muss in einer verbundenen Sitzung aufgerufen werden (nachdem die sitzungs verbundene Benachrichtigung auf dem Client empfangen wurde). Eine beliebige Anzahl von RemoteApp-Programmen kann in einer Sitzung gestartet werden. Bei einer RemoteApp-Sitzung kommt es zu einem Time out, wenn in der Sitzung kein RemoteApp-Programm innerhalb des Time outlimits gestartet wird, das zwei Minuten für Windows Server 2008 beträgt.

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

*bstrExecutablePath* \[ In\]
</dt> <dd>

Der Pfad der ausführbaren RemoteApp-Programmdatei auf dem Server.

</dd> <dt>

*bstrFilePath* \[ In\]
</dt> <dd>

Der Pfad einer Datei, die über eine Dateiassoz auf dem Server geöffnet werden soll, z. B. "C: \\ \\ Dokumente \\ \\MyReport.docx". Wenn Sie *bstrFilePath angeben,* sollten Sie nicht den *Parameter bstrExecutablePath* und umgekehrt angeben. Sie sollten nur einen der Parameter angeben.

</dd> <dt>

*bstrWorkingDirectory* \[ In\]
</dt> <dd>

Das Arbeitsverzeichnis auf dem Server für das RemoteApp-Programm.

</dd> <dt>

*vbExpandEnvVarInWorkingDirectoryOnServer* \[ In\]
</dt> <dd>

Gibt an, ob der Server Umgebungsvariablen im Arbeitsverzeichnispfad erweitern soll. Legen Sie diesen Parameter auf **VARIANT \_ TRUE fest,** wenn der Arbeitsverzeichnispfad Umgebungsvariablen enthält, oder **VARIANT \_ FALSE,** wenn der Arbeitsverzeichnispfad keine Umgebungsvariablen enthält.

</dd> <dt>

*bstrArguments* \[ In\]
</dt> <dd>

Die Befehlszeilenargumente für das RemoteApp-Programm, die in *bstrExecutablePath angegeben sind.* Legen Sie dies **auf NULL** fest, *wenn bstrExecutablePath* nicht angegeben ist.

</dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ In\]
</dt> <dd>

Gibt an, ob der Server Umgebungsvariablen in den Befehlszeilenargumenten erweitern soll. Legen Sie diesen Parameter auf **VARIANT \_ TRUE fest,** wenn die Argumente Umgebungsvariablen enthalten, oder **VARIANT \_ FALSE,** wenn die Argumente keine Umgebungsvariablen enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK zurück,** wenn erfolgreich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram ist als FDD029F9-467A-4c49-8529-64B521DBD1B4 definiert.<br/>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





