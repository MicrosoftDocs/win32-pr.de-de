---
title: Itsremoteprogram-Schnittstelle
description: Enthält Methoden zum Festlegen und Abrufen des RemoteApp-Modus und der Startparameter für ein RemoteApp-Programm, z. b. den Pfad der ausführbaren Datei und das Arbeitsverzeichnis.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Itsremoteprogram-Schnittstelle Remotedesktopdienste
- Itsremoteprogram-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040749"
---
# <a name="itsremoteprogram-interface"></a>Itsremoteprogram-Schnittstelle

Enthält Methoden zum Festlegen und Abrufen des RemoteApp-Modus und der Startparameter für ein RemoteApp-Programm, z. b. den Pfad der ausführbaren Datei und das Arbeitsverzeichnis.

## <a name="members"></a>Member

Die **itsremoteprogram** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Itsremoteprogram** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Schnittstelle **itsremoteprogram** verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**Serverstartprogram**](itsremoteprogram-serverstartprogram.md) | Gibt ein RemoteApp-Programm an, das in der Remote Sitzung gestartet werden soll.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die Schnittstelle **itsremoteprogram** verfügt über diese Eigenschaften.



| Eigenschaft                                                                   | Zugriffstyp           | BESCHREIBUNG                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [**Remoteprogrammode**](itsremoteprogram-remoteprogrammode.md)<br/> | Lesen/Schreiben<br/> | Der RemoteApp-Modus.<br/> |



 

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

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

