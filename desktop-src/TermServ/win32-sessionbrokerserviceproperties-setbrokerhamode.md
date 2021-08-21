---
title: SetBrokerHAMode-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Migriert Daten aus einer lokalen WID-Datenbank zur neuen SQL serverbasierten Datenbank. Außerdem wird der Brokerserver für die Verwendung des zentralen SQL-Servers konfiguriert.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- SetBrokerHAMode-Methode Remotedesktopdienste
- SetBrokerHAMode-Methode Remotedesktopdienste , Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties Klasse Remotedesktopdienste , SetBrokerHAMode-Methode
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
ms.openlocfilehash: 17b72233b51686911e4b1d0a661f4e46fa9bcaa813bb6ccc973b2f8a5b12da24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604549"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>SetBrokerHAMode-Methode der Win32 \_ SessionBrokerServiceProperties-Klasse

Migriert Daten aus einer lokalen WID-Datenbank zur neuen SQL serverbasierten Datenbank. Außerdem wird der Brokerserver für die Verwendung des zentralen SQL-Servers konfiguriert.

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

*connStringToCentralDBRdcms* \[ In\]
</dt> <dd>

Verbindungszeichenfolge zur zentralen Datenbank.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ In\]
</dt> <dd>

Sekundäre Verbindungszeichenfolge zur zentralen Datenbank.

**Windows Server 2012 R2 und Windows Server 2012:** Dieser Parameter ist vor Windows Server 2016 nicht verfügbar.

</dd> <dt>

*brokerDnsRRName* \[ In\]
</dt> <dd>

Broker-DNS-Name.

</dd> <dt>

*activeBrokerName* \[ In\]
</dt> <dd>

Aktiver Brokername.

**Windows Server 2012 R2 und Windows Server 2012:** Dieser Parameter ist vor Windows Server 2016 nicht verfügbar.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





