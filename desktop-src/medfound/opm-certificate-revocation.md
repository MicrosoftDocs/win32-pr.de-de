---
description: OPM-Zertifikatsperrung
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: OPM-Zertifikatsperrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b4caeace94f852394081620555c0b5b04918bf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478906"
---
# <a name="opm-certificate-revocation"></a>OPM-Zertifikatsperrung

Ein OPM-Zertifikat (Output Protection Manager) kann von Microsoft widerrufen werden. Die Liste der gesperrten Zertifikate wird in einer globalen Sperrliste (GRL) gespeichert. Die GRL hat das folgende Format:




| `Section` | BESCHREIBUNG | 
|---------|-------------|
| Header | Eine <a href="grl-header.md"><strong></strong></a> GRL_HEADER-Struktur. | 
| Core | Enthält die folgenden Sperrlisten:<ul><li>Kernelbinärsperren</li><li>Binäre Sperrungen im Benutzermodus</li><li>Zertifikatsperrungen</li><li>Vertrauenswürdige Stämme (reserviert)</li></ul>Die Liste der vertrauenswürdigen Stammverzeichnisse wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. | 
| Erweiterbare Einträge | Enthält Informationen, die von anderen Komponenten verwendet werden. Dieser Abschnitt ist für OPM nicht relevant. | 
| Erneuerungen: | Enthält GUIDs, die Windows Updatebezeichner definieren. Dieser Abschnitt enthält Bezeichner für die folgenden Listen:<ul><li>Kernelbinärsperren</li><li>Binäre Sperrungen im Benutzermodus</li><li>Zertifikatsperrungen</li></ul>Eine Anwendung kann diese Bezeichner verwenden, um eine erneuerte Version einer gesperrten Binärdatei anzufordern, sofern verfügbar. | 
| Signatur: Abschnitt "Core" | Signiert die Header- und Kernabschnitte. | 
| Signatur: Erweiterbarer Abschnitt | Signiert den Header und erweiterbare Abschnitte. | 




 

Der GRL-Header ist eine [**\_ GRL-HEADER-Struktur.**](grl-header.md) Der **dwSequenceNumber-Member** der -Struktur enthält die GRL-Versionsnummer. Diese Zahl wird erhöht, wenn die GRL aktualisiert und eine neue Version auf dem Computer des Benutzers platziert wird.

Gesperrte OPM-Zertifikate sind in der Zertifikatsperrliste des Abschnitts Core aufgeführt. Jeder Core-Eintrag in der GRL ist ein 20-Byte-Array, das den SHA-1-Hash des öffentlichen Schlüssels des gesperrten Zertifikats enthält.

Die Abschnitte Signatur enthalten Signaturen, mit denen überprüft werden kann, ob die GRL nicht manipuliert wurde. Jeder Signaturabschnitt enthält eine [**MF \_ SIGNATURE-Struktur.**](mf-signature.md) Die erste Signatur signiert den Header und den Core-Abschnitt. Die zweite Signatur signiert den Header und den Extensible-Abschnitt. Diese Signatur ist für OPM nicht relevant.

Überprüfen Sie die Signatur wie folgt, um sicherzustellen, dass die GRL selbst nicht manipuliert wurde:

1.  Suchen Sie den Anfang der [**MF \_ SIGNATURE-Struktur.**](mf-signature.md) Die Position der **MF \_ SIGNATURE-Struktur** wird im **cbSignatureCoreOffset-Member** der [**GRL \_ HEADER-Struktur**](grl-header.md) angegeben. Der Speicherort wird als Offset in Bytes ab dem Anfang der GRL angegeben.
2.  Analysieren Sie die [**MF \_ SIGNATURE-Struktur**](mf-signature.md) als PKCS \# 7-Signatur mit einer Zertifikatkette.
3.  Überprüfen Sie die Zertifikatkette bis zu einem vertrauenswürdigen Stamm.
4.  Vergewissern Sie sich, dass das Blattzertifikat über den folgenden Objektbezeichner in der EKU verfügt: "1.3.6.1.4.1.311.10.5.4".
5.  Berechnen Sie einen Hash der Bytes, die den Header und die Kernabschnitte der GRL enthalten.
6.  Überprüfen Sie, ob der Hash mit der Signatur im Blattzertifikat übereinstimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> <dt>

[**\_GRL-HEADER**](grl-header.md)
</dt> <dt>

[**MF \_ SIGNATURE**](mf-signature.md)
</dt> </dl>

 

 



