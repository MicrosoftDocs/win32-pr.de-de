---
description: Fordert an, dass der Zustand des TPM in den im RequestedTPMState-Parameter angegebenen Wert geändert wird.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: RequestTPMStateChange-Methode der CIM_TPM-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 94af1d619ffa686b2fb4546987c6b825e4c658a5ae045d84fe5c6181716e95e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646448"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a>RequestTPMStateChange-Methode der CIM \_ TPM-Klasse

Fordert an, dass der Zustand des TPM in den im *RequestedTPMState-Parameter* angegebenen Wert geändert wird. Wenn der Methodenaufruf erfolgreich abgeschlossen wird, muss die **TPMState-Eigenschaft** gleich dem **RequestedTPMState-Parameter** sein. Das mehrmalige Aufrufen der **RequestTPMStateChange-Methode** kann dazu führen, dass frühere Anforderungen überschrieben oder verloren gegangen sind.

## <a name="syntax"></a>Syntax


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RequestedTPMState* \[ In\]
</dt> <dd>

Der angeforderte TPM-Status.

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**S1 Enabled-Active-Owned** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 Deaktiviert-Aktiv-Besitzer** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**S3 Enabled-Inactive-Owned** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**S4 Disabled-Inactive-Owned (5)**


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**S5 Enabled-Active-Unowned** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 Disabled-Active-Unowned (7)**


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 Enabled-Inactive-Unowned** (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 Disabled-Inactive-Unowned** (9)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*AuthorizationToken* \[ In\]
</dt> <dd>

Autorisierungstoken, das möglicherweise erforderlich ist, damit die Aktion wirksam wird. Der *AuthorizationToken-Parameter* kann erforderlich sein, um physische Präsenz einzurichten oder ownerAuth, das tcg-definierte Besitzerautorisierungskennwort, zu übergeben. Im Fall von OwnerAuth ist möglicherweise der CIM \_ SharedCredential-Wert mit einem Wert ungleich NULL von CIM \_ SharedCredential.Secret erforderlich. Die CIM \_ SharedCredential.Algorithm-Eigenschaft kann auch basierend auf der Eigenschaft CIM \_ TPMCapabilities.SupportedPasswordAlgorithms angegeben werden.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Kann einen Verweis auf den [**CIM \_ ConcreteJob**](cim-concretejob.md) enthalten, der erstellt wurde, um den Zustandsübergang nachzuverfolgen, der durch den Methodenaufruf initiiert wurde.

</dd> <dt>

*TimeoutPeriod* \[ In\]
</dt> <dd>

Ein Timeoutzeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervallformat muss verwendet werden, um *timeoutPeriod* anzugeben. Der Wert 0 oder ein NULL-Parameter gibt an, dass der Client keine Zeitanforderungen für den Übergang hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 oder 4096 zurückgegeben. andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannter oder nicht angegebener Fehler** (2)
</dt> <dt>

**Kann nicht innerhalb des Timeoutzeitraums abgeschlossen werden** (3)
</dt> <dt>

**Fehler** (4)
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**In Verwendung** (6)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Ungültiger Zustandsübergang** (4097)
</dt> <dt>

**Verwendung des Timeoutparameters Wird nicht unterstützt** (4098)
</dt> <dt>

**Ausgelastet** (4099)
</dt> <dt>

**Reservierte Methode** (4100..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ TPM**](cim-tpm.md)
</dt> </dl>

 

 




