---
title: SetStringProperty-Methode der Win32_RDMSDeploymentSettings -Klasse (Certenroll.h)
description: Aktualisiert eine Zeichenfolgeneigenschaft für die Bereitstellungseinstellungen einer Sammlung virtueller Desktops.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- SetStringProperty-Remotedesktopdienste
- SetStringProperty-Methode Remotedesktopdienste , Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings klasse Remotedesktopdienste , SetStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1001d5c723642357263a6029c3569eaa861f7dcf3689cc7d06b42e04ef461aa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987500"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a>SetStringProperty-Methode der Win32 \_ RDMSDeploymentSettings-Klasse

Aktualisiert eine Zeichenfolgeneigenschaft für die Bereitstellungseinstellungen einer Sammlung virtueller Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Der Alias für die Sammlung virtueller Desktops.

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Der neue Eigenschaftswert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| Header<br/>                   | <dl> <dt>Certenroll.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





