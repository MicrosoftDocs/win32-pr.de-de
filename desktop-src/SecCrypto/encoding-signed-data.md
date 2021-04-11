---
description: Stellt die Prozedur zum Codieren einer signierten Nachricht dar.
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: Codieren signierter Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4a542fe0890a6ee9d51ebc1a5ee6b98bab4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217433"
---
# <a name="encoding-signed-data"></a>Codieren signierter Daten

[*Signierte Daten*](../secgloss/s-gly.md) bestehen aus dem Inhalt eines beliebigen Typs und verschlüsselten [*Nachrichtenhashes*](../secgloss/h-gly.md) des Inhalts durch Null oder mehr Signatur Geber. Mit dem resultierenden Hash kann bestätigt werden, dass die ursprüngliche Nachricht seit der Signierung nicht geändert wurde und dass die Daten von den jeweiligen Personen oder Entitäten signiert wurden.

In der folgenden Abbildung wird die Vorgehensweise zum Codieren einer signierten Nachricht veranschaulicht. In der Liste, die der Abbildung folgt, werden die Schritte beschrieben.

Eine Nachricht kann mehrere Signatur Geber, Hash Algorithmen und Zertifikate enthalten. Während in der Abbildung nur Zertifikate, [*CRLs*](../secgloss/c-gly.md)und [*CTLs*](../secgloss/c-gly.md) angezeigt werden, kann der gleiche Prozess verwendet werden. Diese werden in die Abbildung eingefügt, wo Zertifikate angezeigt werden.

![Codieren einer signierten Nachricht](images/signmsg2.png)

Der allgemeine Prozess zum Codieren [*signierter Daten*](../secgloss/s-gly.md) ist wie folgt.

**So codieren Sie signierte Daten**

1.  Die Daten werden (falls erforderlich) erstellt, und es wird ein Zeiger darauf abgerufen.
2.  Es wird ein [*Zertifikat Speicher*](../secgloss/c-gly.md) geöffnet, der das Zertifikat des Signatur Gebers enthält.
3.  Der private Schlüssel für das Zertifikat wird abgerufen. Es gibt zwei Eigenschaften, die für das Zertifikat festgelegt werden müssen, bevor es verwendet wird. Eine wird verwendet, um ein Zertifikat mit einem bestimmten CSP und innerhalb dieses CSP an einen bestimmten privaten [*Schlüssel Container*](../secgloss/k-gly.md)zu binden. Der andere Wert wird verwendet, um anzugeben, welcher Hash Algorithmus verwendet werden soll, wenn ein [*Hash*](../secgloss/h-gly.md) Vorgang aufgerufen wird. Diese müssen nur einmal festgelegt werden.
4.  Die-Eigenschaft eines Zertifikats bestimmt den Hash Algorithmus.
5.  Ein Hash der Daten wird erstellt, indem die Daten über die Hash Funktion gesendet werden.
6.  Die Signatur wird erstellt, indem der Hash mithilfe des privaten Schlüssels verschlüsselt wird, der über eine Eigenschaft im Zertifikat abgerufen wird.
7.  Die fertige, signierte Nachricht enthält die folgenden Daten:
    -   Die zu Signier enden ursprünglichen Daten
    -   Die Hash Algorithmen
    -   Die Signaturen
    -   Die Signatur Geber Info-Strukturen, die den Signatur Geber Bezeichner (Zertifikat Aussteller und Seriennummer) enthalten.
    -   Die Zertifikate des Signatur Gebers (optional)

Diese Prozedur veranschaulicht einen einfachen Fall. Komplexere Fälle umfassen authentifizierte Attribute, die in der Nachricht enthalten sind. Wenn der Inhaltstyp etwas anderes als eine **Byte** Zeichenfolge ist oder mindestens ein authentifiziertes Attribut zusammen mit einem beliebigen Datentyp vorhanden ist, sind zwei authentifizierte Standard Attribute erforderlich: der Inhalt (Daten) und der Hash des Inhalts. Unter diesen Umständen stellt die [*CryptoAPI*](../secgloss/c-gly.md) diese beiden erforderlichen Attribute automatisch bereit. Die Nachrichten Funktionen auf niedriger Ebene hashten die authentifizierten Attribute, verschlüsseln den Hash mit dem privaten Schlüssel und stellen diesen als Signatur bereit.

Verwenden Sie die Meldungs Funktionen auf niedriger Ebene, um die gerade aufgelisteten Aufgaben durchzuführen. gehen Sie hierzu wie folgt vor.

**So codieren Sie eine signierte Nachricht**

1.  Erstellen oder Abrufen des Inhalts.
2.  Verschaffen Sie sich einen Kryptografieanbieter.
3.  Holen Sie sich die Signatur Geber Zertifikate.
4.  Initialisieren Sie die [**CMSG-Signatur Geber- \_ \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) Struktur.
5.  Initialisieren Sie die [**CMSG- \_ signierte \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) Struktur mit Vorzeichen.
6.  Sie können [**cryptmsgcalculateencodedlength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) aufrufen, um die Größe des codierten nachrichtenblobs zu erhalten. Arbeitsspeicher zuweisen.
7.  Nennen Sie [**cryptmsgopentoencode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), und übergeben Sie \_ für " *dwmsgtype* " signierte CMSG und einen Zeiger auf [**CMSG- \_ signierte \_ codierinformationen \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) für " *pvmsgencodeinfo* ", um ein Handle für die geöffnete Nachricht zu erhalten.
8.  Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), und übergeben Sie das in Schritt 7 abgerufene Handle und einen Zeiger auf die Daten, die signiert und codiert werden sollen. Diese Funktion kann so oft wie nötig aufgerufen werden, um den Codierungsprozess abzuschließen.
9.  Aufrufen von [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), übergeben des in Schritt 7 abgerufenen Handles und der entsprechenden Parametertypen für den Zugriff auf die gewünschten, codierten Daten. Übergeben Sie z. b. CMSG \_ Content \_ param, um einen Zeiger auf die gesamte [*PKCS \# 7*](../secgloss/p-gly.md) -Nachricht zu erhalten.

    Wenn das Ergebnis dieser Codierung als [*innere Daten*](../secgloss/i-gly.md) für eine andere codierte Nachricht verwendet werden soll, z. b. eine eingeschlossene Nachricht, muss der CMSG-Parameter für den \_ Bare-Content- \_ \_ Parameter übergeben werden. Ein Beispiel, das dies veranschaulicht, finden Sie unter [alternativer Code zum Codieren einer](alternate-code-for-encoding-an-enveloped-message.md)eingeschlossenen Nachricht.

10. Schließen Sie die Nachricht, indem Sie [**cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)aufrufen.

Das Ergebnis dieser Prozedur ist eine codierte Nachricht, die die ursprünglichen Daten, den verschlüsselten Hash der Daten (Signatur) und die Signatur Geber Informationen enthält. Es ist auch ein Zeiger auf das gewünschte, codierte BLOB vorhanden.

Weitere Informationen zur C-Codierung finden Sie [unter Beispiel c-Programm: Signieren, codieren, decodieren und Überprüfen einer Nachricht](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
