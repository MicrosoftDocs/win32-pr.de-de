---
description: Enthält Definitionen von Sicherheits Begriffen, die mit dem Buchstaben L beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 65dd9a04-fc7c-4179-95ff-dac7dad4668f
title: L (Sicherheits Glossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33ee054c2bcf414ef289cc381ac13ef970da6dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866632"
---
# <a name="l-security-glossary"></a>L (Sicherheits Glossar)

[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) L [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ldap_gly"></span><span id="_SECURITY_LDAP_GLY"></span>**Standardi**
</dt> <dd>

Siehe *Lightweight Directory Access Protocol*

</dd> <dt>

<span id="_security_lightweight_directory_access_protocol_gly"></span><span id="_SECURITY_LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL_GLY"></span>**Lightweight Directory Access-Protokoll**
</dt> <dd>

Eine leichter implementierte Teilmenge des X. 500 DAP-Standards für Verzeichnisdienste.

</dd> <dt>

<span id="_security_little_endian_gly"></span><span id="_SECURITY_LITTLE_ENDIAN_GLY"></span>**Little-d**
</dt> <dd>

Ein Arbeitsspeicher-oder Datenformat, in dem das am wenigsten signifikante Byte an der unteren Adresse gespeichert wird oder zuerst eingeht.

Siehe auch [*Big-erdian*](b-gly.md).

</dd> <dt>

<span id="_security_locally_unique_identifier_gly"></span><span id="_SECURITY_LOCALLY_UNIQUE_IDENTIFIER_GLY"></span>**lokal eindeutiger Bezeichner**
</dt> <dd>

LUID Ein 64-Bit-Wert, der garantiert eindeutig auf dem Betriebssystem ist, von dem es generiert wurde, bis das System neu gestartet wird.

</dd> <dt>

<span id="_security_local_registration_authority_gly"></span><span id="_SECURITY_LOCAL_REGISTRATION_AUTHORITY_GLY"></span>**lokale Registrierungsstelle**
</dt> <dd>

Endgültig Ein Vermittler zwischen einem Verleger und einer [*Zertifizierungsstelle (Certification Authority*](c-gly.md) , ca). Die LRA kann z. b. die Anmelde Informationen eines Herausgebers vor dem Senden an die Zertifizierungsstelle überprüfen.

</dd> <dt>

<span id="_security_local_security_authority_gly"></span><span id="_SECURITY_LOCAL_SECURITY_AUTHORITY_GLY"></span>**Lokale Sicherheits Autorität**
</dt> <dd>

LSA Ein geschütztes Subsystem, das Benutzer auf dem lokalen System authentifiziert und protokolliert. LSA verwaltet auch Informationen zu allen Aspekten der lokalen Sicherheit auf einem System, die zusammenfassend auch als lokale Sicherheitsrichtlinie des Systems bezeichnet werden.

</dd> <dt>

<span id="_security_logical_store_gly"></span><span id="_SECURITY_LOGICAL_STORE_GLY"></span>**Logischer Speicher**
</dt> <dd>

Siehe [*Virtual Store*](v-gly.md).

</dd> <dt>

<span id="_security_logon_data_gly"></span><span id="_SECURITY_LOGON_DATA_GLY"></span>**Anmeldedaten**
</dt> <dd>

Informationen, die dem System von einem [*Sicherheits Prinzipal*](s-gly.md) für die Authentifizierung angezeigt werden.

</dd> <dt>

<span id="_security_logon_identifier_gly"></span><span id="_SECURITY_LOGON_IDENTIFIER_GLY"></span>**Anmelde Bezeichner**
</dt> <dd>

Eine LUID, die eine *Anmelde Sitzung* identifiziert. Eine Anmelde-ID ist gültig, bis der Benutzer sich abmeldet. Eine Anmelde-ID ist eindeutig, während der Computer ausgeführt wird. keine andere Anmelde Sitzung hat dieselbe Anmelde-ID. Der Satz möglicher Anmelde-IDs wird jedoch zurückgesetzt, wenn der Computer gestartet wird. Um die Anmelde-ID aus einem [*Zugriffs Token*](a-gly.md)abzurufen, rufen Sie die **GetTokenInformation** -Funktion für tokenstatistics auf. die Anmelde-ID befindet sich im Member **authenticationid** .

</dd> <dt>

<span id="_security_logon_session_gly"></span><span id="_SECURITY_LOGON_SESSION_GLY"></span>**Anmelde Sitzung**
</dt> <dd>

Eine Anmelde Sitzung beginnt, wenn sich ein Benutzer an einem Computer anmeldet. Alle Prozesse in einer Anmelde Sitzung haben das gleiche primäre [*Zugriffs Token*](a-gly.md). Das Zugriffs Token enthält Informationen zum Sicherheitskontext der Anmelde Sitzung, einschließlich der SID des Benutzers, des *Anmelde Bezeichners* und der Anmelde- *sid*.

</dd> <dt>

<span id="_security_logon_sid_gly"></span><span id="_SECURITY_LOGON_SID_GLY"></span>**Anmelde-SID**
</dt> <dd>

Eine [*Sicherheits*](s-gly.md) -ID (SID), die eine *Anmelde Sitzung* identifiziert. Sie können die Anmelde-SID in einer [*DACL*](d-gly.md) verwenden, um den Zugriff während einer Anmelde Sitzung zu steuern. Eine Anmelde-SID ist gültig, bis der Benutzer sich abmeldet. Eine Anmelde-SID ist eindeutig, während der Computer ausgeführt wird. keine andere Anmelde Sitzung hat dieselbe Anmelde-SID. Der Satz möglicher Anmelde-SIDs wird jedoch zurückgesetzt, wenn der Computer gestartet wird. Rufen Sie die **GetTokenInformation** -Funktion für tokenGroups auf, um die Anmelde-SID von einem [*Zugriffs Token*](a-gly.md)abzurufen.

</dd> <dt>

<span id="_security_low_level_message_functions_gly"></span><span id="_SECURITY_LOW_LEVEL_MESSAGE_FUNCTIONS_GLY"></span>**Nachrichten Funktionen auf niedriger Ebene**
</dt> <dd>

Nachrichten Verwaltungsfunktionen, die auf einer höheren Ebene als die grundlegenden Kryptografiefunktionen funktionieren. Diese Funktionen bieten Funktionen zum Codieren von Daten für die Übertragung und zum Decodieren von Daten, die empfangen wurden. Nachrichten Funktionen auf niedriger Ebene bieten mehr Flexibilität als vereinfachte Nachrichten Funktionen, erfordern jedoch mehr Funktionsaufrufe.

Siehe auch [*vereinfachte Nachrichten Funktionen*](s-gly.md).

</dd> <dt>

<span id="_security_lsa_gly"></span><span id="_SECURITY_LSA_GLY"></span>**LSA**
</dt> <dd>

Siehe *Lokale Sicherheits Autorität*.

</dd> <dt>

<span id="_security_luid_gly"></span><span id="_SECURITY_LUID_GLY"></span>**LUID**
</dt> <dd>

Siehe *lokal eindeutiger Bezeichner*.

</dd> </dl>

 

 



