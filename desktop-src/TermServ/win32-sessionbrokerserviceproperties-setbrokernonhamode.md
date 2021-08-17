---
title: SetBrokerNonHAMode-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Migriert Daten von zentralen SQL Server zu einer lokalen Datenbank. Außerdem wird der Brokerserver für die Verwendung der lokalen Datenbank konfiguriert.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- SetBrokerNonHAMode-Methode Remotedesktopdienste
- SetBrokerNonHAMode-Methode Remotedesktopdienste , Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties Klasse Remotedesktopdienste , SetBrokerNonHAMode-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34daa0817056975a6b15164dd29edcbcc86cd7cd9475f753e91500845ce089a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058409"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>SetBrokerNonHAMode-Methode der Win32 \_ SessionBrokerServiceProperties-Klasse

Migriert Daten von zentralen SQL Server zu einer lokalen Datenbank. Außerdem wird der Brokerserver für die Verwendung der lokalen Datenbank konfiguriert.

## <a name="syntax"></a>Syntax


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*connStringToCentralDBRdcms* \[ In\]
</dt> <dd>

Verbindungszeichenfolge zur zentralen Datenbank.

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

 

 





