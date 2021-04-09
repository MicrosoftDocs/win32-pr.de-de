---
description: Fordert an, dass der Status des TPM in den im requestedtpmstate-Parameter angegebenen Wert geändert wird.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Requesttpmstatechange-Methode der CIM_TPM-Klasse
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
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959406"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a>Requesttpmstatechange-Methode der CIM \_ TPM-Klasse

Fordert an, dass der Status des TPM in den im *requestedtpmstate* -Parameter angegebenen Wert geändert wird. Wenn der Methodenaufruf erfolgreich abgeschlossen wurde, muss die **tpmstate** -Eigenschaft gleich dem **requestedtpmstate** -Parameter sein. Wenn Sie die **requesttpmstatechange** -Methode mehrmals aufrufen, kann dies dazu führen, dass frühere Anforderungen überschrieben werden oder verloren gehen.

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

*Requestedtpmstate* \[ in\]
</dt> <dd>

Der angeforderte TPM-Status.

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**S1 aktiviert-aktiv** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 deaktiviert-aktiv** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**S3 aktiviert-inaktiv** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**S4 deaktiviert-inaktiv** (5)


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**S5 aktiviert, aktiv/nicht im Besitz** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 deaktiviert, aktiv/nicht im Besitz** (7)


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 aktiviert, inaktiv** (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 deaktiviert, inaktiv-nicht im Besitz** (9)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Authorizationtoken* \[ in\]
</dt> <dd>

Autorisierungs Token, das möglicherweise erforderlich ist, damit die Aktion wirksam wird. Der *authorizationtoken* -Parameter ist möglicherweise erforderlich, um eine physische Präsenz einzurichten, oder um die Besitzer Authentifizierung, das von TCG definierte Besitzer Autorisierungs Kennwort, zu übergeben. Im Fall von "Besitzer Authentifizierung" ist möglicherweise der CIM " \_ sharedcredential" mit dem Wert "CIM \_ sharedcredential. Secret" erforderlich, der nicht NULL ist. Die CIM \_ sharedcredential. algorithmuseigenschaft kann auch basierend auf der Eigenschaft CIM \_ tpmfunktionen. supportedpasswordalgorithms angegeben werden.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Kann einen Verweis auf den erstellten [**CIM- \_ bettejob**](cim-concretejob.md) enthalten, um den durch den Methodenaufruf initiierten Zustandsübergang zu verfolgen.

</dd> <dt>

*Timeoutperiod* \[ in\]
</dt> <dd>

Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Zum Angeben des *timeoutperiod* muss das Intervall Format verwendet werden. Der Wert 0 oder ein NULL-Parameter gibt an, dass der Client keine Zeitanforderungen für den Übergang hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannter oder nicht** angegebener Fehler (2)
</dt> <dt>

**Kann nicht innerhalb des Timeout Zeitraums** (3) beendet werden.
</dt> <dt>

Fehler **(4** )
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**In Gebrauch** (6)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Ungültiger Status Übergang** (4097).
</dt> <dt>

**Verwendung des timeout-Parameters wird nicht unterstützt** (4098)
</dt> <dt>

**Ausgelastet** (4099)
</dt> <dt>

**Reservierte Methode** (4100.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
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

 

 




