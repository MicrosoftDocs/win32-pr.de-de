---
description: Das Authenticode-Zeitstempeling basiert auf PKCS \# 7-Standard-Gegensignaturen. Mit Signaturtools von Microsoft können Entwickler Zeitstempel gleichzeitig anheften, während sie Authenticode-Signaturen anheften.
ms.assetid: d0bd3e2f-1eee-4f71-9467-974994f720d5
title: Zeitstempel von Authenticode-Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0232853441d2c11d331c175ac7e8dfd120b341ff
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327185"
---
# <a name="time-stamping-authenticode-signatures"></a>Zeitstempel von Authenticode-Signaturen

Microsoft Authenticode-Signaturen bieten Erstellungs- und Integritätsgarantien für Binärdaten. Das Authenticode-Zeitstempeling basiert auf PKCS \# 7-Standard-Gegensignaturen. Mit Signaturtools von Microsoft können Entwickler Zeitstempel gleichzeitig anheften, während sie Authenticode-Signaturen anheften. Mit dem Zeitstempel können Authenticode-Signaturen auch dann überprüfbar sein, wenn die für die Signatur verwendeten Zertifikate abgelaufen sind.

## <a name="a-brief-introduction-to-authenticode"></a>Eine kurze Einführung in Authenticode

[*Authenticode*](../secgloss/a-gly.md) wendet digitale Signaturtechnologie an, um die Erstellung und Integrität von Binärdaten wie installierbarer Software zu gewährleisten. Ein Clientwebbrowser oder andere Systemkomponenten können die Authenticode-Signaturen verwenden, um die Integrität der Daten zu überprüfen, wenn die Software heruntergeladen oder installiert wird. Authenticode-Signaturen können mit vielen Softwareformaten verwendet werden, einschließlich CAB, EXE, OCX und DLL.

