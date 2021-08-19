---
description: Ruft den Gültigkeitsstatus der Kette oder eines bestimmten Zertifikats in der Kette ab.
title: IChain2::Status-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5307d03d340a0a960a5d78226d26e7b5553d27af72f255131651690e5b723355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769550"
---
# <a name="ichain2status-property"></a>IChain2::Status-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Status -Eigenschaft** ruft den Gültigkeitsstatus der Kette oder eines bestimmten Zertifikats in der Kette ab.

## <a name="syntax"></a>Syntax


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Eigenschaftswert

Ein **LONG-Wert,** der den Gültigkeitsstatusindikator der Kette oder des angegebenen Zertifikats darstellt. In der folgenden Tabelle sind die möglichen Werte aufgeführt. Diese Eigenschaft enthält 0 (null), wenn die Kette oder das angegebene Zertifikat gültig ist. Andernfalls enthält diese Eigenschaft eine Kombination aus einem oder mehreren der folgenden Werte.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ TRUST \_ IS \_ NOT \_ TIME \_ VALID** (&H00000001)


</dt> <dd>

Dieses Zertifikat oder eines der Zertifikate in der Zertifikatkette ist nicht zeit gültig.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ TRUST \_ IS NOT TIME \_ \_ \_ NESTED** (&H000000002)


</dt> <dd>

Zertifikate in der Kette sind nicht ordnungsgemäß geschachtelt.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ TRUST \_ IS \_ REVOKED** (&H000000004)


</dt> <dd>

Die Vertrauensstellung für dieses Zertifikat oder eines der Zertifikate in der Zertifikatkette wurde aufgehoben.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ TRUST \_ IST NICHT SIGNATUR \_ \_ \_ GÜLTIG** (&H00000008)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt nicht über eine gültige Signatur.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ TRUST \_ IST FÜR DIE \_ \_ \_ \_ VERWENDUNG UNGÜLTIG** (&H00000010)


</dt> <dd>

Das Zertifikat oder die Zertifikatkette ist für die vorgeschlagene Verwendung ungültig.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ TRUST \_ IS \_ UNTRUSTED \_ ROOT** (&H00000020)


</dt> <dd>

Das Zertifikat oder die Zertifikatkette basiert auf einem nicht vertrauenswürdigen Stamm.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ TRUST \_ REVOCATION \_ STATUS \_ UNKNOWN** (&H00000040)


</dt> <dd>

Der Sperrstatus des Zertifikats oder eines der Zertifikate in der Zertifikatkette ist unbekannt.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ TRUST \_ IS \_ CYCLIC** (&H000000080)


</dt> <dd>

Eines der Zertifikate in der Kette wurde von einer [*Zertifizierungsstelle*](../secgloss/c-gly.md) ausgestellt, die das ursprüngliche Zertifikat zertifiziert hatte.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ \_UNGÜLTIGE \_ ERWEITERUNG VERTRAUEN** (&H00000100)


</dt> <dd>

Eines der Zertifikate verfügt über eine ungültige Erweiterung.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ \_UNGÜLTIGE \_ \_ RICHTLINIENEINSCHRÄNKUNGEN** VERTRAUEN (&H00000200)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Richtlinieneinschränkungserweiterung, und eines der ausgestellten Zertifikate verfügt über eine unzulässige Richtlinienzuordnungserweiterung oder verfügt nicht über eine erforderliche Erweiterung für Ausstellungsrichtlinien.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ \_UNGÜLTIGE \_ \_ BASIC-EINSCHRÄNKUNGEN** VERTRAUEN (&H00000400)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine grundlegende Einschränkungserweiterung, und entweder kann das Zertifikat nicht zum Ausstellen anderer Zertifikate verwendet werden, oder die Länge des Kettenpfads wurde überschritten.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ \_UNGÜLTIGE \_ \_ NAMENSEINSCHRÄNKUNGEN** VERTRAUEN (&H00000800)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine ungültige Namenseinschränkungserweiterung.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ VERTRAUENSSTELLUNG \_ HAT \_ KEINE \_ \_ \_ NAMENSEINSCHRÄNKUNG UNTERSTÜTZT** (&H00001000)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Namenseinschränkungserweiterung, die nicht unterstützte Felder enthält. Die Felder "Minimum" und "Maximum" werden nicht unterstützt. Daher muss minimum immer 0 (null) und maximum immer fehlen. Für einen anderen Namen wird nur UPN unterstützt. Die folgenden alternativen Namensauswahlen werden nicht unterstützt:

-   X400-Adresse
-   EDI-Partyname
-   Registrierte ID

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ TRUST \_ HAT \_ KEINE \_ \_ \_ NAMENSEINSCHRÄNKUNG DEFINIERT** (&H00002000)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Namenseinschränkungserweiterung, und für eine der Namensoptionen im Endzertifikat fehlt eine Namenseinschränkung.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ VERTRAUENSSTELLUNG \_ HAT \_ KEINE \_ \_ \_ NAMENSEINSCHRÄNKUNG** (&H00004000)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Namenseinschränkungserweiterung, und es gibt keine zulässige Namenseinschränkung für eine der Namensoptionen im Endzertifikat.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ VERTRAUENSSTELLUNG \_ HAT \_ \_ \_ NAMENSEINSCHRÄNKUNG AUSGESCHLOSSEN** (&H00008000)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Namenseinschränkungserweiterung, und eine der Namensoptionen im Endzertifikat wird explizit ausgeschlossen.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ VERTRAUENSSTELLUNG \_ IST \_ \_ OFFLINESPERRUNG** (&H01000000)


</dt> <dd>

Der Sperrstatus des Zertifikats oder eines der Zertifikate in der Zertifikatkette ist entweder offline oder veraltet.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ \_TRUST NO ISSUANCE CHAIN \_ \_ \_ POLICY** (&H020000000)


</dt> <dd>

Das Endzertifikat verfügt über keine resultierenden Ausstellungsrichtlinien, und eines der ausstellenden Zertifizierungsstellenzertifikate verfügt über eine Richtlinieneinschränkungserweiterung, die dies erfordert.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ TRUST \_ IS \_ PARTIAL \_ CHAIN** (&H00010000)


</dt> <dd>

Die Zertifikatkette ist nicht konkurriert.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ TRUST \_ CTL \_ IS \_ NOT \_ TIME \_ VALID** (&H00020000)


</dt> <dd>

Eine zum Erstellen dieser Kette verwendete CTL war nicht zeit gültig.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ \_VERTRAUENS-CTL \_ IST NICHT \_ SIGNATUR \_ \_ GÜLTIG** (&H00040000)


</dt> <dd>

Eine zum Erstellen dieser Kette verwendete CTL verfügte nicht über eine gültige Signatur.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ \_VERTRAUENS-CTL \_ IST FÜR \_ DIE \_ \_ \_ VERWENDUNG UNGÜLTIG** (&H00080000)


</dt> <dd>

Eine CTL, die zum Erstellen dieser Kette verwendet wird, ist für diese Verwendung ungültig.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
