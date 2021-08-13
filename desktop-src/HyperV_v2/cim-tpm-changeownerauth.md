---
description: Ändert die Anmeldeinformationen für die Besitzerautorisierung des TPM-Geräts. Die alten und neuen Autorisierungskennwörter des Besitzers sind erforderlich.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: ChangeOwnerAuth-Methode der CIM_TPM-Klasse
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
ms.openlocfilehash: a92911bcf9c2739d34e8b7602ab5f4cb0032fe5a77376632063971b88f2101d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646662"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a>ChangeOwnerAuth-Methode der CIM \_ TPM-Klasse

Ändert die Anmeldeinformationen für die Besitzerautorisierung des TPM-Geräts. Die alten und neuen Autorisierungskennwörter des Besitzers sind erforderlich.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OldOwnerAuth* \[ In\]
</dt> <dd>

Stellt die alten Anmeldeinformationen für die Besitzerautorisierung dar, die erforderlich sind, um den Besitz des TPM-Geräts zu übernehmen. Die **CIM \_ SharedCredential-Unterklasse** ist möglicherweise mit einem Wert von nicht NULL des **CIM \_ SharedCredential-Werts erforderlich.****Secret-Eigenschaft** für den -Parameter.

</dd> <dt>

*NewOwnerAuth* \[ In\]
</dt> <dd>

Stellt die neuen Anmeldeinformationen für die Besitzerautorisierung dar, die erforderlich sind, um den Besitz des TPM-Geräts zu übernehmen. Die **CIM \_ SharedCredential-Unterklasse** ist möglicherweise mit einem Wert von nicht NULL des **CIM \_ SharedCredential-Werts erforderlich.****Secret-Eigenschaft** für den Parameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannter/nicht angegebener Fehler** (2)
</dt> <dt>

**DMTF Reserved** (3..4095)
</dt> <dt>

**Reservierte Methode** (4096..32767)
</dt> <dt>

**Hersteller angegeben** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ TPM**](cim-tpm.md)
</dt> </dl>

 

 