Microsoft verwaltet eine Liste mit öffentlichen [*Zertifizierungsstellen*](/security/trusted-root/participants-list) (CAs). Zu den Ausstellern von Authenticode-Zertifikaten gehören derzeit [SSL.com](https://www.ssl.com/), [Digicert](https://www.digicert.com/), [Sectigo(Comodo)](https://www.sectigo.com/)und [GlobalSign](https://www.globalsign.com/).

## <a name="about-cryptographic-time-stamping"></a>Informationen zum kryptografischen Zeitstempel

In der Vergangenheit wurde eine Vielzahl kryptografischer Zeitstempelmethoden vorgeschlagen. Siehe z.B. Haber und Storn msi "How to Time-Stamp a Digital Document" im *Journal of Crypto alternatives* (1991) und Benaloh und de Signe "One-Way Akkumulatoren: Eine dezentralisierte Alternative zu digitalen Signaturen" in *Springer-Umleitungshinweisen in Der Computer science* vol. 765 (EUROCRYPT '93). Eine erweiterte Zusammenfassung dieses Artikels finden Sie unter [Microsoft Research.](https://research.microsoft.com/research/pubs/view.aspx?id=233&type=Publication&0sr=a) (Diese Ressourcen sind in einigen Sprachen und Ländern oder Regionen möglicherweise nicht verfügbar.) Da die Zeit eine physische statt einer mathematischen Menge ist, betreffen diese Methoden im Allgemeinen, wie Objekte so verlinkt werden, dass ihre Reihenfolge der Erstellung bestimmt werden kann, oder wie Objekte effizient gruppieren, die alle als gleichzeitig erstellt beschrieben werden können.

Systeme, bei denen die Authentifizierungszeit als Menge verwendet wird, erfordern immer eine Form von Vertrauensstellung. In einer stark konversiven Einstellung können komplexe Protokolle verwendet werden, um ein gewisses Maß an Synchronität sicherzustellen. Diese Protokolle erfordern jedoch eine umfassende Interaktion zwischen den betroffenen Parteien. In der Praxis kann die Quelle einfach als Notar fungieren, wenn nur eine Zeitzertifizierung von einer vertrauenswürdigen Quelle benötigt wird, indem eine signierte Anweisung (Zertifizierung) angegeben wird, dass das Objekt zum angegebenen Zeitpunkt zur Signatur präsentiert wurde.

Die unten implementierte Gegensignaturmethode des Zeitstempels ermöglicht die Überprüfung von Signaturen, auch nachdem das Signaturzertifikat abgelaufen oder widerrufen wurde. Mit dem Zeitstempel kann der Verifizierer zuverlässig wissen, zu welchem Zeitpunkt die Signatur angebracht wurde, und dadurch der Signatur vertrauen, wenn sie zu diesem Zeitpunkt gültig war. Der Zeitstempel sollte über eine zuverlässige und geschützte Zeitquelle verfügen.

## <a name="pkcs-7-signed-documents-and-countersignatures"></a>SIGNIERTE PKCS \# 7-Dokumente und Gegensignaturen

PKCS 7 ist ein Standardformat für kryptografische Daten, einschließlich signierter Daten, Zertifikate und \# Zertifikatsperrlisten (Certificate [*Revocation Lists,*](../secgloss/c-gly.md) CRLs). Der spezielle PKCS 7-Typ, der im Kontext des Zeitstempels von Interesse ist, sind signierte Daten, die dem von \# PKCS 7 definierten \# [**SignedData-Inhaltstyp**](signeddata.md) entspricht.

Das PKCS 7-Paket besteht aus SignedData, die den tatsächlichen Inhalt und bestimmte Informationen darüber sowie \# SignerInfo-Signaturblöcke identifiziert. [](signeddata.md) SignerInfo kann selbst eine Gegensignatur enthalten, die rekursiv eine weitere SignerInfo ist. Im Prinzip kann eine Sequenz solcher Gegensignaturen vorhanden sein. Die Gegensignatur ist ein nicht authentifiziertes Attribut in Bezug auf die Signatur in der SignerInfo. Das heißt, sie kann nach der ursprünglichen Signatur fixiert werden. In Gliederungsform:

[**SignedData**](signeddata.md) (PKCS \# 7)

-   Version (von PKCS \# 7, in der Regel Version 1)
-   DigestAlgorithms (Sammlung aller Algorithmen, die von SignerInfo-Signaturblöcken für die optimierte Verarbeitung verwendet werden)
-   ContentInfo (contentType entspricht [**SignedData**](signeddata.md), plus Inhalt oder Verweis auf Inhalt)
-   OPTIONALE Zertifikate (Sammlung aller verwendeten Zertifikate)
-   OPTIONALE CRLs (Sammlung aller CRLs)
-   SignerInfo-Signaturblöcke (die tatsächliche Signatur, die aus einem oder mehreren SignerInfo-Signaturblöcken besteht)

SignerInfo (der Signaturblock)

-   Version (von PKCS \# 7, in der Regel Version 1)
-   Zertifikat (Aussteller und Seriennummer zur eindeutigen Identifizierung des Signaturgeberzertifikats in [**SignedData)**](signeddata.md)
-   DigestAlgorithm plus DigestEncryptionAlgorithm plus Digest (Hash) plus EncryptedDigest (tatsächliche Signatur)
-   OPTIONAL AuthenticatedAttributes (z. B. von diesem Signaturgeber signiert)
-   OPTIONAL UnauthenticatedAttributes (z. B. nicht von diesem Signaturgeber signiert)

Ein Beispiel für ein authentifiziertes Attribut ist die Signierungszeit (OID 1.2.840.113549.1.9.5), da sie Teil der Signatur des Zeitstempeldiensts ist. Ein Beispiel für ein nicht authentifiziertes Attribut ist die Gegensignatur (OID 1.2.840.113549.1.9.6), da sie nach dem Signieren fixiert werden kann. In diesem Fall enthält signerInfo selbst eine SignerInfo (countersignature).

> [!Note]  
> Das Objekt, das in der Gegensignatur signiert ist, ist die ursprüngliche Signatur (d. b. EncryptedDigest der ursprünglichen SignerInfo).

 

## <a name="signtool-and-the-authenticode-process"></a>SignTool und der Authenticode-Prozess

[SignTool ist](signtool.md) für Authenticode-Signatur- und Zeitstempel-Binärdaten verfügbar. Das Tool wird im Ordner \\ Bin des Installationspfads von Microsoft Windows Software Development Kit (SDK) installiert.

Das Signieren und Das Zeitstempeln von Binärdaten ist mit [SignTool relativ einfach.](signtool.md) Der Herausgeber muss ein Codesignaturzertifikat von einer kommerziellen Codesignatur-Zertifizierungsstelle erhalten. Der Einfachheit halber veröffentlicht und aktualisiert Microsoft eine Liste mit öffentlichen Zertifizierungsstelle, einschließlich der Zertifizierungsstelle, die Authenticode-Zertifikate aushing. Wenn sie zur Veröffentlichung bereit sind, werden die Objektdateien signiert und mithilfe der entsprechenden Befehlszeilenparameter mit dem SignTool-Tool mit einem Zeitstempel versehen. Das Ergebnis eines SignTool-Vorgangs ist immer das PKCS \# 7-Format [**SignedData.**](signeddata.md)

SignTool akzeptiert als Eingabe entweder binäre Rohdaten, die signiert und mit einem Zeitstempel versehen werden sollen, oder zuvor signierte Binärdaten, die mit einem Zeitstempel versehen werden sollen. Daten, die zuvor signiert wurden, können mithilfe des Befehls **signtool timestamp** mit einem Zeitstempel versehen werden.



| Argument             | BESCHREIBUNG                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/t** *HTTPAddress* | Gibt an, dass für die Datei ein Zeitstempel verwendet werden soll. Eine URL, die eine Adresse eines Zeitstempelservers angibt, muss angegeben werden. **/t kann** sowohl mit **signtool sign-** als auch **mit signtool-Zeitstempelbefehlen verwendet** werden. |



 

Weitere Informationen zu Tools, die in diesem Kontext nützlich sein können, finden Sie unter [Cryptography Tools](cryptography-tools.md) und [SignTool](signtool.md).

## <a name="implementation-details-and-wire-format"></a>Implementierungsdetails und Wire Format

[SignTool verwendet](signtool.md) die Windows Authenticode-Implementierung zum Erstellen von Und Zeitstempelsignaturen. [*Authenticode*](../secgloss/a-gly.md) arbeitet mit Binärdateien wie CAB, EXE, DLL oder OCX. Authenticode erstellt zuerst die Signatur und erzeugt einen PKCS \# 7 [**SignedData-Wert.**](signeddata.md) Diese **SignedData-Daten** müssen gegensigniert werden, wie in PKCS \# 9 beschrieben.

Der Gegensignaturprozess erfolgt in vier Schritten:

1.  Kopieren Sie die Signatur (d.h. encryptedDigest) aus der SignerInfo des PKCS \# 7 [**SignedData**](signeddata.md).
2.  Erstellen Sie eine Zeitstempelanforderung, deren Inhalt die ursprüngliche Signatur ist. Senden Sie dies an den Zeitstempelserver [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1), der als TimeStampRequest codiert ist.
3.  Empfangen Sie einen Zeitstempel, der als zweites PKCS 7 SignedData formatiert ist \# und vom Zeitstempelserver zurückgegeben wird. [](signeddata.md)
4.  Kopieren Sie signerInfo aus dem Zeitstempel direkt in die ursprüngliche PKCS \# 7 [**SignedData**](signeddata.md)als PKCS \# 9-Gegensignatur (d.amp;n.b. ein nicht authentifiziertes Attribut in der SignerInfo des Originals).

## <a name="time-stamp-request"></a>Zeitstempelanforderung

Die Zeitstempelanforderung wird innerhalb einer HTTP 1.1 POST-Nachricht gesendet. Im HTTP-Header wird die CacheControl-Direktive auf no-cache und die Content-Type-Direktive auf application/octet-stream festgelegt. Der Text der HTTP-Nachricht ist eine Base64-Codierung der [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-Codierung der Zeitstempelanforderung.

Obwohl sie derzeit nicht verwendet wird, sollte die Content-Length-Direktive auch zum Erstellen der HTTP-Nachricht verwendet werden, da sie dem Zeitstempelserver hilft, zu ermitteln, wo sich die Anforderung innerhalb von HTTP POST befindet.

Andere HTTP-Header können ebenfalls vorhanden sein und sollten ignoriert werden, wenn sie vom Anforderer oder Zeitstempelserver nicht verstanden werden.

Die Zeitstempelanforderung ist eine ASN.1-codierte Nachricht. Das Format der Anforderung lautet wie folgt.

``` syntax
TimeStampRequest ::= SEQUENCE {
   countersignatureType OBJECT IDENTIFIER,
   attributes Attributes OPTIONAL, 
   content  ContentInfo
}
```

CountersignatureType ist der [*Objektbezeichner*](../secgloss/o-gly.md) (OID), der diese als Zeitstempel-Gegensignatur identifiziert und die genaue OID 1.3.6.1.4.1.311.3.2.1 sein sollte.

In der Zeitstempelanforderung sind derzeit keine Attribute enthalten.

Der Inhalt ist eine ContentInfo, wie in PKCS \# 7 definiert. Bei dem Inhalt handelt es sich um die zu signierten Daten. Für das Signaturzeitstempeln sollte der ContentType Data sein, und der Inhalt sollte der encryptedDigest (Signatur) aus der SignerInfo des PKCS \# 7-Inhalts sein, um einen Zeitstempel zu erhalten.

## <a name="time-stamp-response"></a>Zeitstempelantwort

Die Zeitstempelantwort wird auch innerhalb einer HTTP 1.1-Nachricht gesendet. Im HTTP-Header wird die Content-Type-Direktive ebenfalls auf application/octet-stream festgelegt. Der Text der HTTP-Nachricht ist eine Base64-Codierung der DER-Codierung der Zeitstempelantwort.

Die Zeitstempelantwort ist eine vom Zeitstempeler signierte PKCS \# 7-Nachricht. Die ContentInfo der PKCS 7-Nachricht ist mit der im Zeitstempel \# empfangenen ContentInfo identisch. Der PKCS 7-Inhalt enthält das authentifizierte Signaturzeitattribut \# (definiert in PKCS \# 99, OID 1.2.840.113549.9.5).

Nachdem Authenticode den Zeitstempel vom Server empfangen hat, integriert Authenticode den Zeitstempel in die ursprünglichen PKCS \# 7 [**SignedData-Daten**](signeddata.md) als Gegensignatur. Hierzu wird die ContentInfo der zurückgegebenen PKCS 7 SignedData verworfen, und die SignerInfo des zurückgegebenen Zeitstempels wird als Gegensignatur in die SignerInfo der ursprünglichen \# PKCS  \# 7 **SignedData** kopiert. Die Zertifikatkette des Zeitstempels wird auch in Zertifikate in den ursprünglichen PKCS \# 7 **SignedData** als nicht authentifizierte Attribute des ursprünglichen Signaturers kopiert.

Weitere Informationen zu PKCS und anderen Sicherheitsthemen finden Sie in der [Inhaltsbibliothek der RSA-Website](https://www.rsa.com/content_library.aspx).

 

 
