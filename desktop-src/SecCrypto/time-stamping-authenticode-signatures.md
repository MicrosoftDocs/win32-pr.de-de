---
description: Die Authenticode-Zeitstempel basiert auf Standard-PKCS \# 9-gegen Signaturen. Mithilfe von Signierungs Tools von Microsoft können Entwicklerzeit Stempel zur gleichen Zeit wie Authentifizieren von Authenticode-Signaturen zulösen.
ms.assetid: d0bd3e2f-1eee-4f71-9467-974994f720d5
title: Zeitstempel für Authenticode-Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3631d402da56d4078cecce65075c92dff0ec7e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216198"
---
# <a name="time-stamping-authenticode-signatures"></a>Zeitstempel für Authenticode-Signaturen

Microsoft Authenticode-Signaturen bieten Autoren-und Integritäts Garantien für Binärdaten. Die Authenticode-Zeitstempel basiert auf Standard-PKCS \# 9-gegen Signaturen. Mithilfe von Signierungs Tools von Microsoft können Entwicklerzeit Stempel zur gleichen Zeit wie Authentifizieren von Authenticode-Signaturen zulösen. Das Zeitstempel ermöglicht die über Prüfbarkeit von Authenticode-Signaturen, auch nachdem die für die Signatur verwendeten Zertifikate abgelaufen sind.

## <a name="a-brief-introduction-to-authenticode"></a>Eine kurze Einführung in Authenticode

[*Authenticode*](../secgloss/a-gly.md) wendet eine digitale Signatur Technologie an, um die Autorenschaft und Integrität binärer Daten, z. b. installier barer Software Ein Client Webbrowser oder andere Systemkomponenten können die Authenticode-Signaturen verwenden, um die Integrität der Daten zu überprüfen, wenn die Software heruntergeladen oder installiert wird. Authenticode-Signaturen können mit vielen Software Formaten verwendet werden, einschließlich CAB-, exe-, ocx-und dll-Dateien.

