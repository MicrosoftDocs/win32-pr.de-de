---
description: Enthält Definitionen von Sicherheits Begriffen, die mit dem Buchstaben "M" beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4c4402e9-7455-4868-978f-3899a8fd86c1
title: M (Sicherheits Glossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63fc76d4b8b803d523c46012dcb10ed5380e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960126"
---
# <a name="m-security-glossary"></a>M (Sicherheits Glossar)

[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) M [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_mac_gly"></span><span id="_SECURITY_MAC_GLY"></span>**Mac**
</dt> <dd>

Siehe *Nachrichtenauthentifizierungscode*.

</dd> <dt>

<span id="_security_mac_key_gly"></span><span id="_SECURITY_MAC_KEY_GLY"></span>**Mac-Taste**
</dt> <dd>

Ein für [*SChannel*](s-gly.md) -Protokolle verwendeter Code Schlüssel für die Nachrichten Authentifizierung.

</dd> <dt>

<span id="_security_master_key_gly"></span><span id="_SECURITY_MASTER_KEY_GLY"></span>**Hauptschlüssel**
</dt> <dd>

Der Schlüssel, der vom Client und Server für die Erstellung aller Sitzungsschlüssel verwendet wird. Der Hauptschlüssel wird verwendet, um den Client Lese Schlüssel, den Client Schreib Schlüssel, den Schlüssel für den Server Lesevorgang und den Schlüssel für den Server Schreibvorgang zu generieren. Hauptschlüssel können als einfache Schlüsselblob exportiert werden.

</dd> <dt>

<span id="_security_md2_gly"></span><span id="_SECURITY_MD2_GLY"></span>**MD2**
</dt> <dd>

Der Name des CryptoAPI-Algorithmus für den MD2-Hash Algorithmus. Andere Hash Algorithmen sind *MD4*, *MD5* und [*SHA*](s-gly.md).

Siehe auch *MD2-Algorithmus*.

</dd> <dt>

<span id="_security_md2_algorithm_gly"></span><span id="_SECURITY_MD2_ALGORITHM_GLY"></span>**MD2-Algorithmus**
</dt> <dd>

MD2 Ein Hash Algorithmus, der einen 128-Bit-Hashwert erstellt. MD2 wurde für die Verwendung mit 8-Bit-Computern optimiert. CryptoAPI verweist auf diesen Algorithmus durch den Typ (calg \_ MD2), den Namen (Mac) und die Klasse (ALG- \_ Klassen \_ Hash). MD2 wurde von RSA Data Security, Inc. entwickelt.

Siehe auch *MD4-Algorithmus*, *MD5-Algorithmus*.

</dd> <dt>

<span id="_security_md4_gly"></span><span id="_SECURITY_MD4_GLY"></span>**MD4**
</dt> <dd>

Der Name des CryptoAPI-Algorithmus für den MD4-Hash Algorithmus. Andere Hash Algorithmen sind *MD2*, *MD5* und [*SHA*](s-gly.md).

Siehe *MD4-Algorithmus*.

</dd> <dt>

<span id="_security_md4_algorithm_gly"></span><span id="_SECURITY_MD4_ALGORITHM_GLY"></span>**MD4-Algorithmus**
</dt> <dd>

MD4 Ein Hash Algorithmus, der einen 128-Bit-Hashwert erstellt. MD4 wurde für 32-Bit-Computer optimiert. Sie wird jetzt als beschädigt eingestuft, da Konflikte zu schnell und einfach zu finden sind. MD4 wurde von RSA Data Security, Inc. entwickelt.

Siehe auch *MD2-Algorithmus*, *MD5-Algorithmus*.

</dd> <dt>

<span id="_security_md5_gly"></span><span id="_SECURITY_MD5_GLY"></span>**Benutzen**
</dt> <dd>

Der Name des CryptoAPI-Algorithmus für den MD5-Hash Algorithmus. Andere Hash Algorithmen sind *MD2*, *MD4* und [*SHA*](s-gly.md).

Siehe auch *MD5-Algorithmus*.

</dd> <dt>

<span id="_security_md5_algorithm_gly"></span><span id="_SECURITY_MD5_ALGORITHM_GLY"></span>**MD5-Algorithmus**
</dt> <dd>

Benutzen Ein Hash Algorithmus, der einen 128-Bit-Hashwert erstellt. MD5 wurde für 32-Bit-Computer optimiert. CryptoAPI verweist auf diesen Algorithmus durch den Algorithmusbezeichner (calg \_ MD5), den Namen (MD5) und die Klasse (ALG- \_ Klassen \_ Hash). MD5 wurde von RSA Data Security, Inc. entwickelt und wird von Prov \_ RSA \_ Full, Prov \_ RSA \_ SIG, Prov \_ DSS, Prov \_ DSS \_ dh und Prov \_ MS \_ Exchange Provider Types angegeben.

Siehe auch *MD2-Algorithmus*, *MD4-Algorithmus*.

</dd> <dt>

<span id="_security_message_gly"></span><span id="_SECURITY_MESSAGE_GLY"></span>**Nachricht**
</dt> <dd>

Alle Daten, die für die Übertragung an eine Person oder Entität codiert oder von dieser empfangen wurden. Nachrichten können für den Datenschutz verschlüsselt, zu Authentifizierungs Zwecken digital signiert werden oder beides.

</dd> <dt>

<span id="_security_message_digest_gly"></span><span id="_SECURITY_MESSAGE_DIGEST_GLY"></span>**Nachrichten Digest**
</dt> <dd>

Siehe [*Hash*](h-gly.md).

</dd> <dt>

<span id="_security_message_authentication_code_gly"></span><span id="_SECURITY_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**Nachrichtenauthentifizierungscode**
</dt> <dd>

Mac Ein Schlüssel gebundener Hash Algorithmus, der einen symmetrischen Sitzungsschlüssel verwendet, um sicherzustellen, dass ein Datenblock von dem Zeitpunkt, an dem er gesendet wurde, seine Integrität beibehaltenen hat. Wenn Sie diese Art von Algorithmus verwenden, muss die empfangende Anwendung auch den Sitzungsschlüssel besitzen, um den Hashwert neu zu berechnen, damit überprüft werden kann, ob sich die Basisdaten nicht geändert haben. CryptoAPI verweist auf diesen Algorithmus durch den Typ (calg \_ Mac), den Namen (Mac) und die Klasse (ALG- \_ Klassen \_ Hash).

</dd> <dt>

<span id="_security_message_encoding_type_gly"></span><span id="_SECURITY_MESSAGE_ENCODING_TYPE_GLY"></span>**Nachrichten Codierungstyp**
</dt> <dd>

Definiert, wie die Meldung codiert wird. Der Nachrichten Codierungstyp wird im hochwertigen Wort der Codierungstyp Struktur gespeichert. Die aktuell definierten Codierungs Typen lauten: Crypt \_ ASN \_ Encoding, X509 \_ ASN \_ Encoding und PKCS \_ 7 \_ ASN \_ Encoding.

</dd> <dt>

<span id="_security_message_management_functions_gly"></span><span id="_SECURITY_MESSAGE_MANAGEMENT_FUNCTIONS_GLY"></span>**Nachrichten Verwaltungsfunktionen**
</dt> <dd>

Funktionen, die zwei Ebenen der Nachrichten Verwaltung bereitstellen: Nachrichten Funktionen auf niedriger Ebene und vereinfachte Nachrichten Funktionen. Die Nachrichten Funktionen auf niedriger Ebene bieten mehr Flexibilität als die vereinfachten Nachrichten Funktionen. Allerdings benötigen Sie mehr Funktionsaufrufe.

</dd> <dt>

<span id="_security_message_signing_functions_gly"></span><span id="_SECURITY_MESSAGE_SIGNING_FUNCTIONS_GLY"></span>**Funktionen zur Nachrichten Signierung**
</dt> <dd>

Funktionen zum Signieren von Nachrichten und Daten.

Siehe auch [*vereinfachte Nachrichten Funktionen*](s-gly.md).

</dd> <dt>

<span id="_security_mpr_gly"></span><span id="_SECURITY_MPR_GLY"></span>**MPR**
</dt> <dd>

Siehe *mehrere Anbieter Router*.

</dd> <dt>

<span id="_security_multiple_provider_router_gly"></span><span id="_SECURITY_MULTIPLE_PROVIDER_ROUTER_GLY"></span>**Mehrere Anbieter Router**
</dt> <dd>

MPR Eine Systemkomponente, die die Kommunikation zwischen dem System und allen Netzwerkanbietern verarbeitet. Die MPR Ruft die Netzwerkanbieter Funktionen auf, die von jedem Netzwerkanbieter verfügbar gemacht werden.

</dd> </dl>

 

 



