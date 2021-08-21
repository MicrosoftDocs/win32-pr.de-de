---
title: IsDbReachable-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Überprüft, ob die Datenbank erreichbar ist.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- IsDbReachable-Methode Remotedesktopdienste
- IsDbReachable-Methode Remotedesktopdienste , Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste , IsDbReachable-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1cd7aaf2035251c503d85683f9aa9e9fe7b7f6285084a97133f0573ba41d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848417"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a>IsDbReachable-Methode der Win32 \_ SessionBrokerServiceProperties-Klasse

Überprüft, ob die Datenbank erreichbar ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*connStringToDb* \[ In\]
</dt> <dd>

Die Verbindungszeichenfolge für die Datenbank.

</dd> <dt>

*connSecondaryStringToDb* \[ In\]
</dt> <dd>

Sekundäre Verbindungszeichenfolge zur zentralen Datenbank.

**Windows Server 2012 R2 und Windows Server 2012:** Dieser Parameter ist vor Windows Server 2016 nicht verfügbar.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





