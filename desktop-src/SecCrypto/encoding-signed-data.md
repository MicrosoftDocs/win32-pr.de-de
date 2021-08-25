---
description: Beschreibt das Verfahren zum Codieren einer signierten Nachricht.
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: Codieren signierter Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e5c3ab338c4e7b251416f1a488747eb0c9b897c1fa02082afcb580cb12341b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874844"
---
# <a name="encoding-signed-data"></a>Codieren signierter Daten

[*Signierte Daten*](../secgloss/s-gly.md) bestehen aus Inhalten eines beliebigen Typs und verschlüsselten [*Nachrichtenhashes*](../secgloss/h-gly.md) des Inhalts von null oder mehr Signierern. Der resultierende Hash kann bestätigen, dass die ursprüngliche Nachricht seit dem Signieren nicht geändert wurde und dass bestimmte Personen oder Entitäten die Daten signiert haben.

Die folgende Abbildung zeigt das Verfahren zum Codieren einer signierten Nachricht. In der Liste, die auf die Abbildung folgt, werden die Schritte beschrieben.

Eine Nachricht kann mehrere Signierer, Hashalgorithmen und Zertifikate haben. Die Abbildung zeigt zwar nur Zertifikate, [*CRLs*](../secgloss/c-gly.md)und [*CTLs*](../secgloss/c-gly.md) können denselben Prozess verwenden. Sie würden überall dort in die Abbildung passen, wo Zertifikate angezeigt werden.

![Codieren einer signierten Nachricht](images/signmsg2.png)

Der allgemeine Prozess zum Codieren [*signierter Daten*](../secgloss/s-gly.md) lautet wie folgt.

**So codieren Sie signierte Daten**

1.  Die Daten werden erstellt (falls erforderlich), und ein Zeiger darauf wird abgerufen.
2.  Es [*wird ein Zertifikatspeicher*](../secgloss/c-gly.md) geöffnet, der das Zertifikat des Signers enthält.
3.  Der private Schlüssel für das Zertifikat wird abgerufen. Es gibt zwei Eigenschaften, die für das Zertifikat festgelegt werden müssen, bevor es verwendet wird. Eine wird verwendet, um ein Zertifikat an einen bestimmten CSP und innerhalb dieses CSP an einen bestimmten privaten [*Schlüsselcontainer zu binden.*](../secgloss/k-gly.md) Der andere wird verwendet, um anzugeben, welcher Hashalgorithmus verwendet werden soll, wenn ein [*Hashvorgang*](../secgloss/h-gly.md) aufgerufen wird. Diese müssen nur einmal festgelegt werden.
4.  Die -Eigenschaft eines Zertifikats bestimmt den Hashalgorithmus.
5.  Ein Hash der Daten wird durch Senden der Daten über die Hashfunktion erstellt.
6.  Die Signatur wird erstellt, indem der Hash mithilfe des privaten Schlüssels verschlüsselt wird, der über eine Eigenschaft im Zertifikat ermittelt wird.
7.  Die folgenden Daten sind in der fertig gestellten, signierten Nachricht enthalten:
    -   Die ursprünglichen zu signierten Daten
    -   Die Hashalgorithmen
    -   Die Signaturen
    -   Die Signatorinformationsstrukturen, die den Signatorbezeichner (Zertifikataussteller und Seriennummer) enthalten
    -   Zertifikate des Signers (optional)

Dieses Verfahren veranschaulicht einen einfachen Fall. Komplexere Fälle umfassen authentifizierte Attribute, die in der Nachricht enthalten sind. Wenn der Inhaltstyp eine **BYTE-Zeichenfolge** ist oder mindestens ein authentifiziertes Attribut zusammen mit einem beliebigen Datentyp vorgibt, sind zwei standardmäßig authentifizierte Attribute erforderlich: der Inhaltstyp (Daten) und der Hash des Inhalts. Unter diesen Umständen stellt [*die CryptoAPI*](../secgloss/c-gly.md) automatisch diese beiden erforderlichen Attribute zur Lage. Die Nachrichtenfunktionen auf niedriger Ebene hashen die authentifizierten Attribute, verschlüsseln den Hash mit dem privaten Schlüssel und stellen diese als Signatur zur Verfügung.

Verwenden Sie die Nachrichtenfunktionen auf niedriger Ebene, um die soeben aufgeführten Aufgaben mithilfe des folgenden Verfahrens auszuführen.

**So codieren Sie eine signierte Nachricht**

1.  Erstellen sie den Inhalt, oder rufen Sie den Inhalt ab.
2.  Hier erhalten Sie einen Kryptografieanbieter.
3.  Erhalten Sie die Signatorzertifikate.
4.  Initialisieren Sie [**die CMSG \_ SIGNER \_ ENCODE \_ INFO-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info)
5.  Initialisieren Sie die [**CMSG \_ SIGNED \_ ENCODE \_ INFO-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)
6.  Rufen [**Sie CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) auf, um die Größe des codierten Nachrichtenblobs zu erhalten. Ordnen Sie Arbeitsspeicher dafür zu.
7.  Rufen [**Sie CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)auf, und übergeben Sie CMSG SIGNED für dwMsgType und einen Zeiger auf \_ [**CMSG \_ SIGNED \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) für *pvMsgEncodeInfo,* um ein Handle für die geöffnete Nachricht zu erhalten. 
8.  Rufen [**Sie CryptMsgUpdate auf,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)und übergeben Sie das in Schritt 7 abgerufene Handle und einen Zeiger auf die Daten, die signiert und codiert werden sollen. Diese Funktion kann so oft wie nötig aufgerufen werden, um den Codierungsprozess abschließen zu können.
9.  Rufen [**Sie CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)auf, und übergeben Sie dabei das in Schritt 7 abgerufene Handle und die entsprechenden Parametertypen, um auf die gewünschten, codierten Daten zu zugreifen. Übergeben Sie beispielsweise CMSG CONTENT PARAM, um einen Zeiger auf die gesamte \_ \_ [*PKCS \# 7-Nachricht zu*](../secgloss/p-gly.md) erhalten.

    Wenn das Ergebnis dieser Codierung als [](../secgloss/i-gly.md) innere Daten für eine andere codierte Nachricht verwendet werden soll, z. B. eine umhumschlagte Nachricht, muss der PARAMETER CMSG \_ BARE \_ CONTENT \_ PARAM übergeben werden. Ein Beispiel, das dies zeigt, finden Sie unter [Alternativer Code für die Codierung einer umschlagten Nachricht.](alternate-code-for-encoding-an-enveloped-message.md)

10. Schließen Sie die Nachricht, indem Sie [**CryptMsgClose aufrufen.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)

Das Ergebnis dieser Prozedur ist eine codierte Nachricht, die die ursprünglichen Daten, den verschlüsselten Hash dieser Daten (Signatur) und die Signaturinformationen enthält. Es gibt auch einen Zeiger auf das gewünschte, codierte BLOB.

Weitere Informationen zur C-Codierung finden Sie unter [C-Beispielprogramm: Signieren, Codieren, Decodieren und Überprüfen einer Nachricht.](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)

 

 
