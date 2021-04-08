---
title: Eigenschaften der EAP-Methode (eaptypes. h)
description: Wird von Supplicants und Authentifikatoren verwendet, um die EAP-Methoden zu ermitteln, die mit einem bestimmten Supplicant oder Authentifikator verwendet werden sollen. Methoden Eigenschaften geben auch die Konfiguration einer Methode an.
ms.assetid: 10407b85-5d2c-4c75-9b65-a0d65d4cc7ab
topic_type:
- apiref
api_name:
- eapPropCipherSuiteNegotiation
- eapPropMutualAuth
- eapPropIntegrity
- eapPropReplayProtection
- eapPropConfidentiality
- eapPropKeyDerivation
- eapPropKeyStrength64
- eapPropKeyStrength128
- eapPropKeyStrength256
- eapPropKeyStrength512
- eapPropKeyStrength1024
- eapPropDictionaryAttackResistance
- eapPropFastReconnect
- eapPropCryptoBinding
- eapPropSessionIndependence
- eapPropFragmentation
- eapPropChannelBinding
- eapPropNap
- eapPropStandalone
- eapPropMppeEncryption
- eapPropTunnelMethod
- eapPropSupportsConfig
- eapPropCertifiedMethod
- eapPropmachineAuth
- eapPropUserAuth
- eapPropIdentityPrivacy
- eapPropMethodChaining
- eapPropSharedStateEquivalence
- eapPropReserved
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 844f897456ee21dfa93dfaa5b16b4f218ba5efb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741848"
---
# <a name="eap-method-properties"></a><span data-ttu-id="9bba3-104">Eigenschaften der EAP-Methode</span><span class="sxs-lookup"><span data-stu-id="9bba3-104">EAP Method Properties</span></span>

<span data-ttu-id="9bba3-105">Wird von Supplicants und Authentifikatoren verwendet, um die EAP-Methoden zu ermitteln, die mit einem bestimmten Supplicant oder Authentifikator verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9bba3-105">Used by supplicants and authenticators to determine the EAP methods to be used with a given supplicant or authenticator.</span></span> <span data-ttu-id="9bba3-106">Methoden Eigenschaften geben auch die Konfiguration einer Methode an.</span><span class="sxs-lookup"><span data-stu-id="9bba3-106">Method properties also specify the configuration of a method.</span></span>

