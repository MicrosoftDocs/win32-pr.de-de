---
title: Setclientaccessname-Methode der Win32_RDMSEnvironment-Klasse
description: Aktualisiert den Namen der Domain Name System (DNS) Resource Record (RR) einer Remotedesktop Verwaltungsdienste-Umgebung (RDMs).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Setclientaccessname-Methode Remotedesktopdienste
- Setclientaccessname-Methode Remotedesktopdienste, Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment-Klasse Remotedesktopdienste, setclientaccessname-Methode
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
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344506"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Setclientaccessname-Methode der Win32- \_ Klasse "rdmsenvironment"

Aktualisiert den Namen der Domain Name System (DNS) Resource Record (RR) einer Remotedesktop Verwaltungsdienste-Umgebung (RDMs).

## <a name="syntax"></a>Syntax


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Clientaccessname* \[ in\]
</dt> <dd>

Der neue RR-Name.

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

 

 





