---
description: Senden von COPP-Status Anforderungen
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Senden von COPP-Status Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745416"
---
# <a name="sending-copp-status-requests"></a>Senden von COPP-Status Anforderungen

Um eine zertifizierte COPP-Status Anforderung (Output Protection Protocol) zu senden, geben Sie eine [**amcoppstatusinput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) -Struktur mit den Anforderungs Daten ein. Die Strukturmember lauten wie folgt:

-   **rApp**. Eine 128-Bit-Zufallszahl, die als GUID typisiert ist. Die gleiche Zahl wird in der Antwort des Treibers zurückgegeben. Sie sollten die Zufallszahl auf dem Heap zuordnen und Sie dann in die Struktur kopieren. Dies schützt gegen Angriffe, bei denen der Angreifer den Inhalt der [**amcoppstatusinput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) -Struktur ändert.
-   **guidstatuus RequestId**. Eine GUID, die die Anforderung identifiziert. Siehe [COPP-Abfrage Verweis](copp-query-reference.md).
-   **dwsequence**. Die Status Sequenznummer. Erhöhen Sie diesen Wert nach jeder Status Anforderung. (Im Abschnitt [Initiieren einer COPP-Sitzung](initiating-a-copp-session.md)wird dieser Wert in den Codebeispielen als *ustatus-SEQ* angezeigt.)
-   **cbsizedata**. Die Größe (in Bytes) aller zusätzlichen Daten, die für die Anforderung benötigt werden.
-   **Statusdaten**. Daten für die Status Anforderung.

Übergeben Sie die [**amcoppstatusinput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) -Struktur an die [**iamcertifiedoutputprotection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) -Methode. Der folgende Code sendet z. b. eine Status Anforderung, mit der abgefragt wird, welche Schutzmechanismen verfügbar sind:


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



Die Antwort wird in den Member " **coppstatus** " der [**amcoppstatusoutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) -Struktur geschrieben. Die Größe der gültigen Daten in der Antwort wird im **cbsizedata** -Member angegeben. Um die Integrität der Nachricht sicherzustellen, berechnet der Treiber einen Mac (Message Authentication Code) mithilfe des OMAC 1-Algorithmus und gibt diesen Wert im **mackdi** -Member der Struktur zurück. Die Anwendung sollte diesen Wert wie folgt überprüfen:

1.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **mackdi** -Member der [**amcoppstatusoutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) -Struktur angezeigt wird (also **cbsizedata** Plus **coppstatus**).
2.  Vergleichen Sie dieses Tag mit dem Wert in **mackdi** mithilfe eines geraden **memcmp**.

Der OMAC 1-Algorithmus wird ausführlich unter beschrieben [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) . COPP verwendet die folgenden OMAC-1-Parameter:

-   E = AES
-   t = 128 Bits

Die von der Status Anforderung zurückgegebenen Daten beginnen immer mit zwei Elementen:

-   Der gleiche Wert von **rApp** , der von der Anwendung übermittelt wurde. Überprüfen Sie, ob dieser Wert mit dem auf dem Heap gespeicherten ursprünglichen Wert übereinstimmt.
-   Ein [**COPP \_ Statusflags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) -Wert, der angibt, ob sich der Status des Ausgabe Schutzes geändert hat.

Da die Verbindung verloren gehen oder neu konfiguriert werden kann, sollte die Anwendung den Treiber regelmäßig auf den aktuellen Statusabfragen. Wenn das COPP-Flag für die erneute Aushandlung \_ erforderlich ist, sollte die Anwendung versuchen, die Schutz Ebene zurückzusetzen. Wenn das COPP \_ linklost-Flag festgelegt ist, sollte die Anwendung die Wiedergabe des Inhalts abbrechen. Beispielsweise kann das COPP \_ linklost-Flag zurückgegeben werden, weil der Benutzer den ausgabeconnector getrennt hat. Die Anwendung sollte die aktuelle Instanz von VMR freigeben, eine neue Instanz von VMR erstellen und eine neue COPP-Sitzung einrichten (einschließlich Schlüsselaustausch und Zertifikat Überprüfung).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



