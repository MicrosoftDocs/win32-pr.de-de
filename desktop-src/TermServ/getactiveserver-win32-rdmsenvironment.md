---
title: Getactiveserver-Methode der Win32_RDMSEnvironment-Klasse
description: Ruft den voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN) der RDMs-Umgebung (Remotedesktop Management Services) ab.
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Getactiveserver-Methode Remotedesktopdienste
- Getactiveserver-Methode Remotedesktopdienste, Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment-Klasse Remotedesktopdienste, getactiveserver-Methode
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
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477457"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Getactiveserver-Methode der Win32 \_ rdmsenvironment-Klasse

Ruft den voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN) der RDMs-Umgebung (Remotedesktop Management Services) ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* \[ vorgenommen\]
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
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdmsenvironment**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





