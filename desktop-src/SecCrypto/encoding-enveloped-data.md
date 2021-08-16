---
description: Kryptografische Nachrichtensyntax kann verwendet werden, um umhumhierte Nachrichten zu codieren.
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: Codieren von umhumhierten Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3517a956311373d067072899ee71bcdf742990877c7d569bfe4e5ef7f2757e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766760"
---
# <a name="encoding-enveloped-data"></a>Codieren von umhumhierten Daten

Umschlagdaten bestehen aus verschlüsselten Inhalten eines beliebigen Typs und verschlüsselten Sitzungsschlüsseln für die Inhaltsverschlüsselung für einen oder mehrere Empfänger. Umhumschlagene Nachrichten behalten den Inhalt des Nachrichtengeheimnis bei und erlauben nur angegebenen Personen oder Entitäten, den Inhalt abzurufen.

Kryptografische Nachrichtensyntax (CRYPTOGRAPHIC Message Syntax, CMS) kann verwendet werden, um umhumhierte Nachrichten zu codieren. CMS unterstützt drei Schlüsselverwaltungstechniken: Schlüsseltransport, Schlüsselvereinbarung und zuvor verteilte symmetrische Schlüsselverschlüsselungsschlüssel (KEK). Zuvor verteilte symmetrische KEK werden auch als Verteilung von Adressenlistenschlüsseln bezeichnet.

Bei jeder dieser drei Verfahren wird ein einzelner Sitzungsschlüssel generiert, um die umhumschlagte Nachricht zu verschlüsseln. Probleme bei der Schlüsselverwaltung befassen sich mit der Art und Weise, wie der Sitzungsschlüssel vom Absender verschlüsselt und von einem Empfänger entschlüsselt wird. Eine einzelne verschlüsselte Nachricht kann mithilfe einer Mischung der Schlüsselverwaltungstechniken an viele Empfänger verteilt werden.

Die Schlüsseltransportschlüsselverwaltung verwendet den öffentlichen Schlüssel eines beabsichtigten Empfängers, um den Sitzungsschlüssel zu verschlüsseln. Der Empfänger entschlüsselt den Sitzungsschlüssel mithilfe des privaten Schlüssels, der dem öffentlichen Schlüssel zugeordnet ist, der zum Verschlüsseln verwendet wurde. Der Empfänger verwendet dann den entschlüsselten Sitzungsschlüssel, um die umhedierten Daten zu entschlüsseln. Wenn der Schlüsseltransport verwendet wird, hat der Empfänger keine Informationen zur Identität des Absenders bestätigt.

Bei der Schlüsselvereinbarungsverwaltung wird ein temporärer, kurzlebiger Diffie-Hellman Schlüssel generiert und zum Verschlüsseln des Sitzungsschlüssels verwendet. Der öffentliche Schlüssel, der dem kurzlebigen privaten Schlüssel entspricht, ist als Teil der Empfängerinformationen der Nachricht enthalten. Der Empfänger entschlüsselt den Sitzungsschlüssel mithilfe des empfangenen kurzlebigen Schlüssels und verwendet diesen entschlüsselten Sitzungsschlüssel, um die umhedierte Nachricht zu entschlüsseln. Bei Verwendung einer kurzlebigen Schlüsselvereinbarung in Verbindung mit dem privaten Schlüssel des Empfängers hat der Nachrichtenempfänger informationen zur Identität des Absenders bestätigt.

Für die Schlüsselverwaltung mit zuvor verteilten [*symmetrischen*](../secgloss/s-gly.md)Schlüsseln enthält jede Nachricht den Inhaltsverschlüsselungsschlüssel, der mit einem zuvor verteilten Schlüsselverschlüsselungsschlüssel verschlüsselt wurde. Empfänger verwenden den zuvor verteilten Schlüsselverschlüsselungsschlüssel, um den Verschlüsselungsschlüssel für den Inhalt zu entschlüsseln, und verwenden dann den entschlüsselten Verschlüsselungsschlüssel für Inhalt, um die umgehdete Nachricht zu entschlüsseln.

In der folgenden Abbildung wird eine typische CMS-Sequenz von Ereignissen zum Codieren von umhumhierten Daten dargestellt.

![Codieren von umhumhierten Daten](images/envelmsg.png)