Microsoft verwaltet eine Liste der öffentlichen [*Zertifizierungs*](/security/trusted-root/participants-list) stellen. Aussteller von Authenticode-Zertifikaten enthalten derzeit [SSL.com](https://www.ssl.com/), [Digicert](https://www.digicert.com/), [sectigo (Comodo)](https://www.sectigo.com/)und [GlobalSign](https://www.globalsign.com/).

## <a name="about-cryptographic-time-stamping"></a>Informationen zum kryptografischen Zeitstempel

In der Vergangenheit wurden verschiedene kryptografische Zeitstempel Methoden vorgeschlagen. Siehe z. b. "ber" und "stornettta" How to Time-Stamp a Digital Document "im *Journal der Cryptology* (1991) und in Benaloh und de Stute" unidirektionale Akkumulatoren: eine dezentralisierte Alternative zu digitalen Signaturen "in den *Springer-Verlag-Vorbemerkungen in Computer Wissenschaft* Vol. 765 (Eurocrypt" 93). Eine erweiterte Abstraktion dieses Artikels ist in [Microsoft Research](https://research.microsoft.com/research/pubs/view.aspx?id=233&type=Publication&0sr=a)verfügbar. (Diese Ressourcen sind möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.) Da time eine physische und nicht mathematische Menge ist, betreffen diese Methoden in der Regel, wie Objekte miteinander verknüpft werden, damit ihre Reihenfolge der Erstellung bestimmt werden kann, oder wie Objekte effizient gruppiert werden können, die als gleichzeitig erstellt werden können.

Systeme, die zur Authentifizierung der Zeit als Menge dienen, benötigen immer eine bestimmte Form von Vertrauenswürdigkeit. In einer Einstellung mit starker Adversarial können komplexe Protokolle verwendet werden, um einen gewissen Grad an Synchronität sicherzustellen. Diese Protokolle erfordern jedoch eine umfangreiche Interaktion zwischen den betroffenen Parteien. In der Praxis kann die Quelle, wenn Sie nur eine zertifizierungszeit von einer vertrauenswürdigen Quelle benötigt, einfach als Notar fungieren, indem eine signierte Anweisung (Certification) bereitgestellt wird, dass das Objekt zum festgelegten Zeitpunkt zur Signatur vorgelegt wurde.

Die unten implementierte Methode zur gegen Signatur des Zeitstempels ermöglicht das Überprüfen von Signaturen, auch wenn das Signaturzertifikat abgelaufen oder widerrufen wurde. Der Zeitstempel ermöglicht dem Verifizierer, die Zeit, zu der die Signatur einging, zuverlässig zu erkennen und damit der Signatur zu vertrauen, wenn Sie zu diesem Zeitpunkt gültig war. Der Zeitstempel sollte eine zuverlässige und geschützte Zeit Quelle aufweisen.

## <a name="pkcs-7-signed-documents-and-countersignatures"></a>Mit PKCS \# 7 signierte Dokumente und gegen Signaturen

PKCS \# 7 ist ein Standardformat für kryptografische Daten, einschließlich signierter Daten, Zertifikate und [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs). Der für den \# Kontext des Zeitstempels relevante PKCS 7-Typ ist signierte Daten, die dem von PKCS \# 7 definierten [**SignedData**](signeddata.md) -Inhaltstyp entsprechen.

Das PKCS \# 7-Paket besteht aus [**SignedData**](signeddata.md) , das den eigentlichen Inhalt und bestimmte Informationen über die Signatur Blöcke von IT und SignerInfo identifiziert. Eine Signatur Info kann selbst eine gegen Signatur enthalten, bei der es sich rekursiv um einen weiteren SignerInfo handelt. Im Prinzip kann eine Sequenz dieser gegen Signaturen vorhanden sein. Die gegen Signatur ist ein nicht authentifiziertes Attribut in Bezug auf die Signatur in der SignerInfo. Das heißt, es kann nach der ursprünglichen Signatur angebracht werden. In umrissform:

[**SignedData**](signeddata.md) (PKCS \# 7)

-   Version (von PKCS \# 7, allgemein Version 1)
-   Digestalgorithms (Sammlung aller von SignerInfo-Signatur Blöcken verwendeten Algorithmen zur Optimierung der Verarbeitung)
-   ContentInfo (ContentType entspricht [**SignedData**](signeddata.md), plus Inhalt oder Verweis auf Inhalt)
-   Optionale Zertifikate (Sammlung aller verwendeten Zertifikate)
-   Optionale CRLs (Sammlung aller CRLs)
-   SignerInfo-Signatur Blöcke (die tatsächliche Signatur, bestehend aus mindestens einem SignerInfo-Signatur Block)

SignerInfo (der Signatur Block)

-   Version (von PKCS \# 7, allgemein Version 1)
-   Zertifikat (Aussteller und Seriennummer, um das Zertifikat des Signatur Gebers in [**SignedData**](signeddata.md)eindeutig zu identifizieren)
-   DigestAlgorithm Plus digestencryptionalgorithmus Plus Digest (Hash) plus verschlüsselteddigest (tatsächliche Signatur)
-   Optionale authenticatedattributes (z. b. von diesem Signatur Geber signiert)
-   Optionaler unauthenticatedattributes (z. b. nicht von diesem Signatur Geber signiert)

Ein Beispiel für ein authentifiziertes Attribut ist die Signatur Zeit (OID 1.2.840.113549.1.9.5), da es Teil der Signatur des Zeitstempel Dienstanbieter ist. Ein Beispiel für ein nicht authentifiziertes Attribut ist die gegen Signatur (OID 1.2.840.113549.1.9.6), da Sie nach dem Signieren angehängt werden kann. In diesem Fall enthält die SignerInfo selbst eine SignerInfo (die gegen Signatur).

> [!Note]  
> Das Objekt, das in der gegen Signatur signiert ist, ist die ursprüngliche Signatur (d. h. der Verschlüsselungs Digest der ursprünglichen SignerInfo).

 

## <a name="signtool-and-the-authenticode-process"></a>SignTool und der Authenticode-Prozess

[SignTool](signtool.md) ist für die Authenticode-Signatur-und Zeitstempel Binärdaten verfügbar. Das Tool wird im \\ Ordner bin des Installations Pfads des Microsoft Windows Software Development Kit (SDK) installiert.

Das Signieren und Zeitstempel von Binärdaten ist mithilfe von [SignTool](signtool.md)relativ unkompliziert. Der Herausgeber muss ein Code Signaturzertifikat von einer kommerziellen Code Signatur-Zertifizierungsstelle erhalten. Aus Gründen der praktische Veröffentlichung veröffentlicht und aktualisiert Microsoft eine Liste mit öffentlichen Zertifizierungsstellen, einschließlich derjenigen, die Authenticode-Zertifikate ausstellen. Wenn Sie bereit für die Veröffentlichung sind, werden die Objektdateien signiert und mit den entsprechenden Befehlszeilen Parametern mit dem SignTool-Tool versehen. Das Ergebnis eines beliebigen SignTool-Vorgangs ist immer ein PKCS \# 7-Format [**SignedData**](signeddata.md).

SignTool akzeptiert als Eingabe entweder unformatierte Binärdaten, die signiert und mit einem Zeitstempel versehen werden, oder zuvor signierte Binärdaten, die Zeitstempel sind. Daten, die zuvor signiert wurden, können mithilfe des **SignTool-Zeitstempel** -Befehls mit einem Zeitstempel versehen werden.



| Argument             | BESCHREIBUNG                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/t** *HttpAddress* | Gibt an, dass die Datei mit einem Zeitstempel versehen werden soll. Eine URL, die die Adresse eines Zeitstempel Servers angibt, muss angegeben werden. **/t** kann mit den Zeitstempel-Befehlen **SignTool Sign** und **SignTool** verwendet werden. |



 

Weitere Informationen zu Tools, die in diesem Kontext nützlich sein können, finden Sie unter [Cryptography Tools](cryptography-tools.md) und [SignTool](signtool.md).

## <a name="implementation-details-and-wire-format"></a>Implementierungs Details und Wire-Format

[SignTool](signtool.md) basiert auf der Windows Authenticode-Implementierung zum Erstellen von und Zeitstempel Signaturen. [*Authenticode*](../secgloss/a-gly.md) funktioniert auf Binärdateien, z. b.. cab,. exe,. dll oder. ocx. Authenticode erstellt zunächst die Signatur und erzeugt eine PKCS \# 7 [**SignedData**](signeddata.md). Diese **SignedData** müssen gegen signiert werden, wie in PKCS \# 9 beschrieben.

Der gegen Signatur Vorgang erfolgt in vier Schritten:

1.  Kopieren Sie die Signatur (d. h. "verschlüsselteddigest") aus den SignerInfo der "PKCS \# 7 [**SignedData**](signeddata.md)".
2.  Erstellen Sie eine Zeitstempel Anforderung, deren Inhalt die ursprüngliche Signatur ist. Senden Sie diese an den Zeitstempel Server [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1), der als timestamprequest codiert ist.
3.  Empfangen eines Zeitstempels, der als zweites PKCS \# 7 [**SignedData**](signeddata.md)formatiert ist und vom Zeitstempel Server zurückgegeben wird.
4.  Kopieren Sie die SignerInfo aus dem Zeitstempel direkt in die ursprünglichen PKCS \# 7 [**SignedData**](signeddata.md)als PKCS \# 9-gegen Signatur (d. h. ein nicht authentifiziertes Attribut in der SignerInfo des Originals).

## <a name="time-stamp-request"></a>Zeitstempel Anforderung

Die Zeitstempel Anforderung wird innerhalb einer HTTP 1,1 Post-Nachricht gesendet. Im HTTP-Header ist die CacheControl-Direktive auf No-Cache festgelegt, und die Content-Type-Direktive ist auf Application/Octett-Stream festgelegt. Der Text der HTTP-Nachricht ist eine Base64-Codierung der [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der)-Codierung der Zeitstempel Anforderung.

Obwohl Sie zurzeit nicht verwendet wird, sollte die Content-length-Direktive auch zum Erstellen der HTTP-Nachricht verwendet werden, da Sie dem Zeitstempel Server beim Suchen nach dem Speicherort der Anforderung innerhalb des http-Beitrags hilft.

Andere HTTP-Header können auch vorhanden sein und sollten ignoriert werden, wenn Sie vom Anforderer oder Zeitstempel Server nicht verstanden werden.

Die Zeitstempel Anforderung ist eine ASN. 1-codierte Nachricht. Das Format der Anforderung lautet wie folgt.

``` syntax
TimeStampRequest ::= SEQUENCE {
   countersignatureType OBJECT IDENTIFIER,
   attributes Attributes OPTIONAL, 
   content  ContentInfo
}
```

Countersignaturetype ist die [*Objekt*](../secgloss/o-gly.md) -ID (OID), die dies als Zeitstempel gegen Signatur identifiziert und die exakte OID-1.3.6.1.4.1.311.3.2.1 sein sollte.

In der Zeitstempel Anforderung sind zurzeit keine Attribute enthalten.

Der Inhalt ist eine ContentInfo, wie von PKCS \# 7 definiert. Der Inhalt ist die zu Signier enden Daten. Zum Signaturzeit Stempel sollte ContentType "Data" lauten, und der Inhalt sollte "verschlüsselteddigest" (Signatur) aus den SignerInfo des PKCS \# 7-Inhalts sein, um einen Zeitstempel zu erhalten.

## <a name="time-stamp-response"></a>Zeitstempel Antwort

Die Zeitstempel Antwort wird auch innerhalb einer HTTP 1,1-Nachricht gesendet. Im HTTP-Header wird die Content-Type-Direktive auch auf Application/Octett-Stream festgelegt. Der Text der HTTP-Nachricht ist eine Base64-Codierung der der-Codierung der Zeitstempel Antwort.

Die Zeitstempel Antwort ist eine PKCS \# 7-signierte Nachricht, die vom Zeitstempel signiert wurde. Die ContentInfo der PKCS \# 7-Nachricht ist mit der im Zeitstempel empfangenen ContentInfo identisch. Der Inhalt von PKCS \# 7 enthält das authentifizierte Signatur Zeit Attribut (definiert in PKCS \# 99, OID 1.2.840.113549.9.5).

Nachdem Authenticode den Zeitstempel vom Server empfangen hat, wird der Zeitstempel von Authenticode als gegen Signatur in die ursprünglichen PKCS \# 7- [**SignedData**](signeddata.md) integriert. Um dies zu erreichen, werden die ContentInfo der zurückgegebenen PKCS \# 7- **SignedData** verworfen, und die SignerInfo des zurückgegebenen Zeitstempels wird als gegen Signatur in die SignerInfo der ursprünglichen PKCS \# 7- **SignedData** kopiert. Die Zertifikat Kette des Zeit stempgers wird auch in die ursprünglichen PKCS \# 7- **SignedData** als nicht authentifiziertes Attribut des ursprünglichen Signatur Gebers kopiert.

Weitere Informationen zu PKCS und anderen Sicherheitsthemen finden Sie in der [Inhalts Bibliothek der RSA-Website](https://www.rsa.com/content_library.aspx).

 

 
