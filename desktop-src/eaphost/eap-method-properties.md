---
title: EAP-Methodeneigenschaften (Eaptypes.h)
description: Wird von Unterstützungs- und Authentifikatoren verwendet, um die EAP-Methoden zu bestimmen, die mit einer bestimmten Unterstützung oder einem Authentifikator verwendet werden sollen. Methodeneigenschaften geben auch die Konfiguration einer Methode an.
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
ms.openlocfilehash: c88c31d77b666e377cbd1911cde8b5df63d8f5c2fc750cd03a701b03af5b60ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094400"
---
# <a name="eap-method-properties"></a>Eigenschaften der EAP-Methode

Wird von Unterstützungs- und Authentifikatoren verwendet, um die EAP-Methoden zu bestimmen, die mit einer bestimmten Unterstützung oder einem Authentifikator verwendet werden sollen. Methodeneigenschaften geben auch die Konfiguration einer Methode an.

Beispielsweise erfordert die [802.1X-Supplizierung](/previous-versions/windows/embedded/ms890287(v=msdn.10)) möglicherweise, dass Methoden bestimmte Eigenschaften für die Verwendung mit der [802.1X-Supplikation](/previous-versions/windows/embedded/ms890287(v=msdn.10)) aufweisen. Schlüsselmaterial ist z. B. eine Anforderung.

Die von EAP-Methoden unterstützten Eigenschaften werden aufgelistet. Eigenschaften werden als Registrierungsschlüsselwerte gespeichert. Weitere Informationen finden Sie im Abschnitt EAP-Peermethoden-DLL-Registrierungsschlüssel des [Themas Registrierungskonfiguration für EAP-Methoden.](registry-keys-for-eap-methods.md)

<dl> <dt>

<span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Mit der -Methode kann die Verschlüsselungssammlung zum Zweck der Datenverschlüsselung ausgehandelt werden. Windows Server 2008 unterstützt die folgenden [3DES-Verschlüsselungssammlungen:](/windows/desktop/SecAuthN/tls-cipher-suites)

-   TLS \_ RSA \_ MIT \_ 3DES \_ EDE \_ CBC SHA \_ (TLS & SSL 3)
-   TLS \_ DHE \_ DSS \_ MIT \_ 3DES \_ EDE \_ CBC SHA \_ (TLS & SSL 3)
-   SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC WITH \_ \_ MD5 (SSL 2, falls aktiviert)

Weitere Informationen zum TLS 1.0-Sicherheitsprotokoll finden Sie unter [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).


</dt> </dl> </dd> <dt>

<span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Die -Methode stellt einen Austausch bereit, bei dem der Authentifikator den Peer authentifiziert und umgekehrt.


</dt> </dl> </dd> <dt>

<span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Die -Methode bietet datenursprungsbasierte Authentifizierung und Schutz vor nicht autorisierten Änderungen von Informationen für EAP-Pakete, einschließlich EAP-Anforderungen und -Antworten. Beim Erstellen dieses Anspruchs muss eine Methodenspezifikation die geschützten EAP-Pakete und geschützten Felder in EAP-Paketen angeben.


</dt> </dl> </dd> <dt>

<span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Die -Methode kann vor der Wiedergabe einer EAP-Methode oder ihrer Nachrichten schützen. Erfolgs- und Fehlerergebnisanzeigen können nicht wiedergegeben werden.


</dt> </dl> </dd> <dt>

<span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Die -Methode kann EAP-Nachrichten verschlüsseln. EAP-Anforderungen, EAP-Antworten, Erfolgsergebnisanzeigen und Fehlerergebnisanzeigen werden verschlüsselt. Eine Methode, die diesen Anspruch stellt, muss identitätsschutz unterstützen.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Die -Methode kann exportierbares Schlüsselmaterial ableiten, z. B. den Mastersitzungsschlüssel (Master Session Key, MSK) und den erweiterten Mastersitzungsschlüssel (Extended Master Session Key, EMSK). Das MSK wird nur für die weitere Schlüsselableitung verwendet, nicht direkt zum Schutz der EAP-Konversation oder nachfolgender Daten. Die Verwendung des EMSK ist reserviert.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Die von der EAP-Methode unterstützte Mindestschlüssellänge beträgt 64 Bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Die von der EAP-Methode unterstützte Mindestschlüssellänge beträgt 128 Bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Die von der EAP-Methode unterstützte Mindestschlüssellänge beträgt 256 Bit.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Die von der EAP-Methode unterstützte Mindestschlüssellänge beträgt 512 Bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Die von der EAP-Methode unterstützte Mindestschlüssellänge beträgt 1024 Bits.


</dt> </dl> </dd> <dt>

