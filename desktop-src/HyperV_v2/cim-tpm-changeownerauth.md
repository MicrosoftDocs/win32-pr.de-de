---
description: Ändert die Autorisierungs Anmelde Informationen des Besitzers des TPM-Geräts. Die alten und neuen Autorisierungs Kennwörter für Besitzer sind erforderlich.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Changebesitzauth-Methode der CIM_TPM-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360022"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a>Changebesitzauth-Methode der CIM \_ TPM-Klasse

Ändert die Autorisierungs Anmelde Informationen des Besitzers des TPM-Geräts. Die alten und neuen Autorisierungs Kennwörter für Besitzer sind erforderlich.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Oldownerauth* \[ in\]
</dt> <dd>

Stellt die alten Autorisierungs Anmelde Informationen dar, die erforderlich sind, um das TPM-Gerät in Besitz zu nehmen. Die **CIM \_ sharedcredential** -Unterklasse ist möglicherweise mit einem nicht-NULL-Wert von **CIM \_ sharedcredential** erforderlich.**Secret** -Eigenschaft für den-Parameter.

</dd> <dt>

" *Netwownerauth* \[ " in\]
</dt> <dd>

Stellt die neuen Autorisierungs Anmelde Informationen dar, die erforderlich sind, um das TPM-Gerät in Besitz zu nehmen. Die **CIM \_ sharedcredential** -Unterklasse ist möglicherweise mit einem nicht-NULL-Wert von **CIM \_ sharedcredential** erforderlich.**Secret** -Eigenschaft für den-Parameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannter/nicht** angegebener Fehler (2)
</dt> <dt>

**DMTF reserviert** (3.. 4095)
</dt> <dt>

**Reservierte Methode** (4096.. 32767)
</dt> <dt>

**Anbieter angegeben** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ TPM**](cim-tpm.md)
</dt> </dl>

 

 




