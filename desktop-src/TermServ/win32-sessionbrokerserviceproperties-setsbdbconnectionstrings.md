---
title: SetSBDbConnectionStrings-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Speichert Datenbankverbindungszeichenfolgen sowohl primär als auch sekundär in der Registrierung.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- SetSBDbConnectionStrings-Methode Remotedesktopdienste
- SetSBDbConnectionStrings-Methode Remotedesktopdienste , Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste , SetSBDbConnectionStrings-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89baa40d25e6ecf316ac6904cc89091fa581d87be1018c52fa31c2b7ab358d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058417"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a>SetSBDbConnectionStrings-Methode der Win32 \_ SessionBrokerServiceProperties-Klasse

Speichert Datenbankverbindungszeichenfolgen sowohl primär als auch sekundär in der Registrierung.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*connStringToCentralDBRdcms* \[ In\]
</dt> <dd>

Die primäre Verbindungszeichenfolge.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ In\]
</dt> <dd>

Die sekundäre Verbindungszeichenfolge.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                         |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





