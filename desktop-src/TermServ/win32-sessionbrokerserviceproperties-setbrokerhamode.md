---
title: Setbrokerhamode-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Migriert Daten aus einer lokalen wid-Datenbank in die neue SQL Server-basierte Datenbank. Außerdem wird der Broker Server für die Verwendung des zentralen SQL Server konfiguriert.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Setbrokerhamode-Methode Remotedesktopdienste
- Setbrokerhamode-Methode Remotedesktopdienste, Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, setbrokerhamode-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103671"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Setbrokerhamode-Methode der Win32- \_ Klasse "sessionbrokerserviceproperties"

Migriert Daten aus einer lokalen wid-Datenbank in die neue SQL Server-basierte Datenbank. Außerdem wird der Broker Server für die Verwendung des zentralen SQL Server konfiguriert.

## <a name="syntax"></a>Syntax


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

"Verbindungs Dienst" für " *recentraldbrdcms* \[ " in\]
</dt> <dd>

Verbindungs Zeichenfolge zur zentralen Datenbank.

</dd> <dt>

*secondaryverbindungs-"stringrecentraldbrdcms* \[ " in\]
</dt> <dd>

Sekundäre Verbindungs Zeichenfolge zur zentralen Datenbank.

**Windows Server 2012 R2 und Windows Server 2012:** Dieser Parameter ist vor Windows Server 2016 nicht verfügbar.

</dd> <dt>

*brokerdnsrrname* \[ in\]
</dt> <dd>

DNS-Broker Name.

</dd> <dt>

*activebrokername* \[ in\]
</dt> <dd>

Name des aktiven Brokers.

**Windows Server 2012 R2 und Windows Server 2012:** Dieser Parameter ist vor Windows Server 2016 nicht verfügbar.

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

 

 





