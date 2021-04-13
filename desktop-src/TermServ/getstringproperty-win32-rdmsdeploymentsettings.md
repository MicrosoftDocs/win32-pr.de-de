---
title: GetStringProperty-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- GetStringProperty-Methode Remotedesktopdienste
- GetStringProperty-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, GetStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391746"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a>GetStringProperty-Methode der Win32 \_ rdmsdeploymentsettings-Klasse

Ruft eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Der Alias für die Sammlung virtueller Desktops.

</dd> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Eine Zeichenfolge, die den abgerufenen Wert empfängt.

</dd> </dl>

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

[**Win32 \_ rdmsdeploymentsettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





