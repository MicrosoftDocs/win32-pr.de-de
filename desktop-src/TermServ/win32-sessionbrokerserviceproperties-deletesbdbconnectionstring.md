---
title: Delta Type bdbconnectionstring-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Löscht DB-Verbindungs Zeichenfolgen (primär oder sekundär) aus der Registrierung.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Delta Type bdbconnectionstring-Methode Remotedesktopdienste
- Delta Type bdbconnectionstring-Methode Remotedesktopdienste, Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, Delta Timeout-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340585"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Delta Type bdbconnectionstring-Methode der Win32 \_ sessionbrokerserviceproperties-Klasse

Löscht DB-Verbindungs Zeichenfolgen (primär oder sekundär) aus der Registrierung.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Issecondaryconfig-Zeichenfolge* \[ in\]
</dt> <dd>

**True** gibt an, dass die sekundäre Verbindungs Zeichenfolge entfernt wird. **False** gibt an, dass die primäre Verbindungs Zeichenfolge entfernt wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                         |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ sessionbrokerserviceproperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





