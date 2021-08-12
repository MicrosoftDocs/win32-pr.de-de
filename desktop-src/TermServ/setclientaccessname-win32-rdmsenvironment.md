---
title: SetClientAccessName-Methode der Win32_RDMSEnvironment-Klasse
description: Aktualisiert den Namen des Domain Name System (DNS)-Ressourceneintrags (RR) einer RDMS-Umgebung (Remotedesktop Management Services).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- SetClientAccessName-Methode Remotedesktopdienste
- SetClientAccessName-Methode Remotedesktopdienste , Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment Klasse Remotedesktopdienste , SetClientAccessName-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbb962a6dd1600ad0cd439f7f34772f69d91b925308e2247e1283575d8f68cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604872"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>SetClientAccessName-Methode der Win32 \_ RDMSEnvironment-Klasse

Aktualisiert den Namen des Domain Name System (DNS)-Ressourceneintrags (RR) einer RDMS-Umgebung (Remotedesktop Management Services).

## <a name="syntax"></a>Syntax


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ClientAccessName* \[ In\]
</dt> <dd>

Der neue RR-Name.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSUmgebung**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