-   Ein Zeiger auf die [*Klartextnachricht*](../secgloss/p-gly.md) wird abgerufen.
-   Ein symmetrischer Schlüssel [*(Sitzung)*](../secgloss/s-gly.md)wird generiert.
-   Der [*symmetrische Schlüssel und*](../secgloss/s-gly.md) der angegebene Verschlüsselungsalgorithmus werden verwendet, um die Nachrichtendaten zu verschlüsseln.
-   Ein [*Zertifikatspeicher*](../secgloss/c-gly.md) wird geöffnet.
-   Das Zertifikat des Empfängers wird aus dem Speicher abgerufen.
-   Der [*öffentliche Schlüssel*](../secgloss/p-gly.md) wird aus dem Zertifikat des Empfängers abgerufen.
-   Mithilfe des öffentlichen Schlüssels des Empfängers wird der symmetrische Schlüssel verschlüsselt.
-   Aus dem Zertifikat des Empfängers wird die ID des Empfängers abgerufen.
-   Die folgenden Informationen sind in der Digital Enveloped Message enthalten: der Datenverschlüsselungsalgorithmus, die verschlüsselten Daten, der verschlüsselte symmetrische Schlüssel und die Empfängerinformationsstruktur.

Um Nachrichtenfunktionen auf niedriger Ebene zu verwenden, um die soeben aufgeführten typischen Aufgaben auszuführen, verwenden Sie das folgende Verfahren.

**So codieren Sie eine umhumschlagte Nachricht**

1.  Erstellen sie den Inhalt, oder rufen Sie den Inhalt ab.
2.  Hier erhalten Sie einen Kryptografieanbieter.
3.  Erhalten Sie ein Empfängerzertifikat.
4.  Initialisieren Sie die [**CMSG \_ ENVELOPED \_ ENCODE \_ INFO-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info)
5.  Rufen [**Sie CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) auf, um die Größe des codierten Nachrichtenblobs zu erhalten. Ordnen Sie Arbeitsspeicher dafür zu.
6.  Rufen [**Sie CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)auf, und übergeben Sie CMSG ENVELOPED für dwMsgType und einen Zeiger auf \_ [**CMSG \_ ENVELOPED \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) *für pvMsgEncodeInfo.*  Als Ergebnis dieses Aufrufs erhalten Sie ein Handle für die geöffnete Nachricht.
7.  Rufen [**Sie CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)auf, und übergeben Sie das in Schritt 6 abgerufene Handle und einen Zeiger auf die Daten, die verschlüsselt, umschlagen und codiert werden sollen. Diese Funktion kann so oft wie nötig aufgerufen werden, um den Codierungsprozess abschließen zu können.
8.  Rufen [**Sie CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)auf, und übergeben Sie dabei das in Schritt 6 abgerufene Handle und die entsprechenden Parametertypen, um auf die gewünschten, codierten Daten zu zugreifen. Übergeben Sie beispielsweise CMSG CONTENT PARAM, um einen Zeiger auf die gesamte \_ \_ PKCS \# 7-Nachricht zu erhalten.

    Wenn das Ergebnis dieser Codierung als [](../secgloss/i-gly.md) innere Daten für eine andere codierte Nachricht verwendet werden soll, z. B. eine umhumschlagte Nachricht, muss der PARAMETER CMSG \_ BARE \_ CONTENT \_ PARAM übergeben werden. Ein Beispiel finden Sie unter [Alternativer Code zum Codieren einer umschlagten Nachricht.](alternate-code-for-encoding-an-enveloped-message.md)

9.  Schließen Sie die Nachricht, indem Sie [**CryptMsgClose aufrufen.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)

Das Ergebnis dieser Prozedur ist eine codierte Nachricht, [](../secgloss/s-gly.md) die die verschlüsselten Daten, den symmetrischen Schlüssel, der mit den öffentlichen Schlüsseln des Empfängers verschlüsselt ist, und die Datenstrukturen der Empfängerinformationen enthält. Die Kombination aus verschlüsseltem Inhalt und einem verschlüsselten symmetrischen Schlüssel für einen Empfänger ist ein [*digitaler Umschlag*](../secgloss/d-gly.md) für diesen Empfänger. Jeder Inhaltstyp kann für mehrere Empfänger umschlagen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel C-Programm: Codieren einer umschlagenden, signierten Nachricht](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