<span data-ttu-id="9bba3-107">Beispielsweise erfordert der [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Supplicant möglicherweise, dass Methoden bestimmte Eigenschaften für die Verwendung mit dem [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Supplicant aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9bba3-107">For example, the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant may require methods to have certain properties for use with the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant.</span></span> <span data-ttu-id="9bba3-108">Das Schlüsselmaterial ist beispielsweise eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9bba3-108">Keying material, for example, is a requirement.</span></span>

<span data-ttu-id="9bba3-109">Die Eigenschaften werden aufgelistet, die von EAP-Methoden unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9bba3-109">The properties supported by EAP methods are listed.</span></span> <span data-ttu-id="9bba3-110">Eigenschaften werden als Registrierungsschlüssel Werte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9bba3-110">Properties are stored as registry key values.</span></span> <span data-ttu-id="9bba3-111">Weitere Informationen finden Sie im Abschnitt zum Registrierungsschlüssel der EAP-Peer Methode DLL des Themas [Registrierungs Konfiguration für EAP-Methoden.](registry-keys-for-eap-methods.md)</span><span class="sxs-lookup"><span data-stu-id="9bba3-111">For more information, see the EAP Peer Method DLL Registry Key section of the topic [Registry Configuration for EAP Methods.](registry-keys-for-eap-methods.md)</span></span>

<dl> <dt>

<span data-ttu-id="9bba3-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eappropciphersuitenegotiation**</span><span class="sxs-lookup"><span data-stu-id="9bba3-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bba3-113">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-114">Die-Methode ermöglicht das Aushandeln der Verschlüsselungs Sammlung für den Zweck der Datenverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="9bba3-114">The method allows the cipher suite to be negotiated for the purpose of data encryption.</span></span> <span data-ttu-id="9bba3-115">Windows Server 2008 unterstützt die folgenden [3DES-](/windows/desktop/SecAuthN/tls-cipher-suites)Verschlüsselungs Sammlungen:</span><span class="sxs-lookup"><span data-stu-id="9bba3-115">Windows Server 2008 supports the following 3DES [cipher suites](/windows/desktop/SecAuthN/tls-cipher-suites):</span></span>

-   <span data-ttu-id="9bba3-116">TLS \_ RSA \_ mit \_ 3DES \_ Ede \_ CBC \_ SHA (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="9bba3-116">TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="9bba3-117">TLS \_ dhe \_ DSS \_ with \_ 3DES \_ Ede \_ CBC \_ SHA (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="9bba3-117">TLS\_DHE\_DSS\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="9bba3-118">SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ mit \_ MD5 (SSL 2 bei Aktivierung)</span><span class="sxs-lookup"><span data-stu-id="9bba3-118">SSL\_CK\_DES\_192\_EDE3\_CBC\_WITH\_MD5 (SSL 2 if enabled)</span></span>

<span data-ttu-id="9bba3-119">Weitere Informationen zum TLS 1,0-Sicherheitsprotokoll finden Sie unter [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span><span class="sxs-lookup"><span data-stu-id="9bba3-119">For more information about the TLS 1.0 security protocol, see [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eappropmutualauth**</span><span class="sxs-lookup"><span data-stu-id="9bba3-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-121">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9bba3-121">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-122">Die-Methode stellt einen Austausch bereit, in dem der Authentifikator den Peer authentifiziert und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="9bba3-122">The method provides an exchange, in which the authenticator authenticates the peer and vice versa.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eappropintegrity**</span><span class="sxs-lookup"><span data-stu-id="9bba3-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-124">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9bba3-124">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-125">Die-Methode bietet Daten Ursprungs Authentifizierung und Schutz vor nicht autorisierten Änderungen von Informationen für EAP-Pakete, einschließlich EAP-Anforderungen und-Antworten.</span><span class="sxs-lookup"><span data-stu-id="9bba3-125">The method provides data origin authentication and protection against unauthorized modification of information for EAP packets, including EAP requests and responses.</span></span> <span data-ttu-id="9bba3-126">Beim Erstellen dieses Anspruchs muss in einer Methoden Spezifikation die geschützten EAP-Pakete und geschützten Felder in EAP-Paketen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9bba3-126">When making this claim, a method specification must specify the protected EAP packets and protected fields within EAP packets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eappropreplayprotection**</span><span class="sxs-lookup"><span data-stu-id="9bba3-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-128">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9bba3-128">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-129">Die-Methode kann vor der Wiedergabe einer EAP-Methode oder Ihrer Nachrichten schützen.</span><span class="sxs-lookup"><span data-stu-id="9bba3-129">The method can protect against replay of an EAP method or its messages.</span></span> <span data-ttu-id="9bba3-130">Erfolgs-und Fehler Ergebnis Hinweise können nicht wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9bba3-130">Success and failure result indications cannot be replayed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eappropvertraulichkeit**</span><span class="sxs-lookup"><span data-stu-id="9bba3-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9bba3-132">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-133">Die-Methode kann EAP-Nachrichten verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="9bba3-133">The method can encrypt EAP messages.</span></span> <span data-ttu-id="9bba3-134">EAP-Anforderungen, EAP-Antworten, Erfolgs Ergebnis Hinweise und Fehler Ergebnis Hinweise werden verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9bba3-134">EAP requests, EAP responses, success result indications, and failure result indications are encrypted.</span></span> <span data-ttu-id="9bba3-135">Eine Methode, die diesen Anspruch macht, muss Identitätsschutz unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9bba3-135">A method making this claim must support identity protection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eappropkeyderivations**</span><span class="sxs-lookup"><span data-stu-id="9bba3-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-137">0x00000020</span><span class="sxs-lookup"><span data-stu-id="9bba3-137">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-138">Die-Methode kann exportier bares Schlüsselmaterial ableiten, z. b. den Master Sitzungsschlüssel (Master Session Key, MSK) und den erweiterten Master Sitzungsschlüssel (emsk).</span><span class="sxs-lookup"><span data-stu-id="9bba3-138">The method can derive exportable keying material, such as the Master Session Key (MSK) and the Extended Master Session Key (EMSK).</span></span> <span data-ttu-id="9bba3-139">Der MSK wird nur zur weiteren Schlüssel Ableitung verwendet, nicht direkt zum Schutz der EAP-Konversation oder der nachfolgenden Daten.</span><span class="sxs-lookup"><span data-stu-id="9bba3-139">The MSK is used only for further key derivation, not directly for protection of the EAP conversation or subsequent data.</span></span> <span data-ttu-id="9bba3-140">Die Verwendung von emsk ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="9bba3-140">Use of the EMSK is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span><span class="sxs-lookup"><span data-stu-id="9bba3-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="9bba3-142">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-143">Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 64 Bits.</span><span class="sxs-lookup"><span data-stu-id="9bba3-143">The minimum key length supported by the EAP method is 64 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span><span class="sxs-lookup"><span data-stu-id="9bba3-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-145">0x00000080</span><span class="sxs-lookup"><span data-stu-id="9bba3-145">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-146">Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 128 Bits.</span><span class="sxs-lookup"><span data-stu-id="9bba3-146">The minimum key length supported by the EAP method is 128 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span><span class="sxs-lookup"><span data-stu-id="9bba3-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-148">0x00000100</span><span class="sxs-lookup"><span data-stu-id="9bba3-148">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-149">Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 256 Bits.</span><span class="sxs-lookup"><span data-stu-id="9bba3-149">The minimum key length supported by the EAP method is 256 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span><span class="sxs-lookup"><span data-stu-id="9bba3-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-151">0x00000200</span><span class="sxs-lookup"><span data-stu-id="9bba3-151">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-152">Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 512 Bits.</span><span class="sxs-lookup"><span data-stu-id="9bba3-152">The minimum key length supported by the EAP method is 512 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span><span class="sxs-lookup"><span data-stu-id="9bba3-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-154">0x00000400</span><span class="sxs-lookup"><span data-stu-id="9bba3-154">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-155">Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 1024 Bits.</span><span class="sxs-lookup"><span data-stu-id="9bba3-155">The minimum key length supported by the EAP method is 1024 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eappropdidaktitionaryangreiresistance**</span><span class="sxs-lookup"><span data-stu-id="9bba3-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-157">0x00000800</span><span class="sxs-lookup"><span data-stu-id="9bba3-157">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-158">Die-Methode lässt keinen Offline Angriff zu, der einen Arbeits Faktor basierend auf der Anzahl der Kenn Wörter im Wörterbuch eines Angreifers hat.</span><span class="sxs-lookup"><span data-stu-id="9bba3-158">The method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span> <span data-ttu-id="9bba3-159">Wenn die Kenn Wort Authentifizierung verwendet wird, werden Kenn Wörter im Allgemeinen aus einer kleinen Gruppe ausgewählt (im Vergleich zu einem Satz von N-Bit-Schlüsseln), was sich auf Wörterbuchangriffe betrifft.</span><span class="sxs-lookup"><span data-stu-id="9bba3-159">Where password authentication is used, passwords are commonly selected from a small set (as compared to a set of N-bit keys), which raises a concern about dictionary attacks.</span></span> <span data-ttu-id="9bba3-160">Eine Methode kann als Schutz vor Wörterbuchangriffen bezeichnet werden, wenn die Methode bei Verwendung eines Kennworts als geheimer Schlüssel keinen Offline Angriff zulässt, der über einen Arbeits Faktor auf der Grundlage der Anzahl der Kenn Wörter im Wörterbuch eines Angreifers verfügt.</span><span class="sxs-lookup"><span data-stu-id="9bba3-160">A method may be said to provide protection against dictionary attacks if, when it uses a password as a secret, the method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eappropfastreconnect**</span><span class="sxs-lookup"><span data-stu-id="9bba3-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-162">0x00001000</span><span class="sxs-lookup"><span data-stu-id="9bba3-162">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-163">Die-Methode hat die Möglichkeit, in dem Fall, in dem bereits eine Sicherheits Zuordnung eingerichtet wurde, eine neue oder aktualisierte Sicherheits Zuordnung zu erstellen, die effizienter oder in einer geringeren Anzahl von Roundtrips ist.</span><span class="sxs-lookup"><span data-stu-id="9bba3-163">The method has the ability, in the case where a security association has been previously established, to create a new or refreshed security association more efficiently or in a smaller number of round-trips.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eappropcryptobinding**</span><span class="sxs-lookup"><span data-stu-id="9bba3-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-165">0x00002000</span><span class="sxs-lookup"><span data-stu-id="9bba3-165">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-166">Die-Methode veranschaulicht den EAP-Server, dass eine einzelne Entität als EAP-Peer für alle Methoden, die innerhalb einer Tunnel Methode ausgeführt werden, agiert hat.</span><span class="sxs-lookup"><span data-stu-id="9bba3-166">The method demonstrates to the EAP server that a single entity has acted as the EAP peer for all methods executed within a tunnel method.</span></span> <span data-ttu-id="9bba3-167">Die Bindung kann auch bedeuten, dass der EAP-Server dem Peer zeigt, dass eine einzelne Entität als EAP-Server für alle Methoden, die innerhalb einer Tunnel Methode ausgeführt wurden, agiert hat.</span><span class="sxs-lookup"><span data-stu-id="9bba3-167">Binding may also imply that the EAP server demonstrates to the peer that a single entity has acted as the EAP server for all methods executed within a tunnel method.</span></span> <span data-ttu-id="9bba3-168">Wenn Sie ordnungsgemäß ausgeführt wird, dient die Bindung zur Abwehr von man-in-the-Middle-Sicherheitsrisiken.</span><span class="sxs-lookup"><span data-stu-id="9bba3-168">If executed correctly, binding serves to mitigate man-in-the-middle vulnerabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eappropsessionindependence**</span><span class="sxs-lookup"><span data-stu-id="9bba3-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-170">0x00004000</span><span class="sxs-lookup"><span data-stu-id="9bba3-170">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-171">Die-Methode veranschaulicht, dass durch passive Angriffe (z. b. die Erfassung der EAP-Konversation) oder aktive Angriffe (einschließlich Kompromittierung von MSK oder emsk) weder nachfolgende noch vorherige msks oder EMS gefährdet werden.</span><span class="sxs-lookup"><span data-stu-id="9bba3-171">The method demonstrates that passive attacks (such as capture of the EAP conversation) or active attacks (including compromise of the MSK or EMSK) do not compromise subsequent or prior MSKs or EMSKs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eappropfragmentierung**</span><span class="sxs-lookup"><span data-stu-id="9bba3-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-173">0x00008000</span><span class="sxs-lookup"><span data-stu-id="9bba3-173">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-174">Die-Methode kann Fragmentierung unterstützen und neu zuweisen, wenn EAP-Pakete die Mindestanzahl der MTU (maximale Übertragungseinheit) von 1020 Oktette überschreiten.</span><span class="sxs-lookup"><span data-stu-id="9bba3-174">The method can support fragmentation and reassembly if EAP packets exceed the minimum MTU (maximum transmission unit) of 1020 octets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eappropchannelbinding**</span><span class="sxs-lookup"><span data-stu-id="9bba3-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-176">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9bba3-176">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-177">Die-Methode kann Integritäts geschützte Kanaleigenschaften, z. b. Endpunkt Bezeichner, kommunizieren. Diese können mit Werten verglichen werden, die über Out-of-Band-Mechanismen kommuniziert werden, z. b. [Authentifizierung, Autorisierung und Kontoführung](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) oder das Protokoll der niedrigeren Ebene.</span><span class="sxs-lookup"><span data-stu-id="9bba3-177">The method can communicate integrity-protected channel properties, such as endpoint identifiers, which can be compared to values communicated using out of band mechanisms - such as an [Authentication, Authorization, and Accounting](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) or the lower layer protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eappropnap**</span><span class="sxs-lookup"><span data-stu-id="9bba3-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="9bba3-179">0x00020000</span><span class="sxs-lookup"><span data-stu-id="9bba3-179">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-180">Die-Methode unterstützt den Netzwerk Zugriffsschutz (NAP).</span><span class="sxs-lookup"><span data-stu-id="9bba3-180">The method supports Network Access Protection (NAP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eappropstandalone**</span><span class="sxs-lookup"><span data-stu-id="9bba3-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-182">0x00040000</span><span class="sxs-lookup"><span data-stu-id="9bba3-182">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-183">Die-Methode kann auf einem eigenständigen Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bba3-183">The method can be used on a standalone machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eappropmppeer Encryption**</span><span class="sxs-lookup"><span data-stu-id="9bba3-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="9bba3-185">0x00080000</span><span class="sxs-lookup"><span data-stu-id="9bba3-185">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-186">Die-Methode unterstützt die Protokoll Verschlüsselung von [Microsoft Point-to-Point-Verschlüsselung (MPPE)](https://go.microsoft.com/fwlink/p/?linkid=83915) .</span><span class="sxs-lookup"><span data-stu-id="9bba3-186">The method supports [Microsoft Point-to-Point Encryption (MPPE) protocol](https://go.microsoft.com/fwlink/p/?linkid=83915) encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapproptunnelmethod**</span><span class="sxs-lookup"><span data-stu-id="9bba3-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-188">0x00100000</span><span class="sxs-lookup"><span data-stu-id="9bba3-188">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-189">Die-Methode unterstützt Tunnelung von anderen EAP-Methoden.</span><span class="sxs-lookup"><span data-stu-id="9bba3-189">The method supports tunneling of other EAP methods.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eappropsupportsconfig**</span><span class="sxs-lookup"><span data-stu-id="9bba3-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-191">0x00200000</span><span class="sxs-lookup"><span data-stu-id="9bba3-191">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-192">Die-Methode unterstützt konfigurierbare Eigenschaften und verfügt über eine Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="9bba3-192">The method supports configurable properties, and has a user interface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eappropcertifiedmethod**</span><span class="sxs-lookup"><span data-stu-id="9bba3-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-194">0x00400000</span><span class="sxs-lookup"><span data-stu-id="9bba3-194">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-195">Die Methode wurde vom EAP-Zertifizierungsprogramm zertifiziert.</span><span class="sxs-lookup"><span data-stu-id="9bba3-195">The method was certified by the EAP Certification Program.</span></span> <span data-ttu-id="9bba3-196">Dieses Bit sollte nur von EAP-Methoden gesendet werden, die die Zertifizierung überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="9bba3-196">This bit should only be sent by EAP methods that have passed certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eappropmachineauth**</span><span class="sxs-lookup"><span data-stu-id="9bba3-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-198">0x01000000</span><span class="sxs-lookup"><span data-stu-id="9bba3-198">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-199">Windows 7 oder höher: die-Methode kann verwendet werden, um einen Computer in einem Netzwerk mithilfe der Computer Anmelde Informationen zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="9bba3-199">Windows 7 or later: The method can be used to authenticate a machine on to a network using the machines credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eappropuserauth**</span><span class="sxs-lookup"><span data-stu-id="9bba3-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-201">0x02000000</span><span class="sxs-lookup"><span data-stu-id="9bba3-201">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-202">Windows 7 oder höher: die-Methode kann verwendet werden, um einen Benutzer bei einem Netzwerk mithilfe der Anmelde Informationen des Benutzers zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="9bba3-202">Windows 7 or later: The method can be used to authenticate a user on to a network using the users credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eappropidentityprivacy**</span><span class="sxs-lookup"><span data-stu-id="9bba3-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-204">0x04000000</span><span class="sxs-lookup"><span data-stu-id="9bba3-204">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-205">Windows 7 oder höher: die-Methode unterstützt das Senden der Benutzeridentität in einem geschützten Kanal.</span><span class="sxs-lookup"><span data-stu-id="9bba3-205">Windows 7 or later: The method supports sending the user identity in a protected channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eappropmethodchaining**</span><span class="sxs-lookup"><span data-stu-id="9bba3-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-207">0x08000000</span><span class="sxs-lookup"><span data-stu-id="9bba3-207">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-208">Windows 7 oder höher: bei der Methode handelt es sich um eine getunnelte Methode, die die EAP-Methoden Verkettung innerhalb des Tunnels unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9bba3-208">Windows 7 or later: The method is a tunnelled method and supports EAP method chaining within the tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eappropsharedstateäquivalenz**</span><span class="sxs-lookup"><span data-stu-id="9bba3-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-210">0x10000000</span><span class="sxs-lookup"><span data-stu-id="9bba3-210">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-211">Windows 7 oder höher: die Methode unterstützt die Äquivalenz von freigegebenen Zuständen, wie in [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455)definiert.</span><span class="sxs-lookup"><span data-stu-id="9bba3-211">Windows 7 or later: The method supports shared state equivalence as defined in [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bba3-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapprobewahrt**</span><span class="sxs-lookup"><span data-stu-id="9bba3-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bba3-213">0x80000000</span><span class="sxs-lookup"><span data-stu-id="9bba3-213">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="9bba3-214">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="9bba3-214">Reserved.</span></span> <span data-ttu-id="9bba3-215">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bba3-215">Not used.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bba3-216">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bba3-216">Requirements</span></span>



| <span data-ttu-id="9bba3-217">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bba3-217">Requirement</span></span> | <span data-ttu-id="9bba3-218">Wert</span><span class="sxs-lookup"><span data-stu-id="9bba3-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bba3-219">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9bba3-219">Minimum supported client</span></span><br/> | <span data-ttu-id="9bba3-220">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bba3-220">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9bba3-221">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9bba3-221">Minimum supported server</span></span><br/> | <span data-ttu-id="9bba3-222">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bba3-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9bba3-223">Header</span><span class="sxs-lookup"><span data-stu-id="9bba3-223">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bba3-224"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bba3-224"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bba3-225">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bba3-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bba3-226">Registrierungsschlüssel für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="9bba3-226">Registry Keys for EAP Methods</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="9bba3-227">Allgemeine EAPHost-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9bba3-227">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

