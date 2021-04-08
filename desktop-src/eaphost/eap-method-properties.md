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
# <a name="eap-method-properties"></a>Eigenschaften der EAP-Methode

Wird von Supplicants und Authentifikatoren verwendet, um die EAP-Methoden zu ermitteln, die mit einem bestimmten Supplicant oder Authentifikator verwendet werden sollen. Methoden Eigenschaften geben auch die Konfiguration einer Methode an.

Beispielsweise erfordert der [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Supplicant möglicherweise, dass Methoden bestimmte Eigenschaften für die Verwendung mit dem [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Supplicant aufweisen. Das Schlüsselmaterial ist beispielsweise eine Anforderung.

Die Eigenschaften werden aufgelistet, die von EAP-Methoden unterstützt werden. Eigenschaften werden als Registrierungsschlüssel Werte gespeichert. Weitere Informationen finden Sie im Abschnitt zum Registrierungsschlüssel der EAP-Peer Methode DLL des Themas [Registrierungs Konfiguration für EAP-Methoden.](registry-keys-for-eap-methods.md)

<dl> <dt>

<span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eappropciphersuitenegotiation**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Die-Methode ermöglicht das Aushandeln der Verschlüsselungs Sammlung für den Zweck der Datenverschlüsselung. Windows Server 2008 unterstützt die folgenden [3DES-](/windows/desktop/SecAuthN/tls-cipher-suites)Verschlüsselungs Sammlungen:

-   TLS \_ RSA \_ mit \_ 3DES \_ Ede \_ CBC \_ SHA (TLS & SSL 3)
-   TLS \_ dhe \_ DSS \_ with \_ 3DES \_ Ede \_ CBC \_ SHA (TLS & SSL 3)
-   SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ mit \_ MD5 (SSL 2 bei Aktivierung)

Weitere Informationen zum TLS 1,0-Sicherheitsprotokoll finden Sie unter [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).


</dt> </dl> </dd> <dt>

<span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eappropmutualauth**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Die-Methode stellt einen Austausch bereit, in dem der Authentifikator den Peer authentifiziert und umgekehrt.


</dt> </dl> </dd> <dt>

<span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eappropintegrity**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Die-Methode bietet Daten Ursprungs Authentifizierung und Schutz vor nicht autorisierten Änderungen von Informationen für EAP-Pakete, einschließlich EAP-Anforderungen und-Antworten. Beim Erstellen dieses Anspruchs muss in einer Methoden Spezifikation die geschützten EAP-Pakete und geschützten Felder in EAP-Paketen angegeben werden.


</dt> </dl> </dd> <dt>

<span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eappropreplayprotection**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Die-Methode kann vor der Wiedergabe einer EAP-Methode oder Ihrer Nachrichten schützen. Erfolgs-und Fehler Ergebnis Hinweise können nicht wiedergegeben werden.


</dt> </dl> </dd> <dt>

<span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eappropvertraulichkeit**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Die-Methode kann EAP-Nachrichten verschlüsseln. EAP-Anforderungen, EAP-Antworten, Erfolgs Ergebnis Hinweise und Fehler Ergebnis Hinweise werden verschlüsselt. Eine Methode, die diesen Anspruch macht, muss Identitätsschutz unterstützen.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eappropkeyderivations**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Die-Methode kann exportier bares Schlüsselmaterial ableiten, z. b. den Master Sitzungsschlüssel (Master Session Key, MSK) und den erweiterten Master Sitzungsschlüssel (emsk). Der MSK wird nur zur weiteren Schlüssel Ableitung verwendet, nicht direkt zum Schutz der EAP-Konversation oder der nachfolgenden Daten. Die Verwendung von emsk ist reserviert.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 64 Bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 128 Bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 256 Bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 512 Bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Die minimale Schlüssellänge, die von der EAP-Methode unterstützt wird, beträgt 1024 Bits.


</dt> </dl> </dd> <dt>

<span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eappropdidaktitionaryangreiresistance**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Die-Methode lässt keinen Offline Angriff zu, der einen Arbeits Faktor basierend auf der Anzahl der Kenn Wörter im Wörterbuch eines Angreifers hat. Wenn die Kenn Wort Authentifizierung verwendet wird, werden Kenn Wörter im Allgemeinen aus einer kleinen Gruppe ausgewählt (im Vergleich zu einem Satz von N-Bit-Schlüsseln), was sich auf Wörterbuchangriffe betrifft. Eine Methode kann als Schutz vor Wörterbuchangriffen bezeichnet werden, wenn die Methode bei Verwendung eines Kennworts als geheimer Schlüssel keinen Offline Angriff zulässt, der über einen Arbeits Faktor auf der Grundlage der Anzahl der Kenn Wörter im Wörterbuch eines Angreifers verfügt.


</dt> </dl> </dd> <dt>

<span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eappropfastreconnect**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Die-Methode hat die Möglichkeit, in dem Fall, in dem bereits eine Sicherheits Zuordnung eingerichtet wurde, eine neue oder aktualisierte Sicherheits Zuordnung zu erstellen, die effizienter oder in einer geringeren Anzahl von Roundtrips ist.


</dt> </dl> </dd> <dt>

<span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eappropcryptobinding**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Die-Methode veranschaulicht den EAP-Server, dass eine einzelne Entität als EAP-Peer für alle Methoden, die innerhalb einer Tunnel Methode ausgeführt werden, agiert hat. Die Bindung kann auch bedeuten, dass der EAP-Server dem Peer zeigt, dass eine einzelne Entität als EAP-Server für alle Methoden, die innerhalb einer Tunnel Methode ausgeführt wurden, agiert hat. Wenn Sie ordnungsgemäß ausgeführt wird, dient die Bindung zur Abwehr von man-in-the-Middle-Sicherheitsrisiken.


</dt> </dl> </dd> <dt>

<span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eappropsessionindependence**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Die-Methode veranschaulicht, dass durch passive Angriffe (z. b. die Erfassung der EAP-Konversation) oder aktive Angriffe (einschließlich Kompromittierung von MSK oder emsk) weder nachfolgende noch vorherige msks oder EMS gefährdet werden.


</dt> </dl> </dd> <dt>

<span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eappropfragmentierung**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Die-Methode kann Fragmentierung unterstützen und neu zuweisen, wenn EAP-Pakete die Mindestanzahl der MTU (maximale Übertragungseinheit) von 1020 Oktette überschreiten.


</dt> </dl> </dd> <dt>

<span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eappropchannelbinding**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Die-Methode kann Integritäts geschützte Kanaleigenschaften, z. b. Endpunkt Bezeichner, kommunizieren. Diese können mit Werten verglichen werden, die über Out-of-Band-Mechanismen kommuniziert werden, z. b. [Authentifizierung, Autorisierung und Kontoführung](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) oder das Protokoll der niedrigeren Ebene.


</dt> </dl> </dd> <dt>

<span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eappropnap**
</dt> <dd> <dl> <dt>

 0x00020000
</dt> <dt>



Die-Methode unterstützt den Netzwerk Zugriffsschutz (NAP).


</dt> </dl> </dd> <dt>

<span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eappropstandalone**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Die-Methode kann auf einem eigenständigen Computer verwendet werden.


</dt> </dl> </dd> <dt>

<span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eappropmppeer Encryption**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Die-Methode unterstützt die Protokoll Verschlüsselung von [Microsoft Point-to-Point-Verschlüsselung (MPPE)](https://go.microsoft.com/fwlink/p/?linkid=83915) .


</dt> </dl> </dd> <dt>

<span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapproptunnelmethod**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Die-Methode unterstützt Tunnelung von anderen EAP-Methoden.


</dt> </dl> </dd> <dt>

<span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eappropsupportsconfig**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Die-Methode unterstützt konfigurierbare Eigenschaften und verfügt über eine Benutzeroberfläche.


</dt> </dl> </dd> <dt>

<span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eappropcertifiedmethod**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Die Methode wurde vom EAP-Zertifizierungsprogramm zertifiziert. Dieses Bit sollte nur von EAP-Methoden gesendet werden, die die Zertifizierung überschritten haben.


</dt> </dl> </dd> <dt>

<span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eappropmachineauth**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Windows 7 oder höher: die-Methode kann verwendet werden, um einen Computer in einem Netzwerk mithilfe der Computer Anmelde Informationen zu authentifizieren.


</dt> </dl> </dd> <dt>

<span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eappropuserauth**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Windows 7 oder höher: die-Methode kann verwendet werden, um einen Benutzer bei einem Netzwerk mithilfe der Anmelde Informationen des Benutzers zu authentifizieren.


</dt> </dl> </dd> <dt>

<span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eappropidentityprivacy**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Windows 7 oder höher: die-Methode unterstützt das Senden der Benutzeridentität in einem geschützten Kanal.


</dt> </dl> </dd> <dt>

<span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eappropmethodchaining**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Windows 7 oder höher: bei der Methode handelt es sich um eine getunnelte Methode, die die EAP-Methoden Verkettung innerhalb des Tunnels unterstützt.


</dt> </dl> </dd> <dt>

<span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eappropsharedstateäquivalenz**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Windows 7 oder höher: die Methode unterstützt die Äquivalenz von freigegebenen Zuständen, wie in [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455)definiert.


</dt> </dl> </dd> <dt>

<span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapprobewahrt**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Reserviert. Nicht verwendet.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Registrierungsschlüssel für EAP-Methoden](registry-keys-for-eap-methods.md)
</dt> <dt>

[Allgemeine EAPHost-Konstanten](common-eap-host-error-constants.md)
</dt> </dl>

