---
title: Verzeichnisdienst Funktionen (Netzwerkverwaltung)
description: Die Netzwerk Verwaltungsverzeichnis Dienst-Funktionen ermöglichen es Entwicklern, mit dem Domänen Controller und der Domänen Mitgliedschaft im Verzeichnisdienst zu arbeiten.
ms.assetid: 9eeb8f40-85c0-49db-a307-193703e4f463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e843e06762b4a7ef55b3f979b12a62ee6adf3
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104039826"
---
# <a name="directory-service-functions"></a>Verzeichnisdienst Funktionen

Die Netzwerk Verwaltungsverzeichnis Dienst-Funktionen ermöglichen es Entwicklern, mit dem Domänen Controller und der Domänen Mitgliedschaft im Verzeichnisdienst zu arbeiten.

Die Funktionen für den Netzwerk Verwaltungsverzeichnis Dienst sind nachfolgend aufgeführt.



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netaddalternativen Computername**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)       | Fügt einen alternativen Namen für den angegebenen Computer hinzu.                                                                                                                                          |
| [**"Nettenreeratecomputernames"**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)           | Listet die Namen für den angegebenen Computer auf.                                                                                                                                                |
| [**Netgetjoinableous**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                           | Ruft eine Liste der Organisationseinheiten (OUs) ab, in denen ein Computer Konto erstellt werden kann.                                                                                                  |
| [**Netgetjoininformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                   | Ruft joinstatusinformationen für den angegebenen Computer ab.                                                                                                                               |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                   | Fügt einen Computer einer Arbeitsgruppe oder einer Domäne hinzu.                                                                                                                                                  |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)       | Stellt ein Computer Konto für die spätere Verwendung in einem Offline-Domänen Beitritts Vorgang bereit.                                                                                                           |
| [**"Nettremuvealternativen Computername"**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername) | Entfernt einen alternativen Namen für den angegebenen Computer.                                                                                                                                       |
| [**"Nettrenamemachineindomain"**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)             | Ändert den Namen eines Computers in einer Domäne.                                                                                                                                                 |
| [**Netsetprimarycomputername**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)           | Legt den Namen des primären Computers für den angegebenen Computer fest.                                                                                                                                  |
| [**Netunjoindomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                               | Der Beitritt eines Computers zu einer Arbeitsgruppe oder einer Domäne wird von entfernt.                                                                                                                                            |
| [**Netvalidatename**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                               | Überprüft die Gültigkeit eines Computer namens, des Arbeitsgruppen namens oder des Domänen Namens.                                                                                                                   |



 

Weitere Informationen zum Programmieren für Active Directory finden Sie in der [Active Directory Referenz](/windows/desktop/AD/active-directory-domain-services-reference). Weitere Informationen zu Organisationseinheiten finden Sie unter [Verwalten von Benutzern](/windows/desktop/AD/managing-users) in der Active Directory-Dokumentation.

 

 