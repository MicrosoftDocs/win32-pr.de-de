---
description: Ruft den Gültigkeitsstatus der Kette oder eines bestimmten Zertifikats in der Kette ab.
title: IChain2::Status (Eigenschaft)
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
# <a name="ichain2status-property"></a>IChain2::Status (Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Status-Eigenschaft** ruft den Gültigkeitsstatus der Kette oder eines bestimmten Zertifikats in der Kette ab.

## <a name="syntax"></a>Syntax


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Eigenschaftswert

Ein **LONG-Wert,** der den Gültigkeitsstatusindikator der Kette oder des angegebenen Zertifikats darstellt. In der folgenden Tabelle sind die möglichen Werte aufgeführt. Diese Eigenschaft enthält 0 (null), wenn die Kette oder das angegebene Zertifikat gültig ist. Andernfalls enthält diese Eigenschaft eine Kombination aus mindestens einem der folgenden Werte.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ TRUST \_ IS \_ NOT \_ TIME \_ VALID** (&H00000001)


</dt> <dd>

Dieses Zertifikat oder eines der Zertifikate in der Zertifikatkette ist nicht zeit gültig.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ TRUST \_ IS \_ NOT \_ TIME \_ NESTED** (&H00000002)


</dt> <dd>

Zertifikate in der Kette sind nicht ordnungsgemäß geschachtelt.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ TRUST \_ IS \_ REVOKED** (&H00000004)


</dt> <dd>

Die Vertrauensstellung für dieses Zertifikat oder eines der Zertifikate in der Zertifikatkette wurde widerrufen.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ TRUST \_ IS \_ NOT \_ SIGNATURE \_ VALID** (&H00000008)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt nicht über eine gültige Signatur.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ TRUST IS NOT VALID FOR USAGE (&\_ \_ \_ \_ \_** H00000010) (VERTRAUENSSTELLUNG IST FÜR DIE VERWENDUNG UNGÜLTIG (&H00000010)


</dt> <dd>

Das Zertifikat oder die Zertifikatkette ist für die vorgeschlagene Verwendung ungültig.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ TRUST \_ IS \_ UNTRUSTED \_ ROOT** (&H00000020)


</dt> <dd>

Das Zertifikat oder die Zertifikatkette basiert auf einem nicht vertrauenswürdigen Stamm.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ \_ \_ VERTRAUENSSPERRSTATUS \_ UNBEKANNT** (&H00000040)


</dt> <dd>

Der Sperrstatus des Zertifikats oder eines der Zertifikate in der Zertifikatkette ist unbekannt.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ TRUST \_ IS \_ CYCLIC** (&H00000080)


</dt> <dd>

Eines der Zertifikate in der Kette wurde von einer Zertifizierungsstelle [*ausgestellt,*](../secgloss/c-gly.md) die das ursprüngliche Zertifikat zertifiziert hat.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ UNGÜLTIGE \_ \_ ERWEITERUNG** VERTRAUEN (&H00000100)


</dt> <dd>

Eines der Zertifikate verfügt über eine ungültige Erweiterung.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ \_UNGÜLTIGE \_ \_ RICHTLINIENEINSCHRÄNKUNGEN** VERTRAUEN (&H00000200)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Richtlinieneinschränkungserweiterung, und eines der ausgestellten Zertifikate verfügt über eine nicht erteilte Richtlinienzuordnungserweiterung oder keine erforderliche Erweiterung für Ausstellungsrichtlinien.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ TRUST \_ INVALID \_ BASIC \_ CONSTRAINTS** (&H00000400)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Erweiterung mit grundlegenden Einschränkungen, und entweder kann das Zertifikat nicht zum Aushängen anderer Zertifikate verwendet werden, oder die Länge des Kettenpfads wurde überschritten.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ \_UNGÜLTIGE \_ \_ NAMENSEINSCHRÄNKUNGEN** VERTRAUEN (&H00000800)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine ungültige Namenseinschränkungserweiterung.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ TRUST \_ HAS \_ NOT \_ SUPPORTED \_ NAME \_ CONSTRAINT** (&H00001000)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Namenseinschränkungserweiterung, die nicht unterstützte Felder enthält. Die minimalen und maximalen Felder werden nicht unterstützt. Daher muss der Mindestwert immer 0 (null) und der Höchstwert immer fehlen. Nur DER UPN wird für einen anderen Namen unterstützt. Die folgenden alternativen Namensoptionen werden nicht unterstützt:

-   X400-Adresse
-   EDI-Parteiname
-   Registrierte ID

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ TRUST \_ HAS \_ NOT \_ DEFINED \_ NAME \_ CONSTRAINT** (&H00002000)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Namenseinschränkungserweiterung, und für eine der Namensoptionen im Endzertifikat fehlt eine Namenseinschränkung.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ TRUST \_ HAS \_ NOT \_ PERMITTED \_ NAME \_ CONSTRAINT** (&H00004000)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Namenseinschränkungserweiterung, und es gibt keine Einschränkung für den zulässigen Namen für eine der Namensoptionen im Endzertifikat.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ TRUST \_ HAS \_ EXCLUDED \_ NAME \_ CONSTRAINT** (&H00008000)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatkette verfügt über eine Namenseinschränkungserweiterung, und eine der Namensoptionen im Endzertifikat wird explizit ausgeschlossen.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ VERTRAUENSSTELLUNG \_ \_ IST \_ OFFLINESPERRUNG** (&H01000000)


</dt> <dd>

Der Sperrstatus des Zertifikats oder eines der Zertifikate in der Zertifikatkette ist offline oder veraltet.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ TRUST \_ NO \_ ISSUANCE \_ CHAIN \_ POLICY** (&H02000000)


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

Eine CTL, die zum Erstellen dieser Kette verwendet wurde, war nicht zeit gültig.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ TRUST CTL IS NOT SIGNATURE VALID (TRUST \_ CTL \_ IS NOT \_ SIGNATURE \_ \_ VALID,** &H00040000)


</dt> <dd>

Eine CTL, die zum Erstellen dieser Kette verwendet wurde, hat keine gültige Signatur.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ TRUST CTL IS NOT VALID FOR USAGE (TRUST CTL IS \_ \_ NOT VALID FOR \_ \_ \_ \_ USAGE** , &H00080000)


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



 

 