<span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAngriffResistance**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Die -Methode lässt keinen Offlineangriff zu, der basierend auf der Anzahl der Kennwörter im Wörterbuch eines Angreifers einen Arbeitsfaktor hat. Wenn die Kennwortauthentifizierung verwendet wird, werden Kennwörter häufig aus einer kleinen Gruppe ausgewählt (im Vergleich zu einem Satz von N-Bit-Schlüsseln), was zu Bedenken bei Wörterbuchangriffen führt. Eine Methode kann als Schutz vor Wörterbuchangriffen bezeichnet werden, wenn sie ein Kennwort als Geheimnis verwendet, lässt die Methode keinen Offlineangriff zu, der basierend auf der Anzahl von Kennwörtern im Wörterbuch eines Angreifers einen Arbeitsfaktor hat.


</dt> </dl> </dd> <dt>

<span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Die -Methode kann in fällen, in denen zuvor eine Sicherheitszuordnung eingerichtet wurde, eine neue oder aktualisierte Sicherheitszuordnung effizienter oder in einer kleineren Anzahl von Roundtrips erstellen.


</dt> </dl> </dd> <dt>

<span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Die -Methode zeigt dem EAP-Server, dass eine einzelne Entität als EAP-Peer für alle Methoden fungiert, die innerhalb einer Tunnelmethode ausgeführt werden. Die Bindung kann auch implizieren, dass der EAP-Server dem Peer zeigt, dass eine einzelne Entität als EAP-Server für alle Methoden fungiert, die innerhalb einer Tunnelmethode ausgeführt werden. Bei ordnungsgemäßer Ausführung dient die Bindung dazu, Man-in-the-Middle-Sicherheitsrisiken zu minimieren.


</dt> </dl> </dd> <dt>

<span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Die -Methode zeigt, dass passive Angriffe (z. B. die Erfassung der EAP-Konversation) oder aktive Angriffe (einschließlich kompromittieren des MSK oder EMSK) nachfolgende oder frühere MSKs oder EMSKs nicht gefährden.


</dt> </dl> </dd> <dt>

<span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Die -Methode kann Fragmentierung und Neuassembly unterstützen, wenn EAP-Pakete die minimale MTU (maximale Übertragungseinheit) von 1.020 Oktetten überschreiten.


</dt> </dl> </dd> <dt>

<span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Die -Methode kann integritätsgeschützte Kanaleigenschaften kommunizieren, z. B. Endpunktbezeichner, die mithilfe von Out-of-Band-Mechanismen wie [Authentifizierung, Autorisierung und Buchhaltung](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) oder dem Protokoll der unteren Ebene verglichen werden können.


</dt> </dl> </dd> <dt>

<span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**
</dt> <dd> <dl> <dt>

 0x00020000
</dt> <dt>



Die -Methode unterstützt Network Access Protection (NAP).


</dt> </dl> </dd> <dt>

<span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Die -Methode kann auf einem eigenständigen Computer verwendet werden.


</dt> </dl> </dd> <dt>

<span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Die -Methode unterstützt [die MPPE-Protokollverschlüsselung (Point-to-Point Encryption)](https://go.microsoft.com/fwlink/p/?linkid=83915) von Microsoft.


</dt> </dl> </dd> <dt>

<span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Die -Methode unterstützt das Tunneln anderer EAP-Methoden.


</dt> </dl> </dd> <dt>

<span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Die -Methode unterstützt konfigurierbare Eigenschaften und verfügt über eine Benutzeroberfläche.


</dt> </dl> </dd> <dt>

<span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Die Methode wurde vom EAP-Zertifizierungsprogramm zertifiziert. Dieses Bit sollte nur von EAP-Methoden gesendet werden, die die Zertifizierung bestanden haben.


</dt> </dl> </dd> <dt>

<span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Windows 7 oder höher: Die -Methode kann zum Authentifizieren eines Computers in einem Netzwerk mithilfe der Computeranmeldeinformationen verwendet werden.


</dt> </dl> </dd> <dt>

<span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Windows 7 oder höher: Die -Methode kann verwendet werden, um einen Benutzer mithilfe der Benutzeranmeldeinformationen bei einem Netzwerk zu authentifizieren.


</dt> </dl> </dd> <dt>

<span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Windows 7 oder höher: Die -Methode unterstützt das Senden der Benutzeridentität in einem geschützten Kanal.


</dt> </dl> </dd> <dt>

<span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Windows 7 oder höher: Die -Methode ist eine getunnelte Methode und unterstützt die EAP-Methodenkette innerhalb des Tunnels.


</dt> </dl> </dd> <dt>

<span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Windows 7 oder höher: Die -Methode unterstützt die Äquivalenz des gemeinsam genutzten Zustands, wie in [RFC 4017 definiert.](https://go.microsoft.com/fwlink/p/?linkid=90455)


</dt> </dl> </dd> <dt>

<span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Reserviert. Wird nicht verwendet.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Registrierungsschlüssel für EAP-Methoden](registry-keys-for-eap-methods.md)
</dt> <dt>

[Allgemeine EAPHost-Konstanten](common-eap-host-error-constants.md)
</dt> </dl>

