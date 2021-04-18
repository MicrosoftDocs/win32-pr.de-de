---
title: Setbrokernonhamode-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Migriert Daten aus Central SQL Server in eine lokale Datenbank. Außerdem wird der Broker Server für die Verwendung der lokalen Datenbank konfiguriert.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Setbrokernonhamode-Methode Remotedesktopdienste
- Setbrokernonhamode-Methode Remotedesktopdienste, Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, setbrokernonhamode-Methode
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
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345292"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Setbrokernonhamode-Methode der Win32 \_ sessionbrokerserviceproperties-Klasse

Migriert Daten aus Central SQL Server in eine lokale Datenbank. Außerdem wird der Broker Server für die Verwendung der lokalen Datenbank konfiguriert.

## <a name="syntax"></a>Syntax


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

"Verbindungs Dienst" für " *recentraldbrdcms* \[ " in\]
</dt> <dd>

Verbindungs Zeichenfolge zur zentralen Datenbank.

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

 

 





