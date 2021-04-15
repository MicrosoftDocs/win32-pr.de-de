---
title: Übersicht über das Tutorial ADSI with Visual Basic
description: Active Directory ist eine zweckgebundene Datenbank \ 8212; Es handelt sich nicht um eine Registrierungs Ersetzung.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104555828"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Übersicht über das Tutorial: ADSI with Visual Basic

> [!Note]  
> Die folgende Dokumentation ist Teil einer erweiterten Szenariobeschreibung für Visual Basic-Entwickler. Eine allgemeine Übersicht über Active Directory finden Sie in der Dokumentation [zu IT-Experten auf TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)). Eine ausführlichere Betrachtung der Entwicklungsseite Active Directory finden Sie unter [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services). Eine größere Einführung in Active Directory-Dienst Schnittstellen finden Sie im übergeordneten Thema dieses Themas: [Active Directory Dienst Schnittstellen](active-directory-service-interfaces-adsi.md)sowie im gleich geordneten Thema: Informationen zu [Active Directory Dienst Schnittstellen](about-adsi.md).

 

Active Directory ist eine zweckgebundene Datenbank – es handelt sich nicht um eine Registrierungs Ersetzung. Das Verzeichnis ist für die Verarbeitung einer großen Anzahl von Lese-und Such Vorgängen und einer erheblich geringeren Anzahl von Änderungen und Updates konzipiert. Active Directory Daten sind hierarchisch, repliziert und erweiterbar. Da Sie repliziert wird, möchten Sie keine dynamischen Daten speichern, wie z. b. Aktienkurse oder CPU-Leistung. Wenn die Daten Computer spezifisch sind, speichern Sie die Daten in der Registrierung. Typische Beispiele für Daten, die im Verzeichnis gespeichert werden, sind Drucker Warteschlangen Daten, Benutzer Kontaktdaten und Netzwerk-/computerkonfigurationsdaten. Die Active Directory-Datenbank besteht aus Objekten und Attributen. Objekte und Attribut Definitionen werden im Active Directory Schema gespeichert.

Sie Fragen sich vielleicht, welche Objekte derzeit in Active Directory gespeichert werden. Active Directory hat drei Partitionen. Diese werden auch als Namenskontexte bezeichnet: Domäne, Schema und Konfiguration. Die Domänen Partition enthält Benutzer, Gruppen, Kontakte, Computer, Organisationseinheiten und viele andere Objekttypen. Da Active Directory erweiterbar ist, können Sie auch eigene Klassen und/oder Attribute hinzufügen. Die Schema Partition enthält Klassen und Attribut Definitionen. Die Konfigurations Partition enthält Konfigurationsdaten für Dienste, Partitionen und Standorte.

Der folgende Screenshot zeigt die Active Directory Domänen Partition.

![Active Directory-Domänen Partition](images/adadsi1.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Active Directory mithilfe Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Szenario: fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Erweiterte Themen](advanced-topics.md)
</dt> </dl>

 

 