---
title: Bibliotheks Zugriff
description: Bibliotheks Zugriff
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player-Bibliothek, Zugriff
- Bibliothek, zugreifen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309979"
---
# <a name="library-access"></a>Bibliotheks Zugriff

Eigenschaften und Methoden des Windows Media Player-Objektmodells, die auf die Bibliothek zugreifen, benötigen entweder Lese-oder Lese-/Schreibzugriff auf die Datenbank. Die Bibliothek enthält Informationen, die einige Benutzer als privat aufbewahren möchten und auf die nur mit Ihrer Zustimmung zugegriffen werden soll.

Für Windows Media Player 9-Serie oder höher können Sie die Zugriffsebene Programm gesteuert festlegen. Rufen Sie die *Einstellungen* ab, um die aktuelle Zugriffsebene zu ermitteln, die dem Code gewährt wurde. **mediaaccessrights** -Eigenschaft. Diese Eigenschaft gibt "None", "Read" oder "Full" (Lese-/Schreibzugriff) zurück. Um bestimmte Zugriffsrechte anzufordern, müssen Sie die *Einstellungen* aufrufen. **requestmediaaccessrights** -Methode, die einen Parameter übergibt, der die von Ihnen angeforderte Ebene angibt. Die-Methode zeigt dem Benutzer eine Meldung an, die die angeforderte Zugriffsebene erläutert, und gibt einen **booleschen** Wert zurück, der angibt, ob der Zugriff gewährt wurde.

Bestimmte Zugriffsrechte werden automatisch abhängig davon erteilt, wo der Code in Relation zum Computer des Benutzers ausgeführt wird.

-   Wenn sich die Webseite oder das Programm auf dem Computer des Benutzers befindet, werden standardmäßig vollständige Zugriffsrechte gewährt.
-   Webseiten haben Lesezugriff auf den *Player*. **currentMedia**, *Player*. **currentwiedergabe** und *Medium*. **SourceUrl** , wenn sich die Webseite in einer Internet Explorer-Sicherheitszone befindet, die der gleichen oder weniger eingeschränkt ist als die Sicherheitszone des Medien Elements oder der Wiedergabeliste.

    Die Sicherheitszonen reichen von der geringsten Beschränkung bis zu den am meisten eingeschränkten Einschränkungen, sind die **Vertrauenswürdige** Zone (einschließlich des lokalen Computers des Benutzers), die **lokale Intranetzone** , die **Internet** Zone und die **Eingeschränkte** Zone.

    Beispielsweise verfügt eine Webseite in der **lokalen Intranetzone** über vollständige Zugriffsrechte für *Player*. **currentMedia** wenn sich das entsprechende Medien Element im lokalen Intranet oder im Internet befindet, müssen Zugriffsrechte für Medienelemente, die sich auf dem lokalen Computer eines Benutzers oder auf einer Website in der **vertrauenswürdigen** Zone befinden, angefordert werden.

Sie sollten Ihre webbasierte oder Windows-basierte Anwendung in allen Sicherheitszonen testen, auf die Sie möglicherweise stoßen. Die Anwendung sollte so entworfen werden, dass Denial-of-Access-Anforderungen ordnungsgemäß verarbeitet werden.

Für Windows Media Player-Objektmodell Versionen vor Windows Media Player 9-Reihe sind **mediaaccessrights** oder **requestmediaaccessrights** nicht enthalten. Diese früheren Versionen von Windows Media Player es dem Benutzer ermöglichen, Zugriffsebenen mithilfe des Dialog Felds **Optionen** festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> <dt>

[**Arbeiten mit der Bibliothek**](working-with-the-library.md)
</dt> </dl>

 

 




