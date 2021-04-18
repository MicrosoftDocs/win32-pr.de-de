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
# <a name="ichain2status-property"></a><span data-ttu-id="f17ee-103">IChain2:: Status-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f17ee-103">IChain2::Status property</span></span>

<span data-ttu-id="f17ee-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f17ee-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f17ee-105">Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="f17ee-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f17ee-106">Die **Status** -Eigenschaft ruft den Gültigkeits Status der Kette oder eines bestimmten Zertifikats in der Kette ab.</span><span class="sxs-lookup"><span data-stu-id="f17ee-106">The **Status** property retrieves the validity status of the chain or a specific certificate in the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="f17ee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f17ee-107">Syntax</span></span>


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a><span data-ttu-id="f17ee-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f17ee-108">Property value</span></span>

<span data-ttu-id="f17ee-109">Ein **Long** -Wert, der den Gültigkeits Status Indikator der Kette oder des angegebenen Zertifikats darstellt.</span><span class="sxs-lookup"><span data-stu-id="f17ee-109">A **LONG** value that represents the validity status indicator of the chain or the specified certificate.</span></span> <span data-ttu-id="f17ee-110">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f17ee-110">The following table shows the possible values.</span></span> <span data-ttu-id="f17ee-111">Diese Eigenschaft enthält 0 (null), wenn die Kette oder das angegebene Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="f17ee-111">This property will contain zero if the chain or specified certificate is valid.</span></span> <span data-ttu-id="f17ee-112">Andernfalls enthält diese Eigenschaft eine Kombination aus einem oder mehreren der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="f17ee-112">Otherwise, this property will contain a combination of one or more of the following values.</span></span>

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span data-ttu-id="f17ee-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist \_ nicht \_ Zeit \_ gültig** (&H00000001).</span><span class="sxs-lookup"><span data-stu-id="f17ee-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_VALID** (&H00000001)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-114">Dieses Zertifikat oder eines der Zertifikate in der Zertifikatskette ist nicht Zeit gültig.</span><span class="sxs-lookup"><span data-stu-id="f17ee-114">This certificate or one of the certificates in the certificate chain is not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span data-ttu-id="f17ee-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist \_ nicht \_ Zeit \_** -und nicht (&H00000002).</span><span class="sxs-lookup"><span data-stu-id="f17ee-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_NESTED** (&H00000002)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-116">Die Zertifikate in der Kette sind nicht ordnungsgemäß in die Zeit eingebettet.</span><span class="sxs-lookup"><span data-stu-id="f17ee-116">Certificates in the chain are not properly time nested.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span data-ttu-id="f17ee-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ Die Vertrauensstellung \_ wird \_ widerrufen** (&H00000004).</span><span class="sxs-lookup"><span data-stu-id="f17ee-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM\_TRUST\_IS\_REVOKED** (&H00000004)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-118">Die Vertrauenswürdigkeit für dieses Zertifikat oder eines der Zertifikate in der Zertifikat Kette wurde widerrufen.</span><span class="sxs-lookup"><span data-stu-id="f17ee-118">Trust for this certificate or one of the certificates in the certificate chain has been revoked.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span data-ttu-id="f17ee-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ Die Vertrauenswürdigkeit \_ ist \_ nicht \_ \_ gültig** (&H00000008).</span><span class="sxs-lookup"><span data-stu-id="f17ee-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_SIGNATURE\_VALID** (&H00000008)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-120">Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist keine gültige Signatur auf.</span><span class="sxs-lookup"><span data-stu-id="f17ee-120">The certificate or one of the certificates in the certificate chain does not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span data-ttu-id="f17ee-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist \_ für die \_ \_ \_ Verwendung ungültig** (&H00000010).</span><span class="sxs-lookup"><span data-stu-id="f17ee-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00000010)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-122">Das Zertifikat oder die Zertifikatskette ist für die vorgeschlagene Verwendung nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="f17ee-122">The certificate or certificate chain is not valid for its proposed usage.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span data-ttu-id="f17ee-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ Vertrauensstellung \_ ist \_ nicht vertrauenswürdiger \_** Stamm (&H00000020)</span><span class="sxs-lookup"><span data-stu-id="f17ee-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM\_TRUST\_IS\_UNTRUSTED\_ROOT** (&H00000020)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-124">Das Zertifikat oder die Zertifikatskette basiert auf einem nicht vertrauenswürdigen Stamm.</span><span class="sxs-lookup"><span data-stu-id="f17ee-124">The certificate or certificate chain is based on an untrusted root.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span data-ttu-id="f17ee-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ Der Vertrauens Sperr \_ \_ Status ist \_ unbekannt** (&H00000040).</span><span class="sxs-lookup"><span data-stu-id="f17ee-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM\_TRUST\_REVOCATION\_STATUS\_UNKNOWN** (&H00000040)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-126">Der Sperr Status des Zertifikats oder eines der Zertifikate in der Zertifikatskette ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f17ee-126">The revocation status of the certificate or one of the certificates in the certificate chain is unknown.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span data-ttu-id="f17ee-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist \_ zyklisch** (&H00000080).</span><span class="sxs-lookup"><span data-stu-id="f17ee-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM\_TRUST\_IS\_CYCLIC** (&H00000080)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-128">Eines der Zertifikate in der Kette wurde von einer [*Zertifizierungs*](../secgloss/c-gly.md) Stelle ausgestellt, von der das ursprüngliche Zertifikat zertifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="f17ee-128">One of the certificates in the chain was issued by a [*certification authority*](../secgloss/c-gly.md) that the original certificate had certified.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span data-ttu-id="f17ee-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ \_Ungültige \_ Erweiterung Vertrauen** (&H00000100)</span><span class="sxs-lookup"><span data-stu-id="f17ee-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM\_TRUST\_INVALID\_EXTENSION** (&H00000100)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-130">Eines der Zertifikate weist eine ungültige Erweiterung auf.</span><span class="sxs-lookup"><span data-stu-id="f17ee-130">One of the certificates has an extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span data-ttu-id="f17ee-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ \_Ungültige \_ Richtlinien \_ Einschränkungen Vertrauen** (&H00000200)</span><span class="sxs-lookup"><span data-stu-id="f17ee-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM\_TRUST\_INVALID\_POLICY\_CONSTRAINTS** (&H00000200)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-132">Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine richtlinieneinschränkungs-Erweiterung auf, und eines der ausgestellten Zertifikate hat eine unzulässige richtlinienzuordnungserweiterung oder verfügt nicht über die erforderliche Ausstellungs Richtlinien Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="f17ee-132">The certificate or one of the certificates in the certificate chain has a policy constraints extension, and one of the issued certificates has a disallowed policy mapping extension or does not have a required issuance policies extension.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span data-ttu-id="f17ee-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ \_Ungültige \_ grundlegende \_ Einschränkungen Vertrauen** (&H00000400)</span><span class="sxs-lookup"><span data-stu-id="f17ee-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM\_TRUST\_INVALID\_BASIC\_CONSTRAINTS** (&H00000400)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-134">Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette verfügt über eine grundlegende Einschränkungs Erweiterung, und entweder kann das Zertifikat nicht zum Ausstellen anderer Zertifikate verwendet werden, oder die Länge des Ketten Pfades wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="f17ee-134">The certificate or one of the certificates in the certificate chain has a basic constraints extension, and either the certificate cannot be used to issue other certificates, or the chain path length has been exceeded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span data-ttu-id="f17ee-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ \_Einschränkungen für ungültige \_ namens \_ Einschränkungen** (&H00000800)</span><span class="sxs-lookup"><span data-stu-id="f17ee-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM\_TRUST\_INVALID\_NAME\_CONSTRAINTS** (&H00000800)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-136">Das Zertifikat oder eines der Zertifikate in der Zertifikatskette weist eine ungültige namens Einschränkungs Erweiterung auf.</span><span class="sxs-lookup"><span data-stu-id="f17ee-136">The certificate or one of the certificates in the certificate chain has a name constraints extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span data-ttu-id="f17ee-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ "Trust" \_ hat \_ keine \_ unterstützte \_ namens \_ Einschränkung** (&H00001000).</span><span class="sxs-lookup"><span data-stu-id="f17ee-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_SUPPORTED\_NAME\_CONSTRAINT** (&H00001000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-138">Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine namens Einschränkungs Erweiterung auf, die nicht unterstützte Felder enthält.</span><span class="sxs-lookup"><span data-stu-id="f17ee-138">The certificate or one of the certificates in the certificate chain has a name constraints extension that contains unsupported fields.</span></span> <span data-ttu-id="f17ee-139">Die minimalen und maximalen Felder werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f17ee-139">The minimum and maximum fields are not supported.</span></span> <span data-ttu-id="f17ee-140">Daher muss der Minimalwert immer NULL sein, und der Höchstwert muss immer nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f17ee-140">Thus minimum must always be zero and maximum must always be absent.</span></span> <span data-ttu-id="f17ee-141">Nur UPN wird für einen anderen Namen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f17ee-141">Only UPN is supported for an Other Name.</span></span> <span data-ttu-id="f17ee-142">Die folgenden alternativen Namensoptionen werden nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f17ee-142">The following alternative name choices are not supported:</span></span>

