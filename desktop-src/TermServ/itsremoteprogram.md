---
title: ITSRemoteProgram-Schnittstelle
description: Enthält Methoden zum Festlegen und Abrufen des RemoteApp-Modus und der Startparameter für ein RemoteApp-Programm, z. B. den Pfad der ausführbaren Datei und des Arbeitsverzeichnisses.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- ITSRemoteProgram-Schnittstelle Remotedesktopdienste
- ITSRemoteProgram-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b719771f265347da59ce4d8c5990a5b9dc5a72315780def0fd3a34b108e18169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756809"
---
# <a name="itsremoteprogram-interface"></a>ITSRemoteProgram-Schnittstelle

Enthält Methoden zum Festlegen und Abrufen des RemoteApp-Modus und der Startparameter für ein RemoteApp-Programm, z. B. den Pfad der ausführbaren Datei und des Arbeitsverzeichnisses.

## <a name="members"></a>Member

Die **ITSRemoteProgram-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITSRemoteProgram** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ITSRemoteProgram-Schnittstelle** verfügt über diese Methoden.



| Methode                                                            | Beschreibung                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**ServerStartProgram**](itsremoteprogram-serverstartprogram.md) | Gibt ein RemoteApp-Programm an, das in der Remotesitzung gestartet werden soll.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ITSRemoteProgram-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                   | Zugriffstyp           | Beschreibung                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [**RemoteProgramMode**](itsremoteprogram-remoteprogrammode.md)<br/> | Lesen/Schreiben<br/> | Der RemoteApp-Modus.<br/> |



 

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

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

