---
description: Die Syntax der kryptografischen Nachricht kann verwendet werden, um eingeschlossene Nachrichten zu codieren.
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: Codieren von eingeschlossenen Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dc20fc7483ba1ef364d8b59824d26bd14d458d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567812"
---
# <a name="encoding-enveloped-data"></a>Codieren von eingeschlossenen Daten

Eingeschlossene Daten bestehen aus verschlüsseltem Inhalt beliebiger Typen und verschlüsselten Inhalts Verschlüsselungs-Sitzungs Schlüsseln für einen oder mehrere Empfänger. Eingeschlossene Nachrichten behalten den Inhalt des geheimen Schlüssels der Nachricht bei und erlauben nur bestimmten Personen oder Entitäten, den Inhalt abzurufen.

Cryptographic Message Syntax (CMS) kann verwendet werden, um eingeschlossene Nachrichten zu codieren. CMS unterstützt drei Schlüssel Verwaltungsverfahren: Schlüssel Transport, Schlüssel Übereinstimmung und zuvor verteilte symmetrische Schlüssel Verschlüsselungsschlüssel (KEK). Zuvor verteilter symmetrischer KEK wird auch als "Mailing List Key Distribution" bezeichnet.

In jeder dieser drei Verfahren wird ein einzelner Sitzungsschlüssel generiert, um die eingeschlossene Nachricht zu verschlüsseln. Wichtige Verwaltungsprobleme behandeln die Art und Weise, wie der Sitzungsschlüssel vom Absender verschlüsselt und von einem Empfänger entschlüsselt wird. Eine einzelne verschlüsselte Nachricht kann mithilfe einer Mischung aus den Schlüssel Verwaltungsverfahren an viele Empfänger verteilt werden.

Die Schlüsselverwaltung des Schlüssel Transports verwendet den öffentlichen Schlüssel eines beabsichtigten Empfängers, um den Sitzungsschlüssel zu verschlüsseln. Der Empfänger entschlüsselt den Sitzungsschlüssel mithilfe des privaten Schlüssels, der dem öffentlichen Schlüssel zugeordnet ist, der für die Verschlüsselung verwendet wurde. Der Empfänger verwendet dann den entschlüsselten Sitzungsschlüssel, um die eingeschlossenen Daten zu entschlüsseln. Bei Verwendung des Schlüssel Transports hat der Empfänger keine Informationen über die Identität des Absenders bestätigt.

In der Schlüssel Vereinbarungs Verwaltung wird ein temporärer, kurzlebiger Diffie-Hellman privater Schlüssel generiert und verwendet, um den Sitzungsschlüssel zu verschlüsseln. Der öffentliche Schlüssel, der dem kurzlebigen privaten Schlüssel entspricht, ist als Teil der Empfängerinformationen der Nachricht enthalten. Der Empfänger entschlüsselt den Sitzungsschlüssel mit dem empfangenen kurzlebigen Schlüssel und verwendet diesen entschlüsselten Sitzungsschlüssel, um die eingeschlossene Nachricht zu entschlüsseln. Mithilfe der kurzlebigen Schlüssel Vereinbarung in Verbindung mit dem privaten Schlüssel des Empfängers verfügt der Nachrichtenempfänger über bestätigte Informationen über die Identität des Absenders.

Bei der Schlüsselverwaltung mit zuvor verteilten [*symmetrischen Schlüsseln*](../secgloss/s-gly.md)enthält jede Nachricht den Inhalts Verschlüsselungsschlüssel, der mit einem zuvor verteilten Schlüssel Verschlüsselungsschlüssel verschlüsselt wurde. Empfänger verwenden den zuvor verteilten Schlüssel Verschlüsselungsschlüssel zum Entschlüsseln des Inhalts Verschlüsselungsschlüssels. verwenden Sie dann den entschlüsselten Inhalts Verschlüsselungsschlüssel, um die eingeschlossene Nachricht zu entschlüsseln.

In der folgenden Abbildung ist eine typische CMS-Sequenz von Ereignissen für die Codierung von eingeschlossenen Daten dargestellt.

![Codieren von eingeschlossenen Daten](images/envelmsg.png)

