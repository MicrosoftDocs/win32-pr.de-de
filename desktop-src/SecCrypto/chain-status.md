---
description: Ruft den Gültigkeits Status der Kette oder eines bestimmten Zertifikats in der Kette ab.
title: 'IChain2:: Status-Eigenschaft'
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
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371602"
---
# <a name="ichain2status-property"></a>IChain2:: Status-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Status** -Eigenschaft ruft den Gültigkeits Status der Kette oder eines bestimmten Zertifikats in der Kette ab.

## <a name="syntax"></a>Syntax


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Eigenschaftswert

Ein **Long** -Wert, der den Gültigkeits Status Indikator der Kette oder des angegebenen Zertifikats darstellt. In der folgenden Tabelle sind die möglichen Werte aufgeführt. Diese Eigenschaft enthält 0 (null), wenn die Kette oder das angegebene Zertifikat gültig ist. Andernfalls enthält diese Eigenschaft eine Kombination aus einem oder mehreren der folgenden Werte.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist \_ nicht \_ Zeit \_ gültig** (&H00000001).


</dt> <dd>

Dieses Zertifikat oder eines der Zertifikate in der Zertifikatskette ist nicht Zeit gültig.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist \_ nicht \_ Zeit \_** -und nicht (&H00000002).


</dt> <dd>

Die Zertifikate in der Kette sind nicht ordnungsgemäß in die Zeit eingebettet.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ Die Vertrauensstellung \_ wird \_ widerrufen** (&H00000004).


</dt> <dd>

Die Vertrauenswürdigkeit für dieses Zertifikat oder eines der Zertifikate in der Zertifikat Kette wurde widerrufen.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ Die Vertrauenswürdigkeit \_ ist \_ nicht \_ \_ gültig** (&H00000008).


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist keine gültige Signatur auf.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist \_ für die \_ \_ \_ Verwendung ungültig** (&H00000010).


</dt> <dd>

Das Zertifikat oder die Zertifikatskette ist für die vorgeschlagene Verwendung nicht gültig.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ Vertrauensstellung \_ ist \_ nicht vertrauenswürdiger \_** Stamm (&H00000020)


</dt> <dd>

Das Zertifikat oder die Zertifikatskette basiert auf einem nicht vertrauenswürdigen Stamm.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ Der Vertrauens Sperr \_ \_ Status ist \_ unbekannt** (&H00000040).


</dt> <dd>

Der Sperr Status des Zertifikats oder eines der Zertifikate in der Zertifikatskette ist unbekannt.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist \_ zyklisch** (&H00000080).


</dt> <dd>

Eines der Zertifikate in der Kette wurde von einer [*Zertifizierungs*](../secgloss/c-gly.md) Stelle ausgestellt, von der das ursprüngliche Zertifikat zertifiziert wurde.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ \_Ungültige \_ Erweiterung Vertrauen** (&H00000100)


</dt> <dd>

Eines der Zertifikate weist eine ungültige Erweiterung auf.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ \_Ungültige \_ Richtlinien \_ Einschränkungen Vertrauen** (&H00000200)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine richtlinieneinschränkungs-Erweiterung auf, und eines der ausgestellten Zertifikate hat eine unzulässige richtlinienzuordnungserweiterung oder verfügt nicht über die erforderliche Ausstellungs Richtlinien Erweiterung.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ \_Ungültige \_ grundlegende \_ Einschränkungen Vertrauen** (&H00000400)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette verfügt über eine grundlegende Einschränkungs Erweiterung, und entweder kann das Zertifikat nicht zum Ausstellen anderer Zertifikate verwendet werden, oder die Länge des Ketten Pfades wurde überschritten.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ \_Einschränkungen für ungültige \_ namens \_ Einschränkungen** (&H00000800)


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikatskette weist eine ungültige namens Einschränkungs Erweiterung auf.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ "Trust" \_ hat \_ keine \_ unterstützte \_ namens \_ Einschränkung** (&H00001000).


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine namens Einschränkungs Erweiterung auf, die nicht unterstützte Felder enthält. Die minimalen und maximalen Felder werden nicht unterstützt. Daher muss der Minimalwert immer NULL sein, und der Höchstwert muss immer nicht vorhanden sein. Nur UPN wird für einen anderen Namen unterstützt. Die folgenden alternativen Namensoptionen werden nicht unterstützt:

-   X400-Adresse
-   Name der EDI-Partei
-   Registrierte ID

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ Der \_ Trust \_ hat \_ keine \_ namens \_ Einschränkung definiert** (&H00002000).


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine namens Einschränkungs Erweiterung auf, und für eine der Namensoptionen im Endzertifikat fehlt eine namens Einschränkung.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ Für die Vertrauensstellung \_ ist \_ keine \_ \_ namens \_ Einschränkung zulässig** (&H00004000).


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine namens Einschränkungs Erweiterung auf, und es gibt keine zulässige namens Einschränkung für eine der Namensoptionen im Endzertifikat.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ Die Vertrauensstellung \_ hat eine \_ Ausschluss \_ namens \_ Einschränkung** (&H00008000).


</dt> <dd>

Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine namens Einschränkungs Erweiterung auf, und eine der Namensoptionen im Endzertifikat wird explizit ausgeschlossen.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist eine \_ Offline \_** Sperrung (&H01000000).


</dt> <dd>

Der Sperr Status des Zertifikats oder eines der Zertifikate in der Zertifikatskette ist entweder offline oder veraltet.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ Vertrauensstellungs- \_ \_ \_ \_ Richtlinie Vertrauen** (&H02000000)


</dt> <dd>

Das Endzertifikat hat keine resultierenden Ausstellungs Richtlinien, und eines der ausstellenden Zertifizierungsstellen Zertifikate hat eine Richtlinien Einschränkungs Erweiterung, die es benötigt.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ Vertrauensstellung \_ ist \_ partielle \_ Kette** (&H00010000)


</dt> <dd>

Die Zertifikatskette ist nicht konkurrenzfähig.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ Trust \_ CTL \_ ist \_ nicht \_ Zeit \_ gültig** (&H00020000)


</dt> <dd>

Eine CTL, die zum Erstellen dieser Kette verwendet wurde, war nicht Zeit gültig.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ "Trust \_ CTL" \_ ist \_ keine \_ Signatur \_ gültig** (&H00040000)


</dt> <dd>

Eine CTL, die zum Erstellen dieser Kette verwendet wurde, hatte keine gültige Signatur.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ "Trust \_ CTL" \_ ist \_ für die \_ \_ \_ Verwendung ungültig** (&H00080000).


</dt> <dd>

Eine CTL, die zum Erstellen dieser Kette verwendet wird, ist für diese Verwendung nicht gültig.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
