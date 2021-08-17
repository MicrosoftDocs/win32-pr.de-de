---
title: InstallBrokerDatabase-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Installiert eine RD-Verbindungsbrokerdatenbank auf einem zentralen SQL Server.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- InstallBrokerDatabase-Remotedesktopdienste
- InstallBrokerDatabase-Methode Remotedesktopdienste , Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties klasse Remotedesktopdienste , InstallBrokerDatabase-Methode
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
ms.openlocfilehash: 4e77a34c70fbf06bac5501c8cacddce9feb9211d1fe21c1ef30fe429d3e75308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422450"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>InstallBrokerDatabase-Methode der Win32 \_ SessionBrokerServiceProperties-Klasse

Installiert eine RD-Verbindungsbrokerdatenbank auf einem zentralen SQL Server.

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

*newDbFilePath* \[ In\]
</dt> <dd>

Neuer Datenbankdateipfad.

</dd> <dt>

*connStringToCentralDBMaster* \[ In\]
</dt> <dd>

Verbindungszeichenfolge für den zentralen Datenbankmaster.

</dd> <dt>

*centralRdcmsDbName* \[ In\]
</dt> <dd>

Name der zentralen Datenbank.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





