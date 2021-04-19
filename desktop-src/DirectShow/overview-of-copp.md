---
description: Übersicht über COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Übersicht über COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342726"
---
# <a name="overview-of-copp"></a>Übersicht über COPP

Im folgenden finden Sie die grundlegenden Schritte, die eine Anwendung ausführen muss, um das Certified Output Protection Protocol (COPP) zu verwenden.

**Zertifikat Kette des Treibers erhalten**

1.  Erstellen Sie ein DirectShow-Wiedergabe Diagramm, das Video mit dem Video Mischungs-Renderer (VMR-7 oder VMR-9) oder dem [**erweiterten Videorenderer**](enhanced-video-renderer-filter.md) -Filter (EVR) rendert.
2.  Fragen Sie den VMR für die [**iamcertifiedoutputprotection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) -Schnittstelle ab.
3.  Nennen Sie [**iamcertifiedoutputprotection:: keyexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Diese Methode gibt eine 128-Bit-Zufallszahl aus dem Treiber zusammen mit einer Zertifikat Kette zurück, die den öffentlichen 2048-Bit-RSA-Schlüssel des Treibers enthält.

**Überprüfen der Zertifikat Kette**

1.  Überprüfen Sie die Zertifikat Kette. Wenn die Zertifikatskette ungültig ist, wird beendet.
2.  Überprüfen Sie die Zertifikat Sperr Liste. Wenn eines der Zertifikate in der Zertifikat Kette in der Sperr Liste angezeigt wird, wird beendet.
3.  Den öffentlichen RSA-Schlüssel aus der Zertifikat Kette erhalten.

**Initialisieren der COPP-Sitzung**

1.  Generieren Sie einen 128-Bit-AES-Sitzungsschlüssel. Dieser Schlüssel wird verwendet, um Daten zu signieren und zu überprüfen, ob signierte Daten nicht manipuliert wurden.
2.  Generieren Sie zwei kryptografisch sichere 32-Bit-Zufallszahlen. Der erste ist eine Status Sequenznummer, die zweite eine Befehlssequenz Nummer. Jedes Mal, wenn die Anwendung einen Befehl oder eine Status Anforderung sendet, erhöht Sie die entsprechende Sequenznummer und schließt diese Zahl in den COPP-Befehl oder die Anforderungs Daten ein.
3.  Verketten Sie die Zufallszahl 128-Bit aus dem Grafiktreiber, dem AES-Sitzungsschlüssel, der Status Sequenznummer und der Befehlssequenz Nummer. Verschlüsseln Sie dieses Bytearray mit dem öffentlichen Schlüssel des Treibers, und übergeben Sie das Ergebnis an [**iamcertifiedoutputprotection:: sessionsequencestart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).

**COPP-Befehle und-Status Anforderungen senden**

1.  Fragen Sie die verfügbaren Schutz Typen und andere Informationen ab, indem Sie [**iamcertifiedoutputprotection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus)aufrufen.
2.  Legen Sie die gewünschten Schutz Ebenen durch Aufrufen von [**iamcertifiedoutputprotection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand)fest.
3.  Fragen Sie regelmäßig die aktuelle lokale Schutz Ebene ab. Wiedergabe wird beendet, wenn die lokale Schutz Ebene unerwartet geändert wird oder wenn ein Problem erkannt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



