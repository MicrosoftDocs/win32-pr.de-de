---
title: 'Tutorial: Übersicht über ADSI mit Visual Basic'
description: Active Directory ist eine spezielle Datenbank \ 8212; es handelt sich nicht um einen Registrierungsersetzungs-.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cd6afe11b8991b6ced53367582ddf11d8eba0ea428105d3e9ba39c625d54fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082249"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Tutorialübersicht: ADSI mit Visual Basic

> [!Note]  
> Die folgende Dokumentation ist Teil einer erweiterten Szenariobeschreibung für Visual Basic Entwickler. Eine allgemeine Übersicht über Active Directory finden Sie in der DOKUMENTATION Pro [IT-Pro Technet.](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)) Einen detaillierteren Einblick in die Entwicklungsseite von Active Directory finden Sie unter [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services). Eine umfangreichere Einführung in Active Directory-Dienstschnittstellen finden Sie im übergeordneten Thema dieses Themas: Active Directory-Dienstschnittstellen sowie im nebengeordneten Thema: [Informationen zu Active Directory-Dienstschnittstellen](about-adsi.md). [](active-directory-service-interfaces-adsi.md)

 

Active Directory ist eine spezielle Datenbank– es handelt sich nicht um einen Registrierungsersetzungs-. Das Verzeichnis ist für die Handhabung einer großen Anzahl von Lese- und Suchvorgängen sowie einer deutlich geringeren Anzahl von Änderungen und Updates konzipiert. Active Directory-Daten sind hierarchisch, repliziert und erweiterbar. Da es repliziert wird, möchten Sie keine dynamischen Daten speichern, z. B. Aktienkurse des Unternehmens oder CPU-Leistung. Wenn Ihre Daten computerspezifisch sind, speichern Sie die Daten in der Registrierung. Typische Beispiele für im Verzeichnis gespeicherte Daten sind Druckerwarteschlangendaten, Benutzerkontaktdaten und Netzwerk-/Computerkonfigurationsdaten. Die Active Directory-Datenbank besteht aus Objekten und Attributen. Objekte und Attributdefinitionen werden im Active Directory-Schema gespeichert.

Möglicherweise fragen Sie sich, welche Objekte derzeit in Active Directory gespeichert sind. Active Directory verfügt über drei Partitionen. Diese werden auch als Namenskontexte bezeichnet: Domäne, Schema und Konfiguration. Die Domänenpartition enthält Benutzer, Gruppen, Kontakte, Computer, Organisationseinheiten und viele andere Objekttypen. Da Active Directory erweiterbar ist, können Sie auch eigene Klassen und/oder Attribute hinzufügen. Die Schemapartition enthält Klassen und Attributdefinitionen. Die Konfigurationspartition enthält Konfigurationsdaten für Dienste, Partitionen und Standorte.

Der folgende Screenshot zeigt die Active Directory-Domänenpartition.

![Active Directory-Domänenpartition](images/adadsi1.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Active Directory mit Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Szenario: Die Fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Erweiterte Themen](advanced-topics.md)
</dt> </dl>

 

 