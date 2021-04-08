---
title: Installbrokerdatabase-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Installiert eine Remote Desktop-Verbindungs Broker-Datenbank auf einem zentralen SQL-Server.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Installbrokerdatabase-Methode Remotedesktopdienste
- Installbrokerdatabase-Methode Remotedesktopdienste, Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, installbrokerdatabase-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740200"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Installbrokerdatabase-Methode der Win32- \_ Klasse "sessionbrokerserviceproperties"

Installiert eine Remote Desktop-Verbindungs Broker-Datenbank auf einem zentralen SQL-Server.

## <a name="syntax"></a>Syntax


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newdbfilepath* \[ in\]
</dt> <dd>

neuer Daten Bank Dateipfad.

</dd> <dt>

"Configuration Manager-Manager"  \[ in\]
</dt> <dd>

Verbindungs Zeichenfolge zum zentralen Daten Bank Master.

</dd> <dt>

*centralrdcmsdbname* \[ in\]
</dt> <dd>

Name der zentralen Datenbank.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ sessionbrokerserviceproperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





