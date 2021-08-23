---
title: GetActiveServer-Methode der Win32_RDMSEnvironment Klasse
description: Ruft den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) der RDMS-Umgebung (Remotedesktop Management Services) ab.
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- GetActiveServer-Remotedesktopdienste
- GetActiveServer-Methode Remotedesktopdienste , Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment klasse Remotedesktopdienste , GetActiveServer-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730fa1230ddf08f5bd598e2041cd82ab4287d30387fa61460771fea5bcf3ec50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139013"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a>GetActiveServer-Methode der Win32 \_ RDMSEnvironment-Klasse

Ruft den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) der RDMS-Umgebung (Remotedesktop Management Services) ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ServerName* \[ out\]
</dt> <dd>

Empfängt den abgerufenen FQDN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSUmgebung**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