-   <span data-ttu-id="f17ee-143">X400-Adresse</span><span class="sxs-lookup"><span data-stu-id="f17ee-143">X400 Address</span></span>
-   <span data-ttu-id="f17ee-144">Name der EDI-Partei</span><span class="sxs-lookup"><span data-stu-id="f17ee-144">EDI Party Name</span></span>
-   <span data-ttu-id="f17ee-145">Registrierte ID</span><span class="sxs-lookup"><span data-stu-id="f17ee-145">Registered Id</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span data-ttu-id="f17ee-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ Der \_ Trust \_ hat \_ keine \_ namens \_ Einschränkung definiert** (&H00002000).</span><span class="sxs-lookup"><span data-stu-id="f17ee-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_DEFINED\_NAME\_CONSTRAINT** (&H00002000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-147">Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine namens Einschränkungs Erweiterung auf, und für eine der Namensoptionen im Endzertifikat fehlt eine namens Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="f17ee-147">The certificate or one of the certificates in the certificate chain has a name constraints extension, and a name constraint is missing for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span data-ttu-id="f17ee-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ Für die Vertrauensstellung \_ ist \_ keine \_ \_ namens \_ Einschränkung zulässig** (&H00004000).</span><span class="sxs-lookup"><span data-stu-id="f17ee-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_PERMITTED\_NAME\_CONSTRAINT** (&H00004000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-149">Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine namens Einschränkungs Erweiterung auf, und es gibt keine zulässige namens Einschränkung für eine der Namensoptionen im Endzertifikat.</span><span class="sxs-lookup"><span data-stu-id="f17ee-149">The certificate or one of the certificates in the certificate chain has a name constraints extension, and there is not a permitted name constraint for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span data-ttu-id="f17ee-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ Die Vertrauensstellung \_ hat eine \_ Ausschluss \_ namens \_ Einschränkung** (&H00008000).</span><span class="sxs-lookup"><span data-stu-id="f17ee-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_EXCLUDED\_NAME\_CONSTRAINT** (&H00008000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-151">Das Zertifikat oder eines der Zertifikate in der Zertifikat Kette weist eine namens Einschränkungs Erweiterung auf, und eine der Namensoptionen im Endzertifikat wird explizit ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f17ee-151">The certificate or one of the certificates in the certificate chain has a name constraints extension, and one of the name choices in the end certificate is explicitly excluded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span data-ttu-id="f17ee-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ Die Vertrauensstellung \_ ist eine \_ Offline \_** Sperrung (&H01000000).</span><span class="sxs-lookup"><span data-stu-id="f17ee-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM\_TRUST\_IS\_OFFLINE\_REVOCATION** (&H01000000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-153">Der Sperr Status des Zertifikats oder eines der Zertifikate in der Zertifikatskette ist entweder offline oder veraltet.</span><span class="sxs-lookup"><span data-stu-id="f17ee-153">The revocation status of the certificate or one of the certificates in the certificate chain is either offline or stale.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span data-ttu-id="f17ee-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ Vertrauensstellungs- \_ \_ \_ \_ Richtlinie Vertrauen** (&H02000000)</span><span class="sxs-lookup"><span data-stu-id="f17ee-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM\_TRUST\_NO\_ISSUANCE\_CHAIN\_POLICY** (&H02000000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-155">Das Endzertifikat hat keine resultierenden Ausstellungs Richtlinien, und eines der ausstellenden Zertifizierungsstellen Zertifikate hat eine Richtlinien Einschränkungs Erweiterung, die es benötigt.</span><span class="sxs-lookup"><span data-stu-id="f17ee-155">The end certificate does not have any resultant issuance policies, and one of the issuing CA certificates has a policy constraints extension requiring it.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span data-ttu-id="f17ee-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ Vertrauensstellung \_ ist \_ partielle \_ Kette** (&H00010000)</span><span class="sxs-lookup"><span data-stu-id="f17ee-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM\_TRUST\_IS\_PARTIAL\_CHAIN** (&H00010000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-157">Die Zertifikatskette ist nicht konkurrenzfähig.</span><span class="sxs-lookup"><span data-stu-id="f17ee-157">The certificate chain is not compete.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span data-ttu-id="f17ee-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ Trust \_ CTL \_ ist \_ nicht \_ Zeit \_ gültig** (&H00020000)</span><span class="sxs-lookup"><span data-stu-id="f17ee-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_TIME\_VALID** (&H00020000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-159">Eine CTL, die zum Erstellen dieser Kette verwendet wurde, war nicht Zeit gültig.</span><span class="sxs-lookup"><span data-stu-id="f17ee-159">A CTL used to create this chain was not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span data-ttu-id="f17ee-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ "Trust \_ CTL" \_ ist \_ keine \_ Signatur \_ gültig** (&H00040000)</span><span class="sxs-lookup"><span data-stu-id="f17ee-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_SIGNATURE\_VALID** (&H00040000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-161">Eine CTL, die zum Erstellen dieser Kette verwendet wurde, hatte keine gültige Signatur.</span><span class="sxs-lookup"><span data-stu-id="f17ee-161">A CTL used to create this chain did not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span data-ttu-id="f17ee-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ "Trust \_ CTL" \_ ist \_ für die \_ \_ \_ Verwendung ungültig** (&H00080000).</span><span class="sxs-lookup"><span data-stu-id="f17ee-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00080000)</span></span>


</dt> <dd>

<span data-ttu-id="f17ee-163">Eine CTL, die zum Erstellen dieser Kette verwendet wird, ist für diese Verwendung nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="f17ee-163">A CTL used to create this chain is not valid for this usage.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f17ee-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f17ee-164">Requirements</span></span>



| <span data-ttu-id="f17ee-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f17ee-165">Requirement</span></span> | <span data-ttu-id="f17ee-166">Wert</span><span class="sxs-lookup"><span data-stu-id="f17ee-166">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f17ee-167">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f17ee-167">End of client support</span></span><br/> | <span data-ttu-id="f17ee-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f17ee-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f17ee-169">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f17ee-169">End of server support</span></span><br/> | <span data-ttu-id="f17ee-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f17ee-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f17ee-171">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f17ee-171">Redistributable</span></span><br/>       | <span data-ttu-id="f17ee-172">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f17ee-172">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f17ee-173">DLL</span><span class="sxs-lookup"><span data-stu-id="f17ee-173">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f17ee-174"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f17ee-174"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