-   Ein Zeiger auf die [*Klartext*](../secgloss/p-gly.md) -Nachricht wird abgerufen.
-   Ein symmetrischer ([*Sitzungs*](../secgloss/s-gly.md)-) Schlüssel wird generiert.
-   Der [*symmetrische Schlüssel*](../secgloss/s-gly.md) und der angegebene Verschlüsselungsalgorithmus werden verwendet, um die Nachrichten Daten zu verschlüsseln.
-   Ein [*Zertifikat Speicher*](../secgloss/c-gly.md) wird geöffnet.
-   Das Zertifikat des Empfängers wird aus dem Speicher abgerufen.
-   Der [*öffentliche Schlüssel*](../secgloss/p-gly.md) wird aus dem Zertifikat des Empfängers abgerufen.
-   Mithilfe des öffentlichen Schlüssels des Empfängers wird der symmetrische Schlüssel verschlüsselt.
-   Aus dem Zertifikat des Empfängers wird die ID des Empfängers abgerufen.
-   Die folgenden Informationen sind in der Digital umgerufenen Nachricht enthalten: der Daten Verschlüsselungsalgorithmus, die verschlüsselten Daten, der verschlüsselte symmetrische Schlüssel und die Struktur der Empfängerinformationen.

Verwenden Sie das folgende Verfahren, wenn Sie Nachrichten Funktionen auf niedriger Ebene verwenden möchten, um die gerade aufgelisteten Aufgaben zu erledigen.

**So codieren Sie eine eingeschlossene Nachricht**

1.  Erstellen oder Abrufen des Inhalts.
2.  Verschaffen Sie sich einen Kryptografieanbieter.
3.  Erhalten Sie ein Empfänger Zertifikat.
4.  Initialisieren Sie die eingefügte CMSG-Struktur zum [**\_ \_ Codieren von \_ Informationen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) .
5.  Sie können [**cryptmsgcalculateencodedlength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) aufrufen, um die Größe des codierten nachrichtenblobs zu erhalten. Arbeitsspeicher zuweisen.
6.  Nennen Sie [**cryptmsgopentoencode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), und übergeben Sie CMSG \_ für *dwmsgtype* und einen Zeiger auf [**CMSG \_ enveloped \_ encode \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) for *pvmsgencodeinfo*. Als Ergebnis dieses Aufrufes wird ein Handle für die geöffnete Nachricht angezeigt.
7.  Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), und übergeben Sie das in Schritt 6 abgerufene Handle und einen Zeiger auf die zu verschlüsselnden, umschlossenen und codierten Daten. Diese Funktion kann so oft wie nötig aufgerufen werden, um den Codierungsprozess abzuschließen.
8.  Aufrufen von [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), übergeben des in Schritt 6 abgerufenen Handles und der entsprechenden Parametertypen für den Zugriff auf die gewünschten, codierten Daten. Übergeben Sie z. b. CMSG \_ Content \_ param, um einen Zeiger auf die gesamte PKCS 7-Nachricht zu erhalten \# .

    Wenn das Ergebnis dieser Codierung als [*innere Daten*](../secgloss/i-gly.md) für eine andere codierte Nachricht verwendet werden soll, z. b. eine eingeschlossene Nachricht, muss der CMSG-Parameter für den \_ Bare-Content- \_ \_ Parameter übergeben werden. Ein Beispiel finden Sie unter [alternativer Code zum Codieren einer](alternate-code-for-encoding-an-enveloped-message.md)eingeschlossenen Nachricht.

9.  Schließen Sie die Nachricht, indem Sie [**cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)aufrufen.

Das Ergebnis dieser Prozedur ist eine codierte Nachricht, die die verschlüsselten Daten, den [*symmetrischen Schlüssel*](../secgloss/s-gly.md) , der mit den öffentlichen Schlüsseln des Empfängers verschlüsselt ist, und die Datenstrukturen der Empfängerinformationen enthält. Die Kombination aus verschlüsseltem Inhalt und einem verschlüsselten symmetrischen Schlüssel für einen Empfänger ist ein [*digitaler Umschlag*](../secgloss/d-gly.md) für diesen Empfänger. Jeder Inhaltstyp kann für mehrere Empfänger umgehüllt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel-C-Programm: Codieren einer eingeschlossenen, signierten Nachricht](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
