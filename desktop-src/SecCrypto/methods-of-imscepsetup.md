---
description: Methoden, die von der unscepsetup-Schnittstelle definiert werden.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Methoden der imscep-Einrichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f543bb4525a3335128846ec5724e1a9a09a35f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526732"
---
# <a name="methods-of-imscepsetup"></a>Methoden der imscep-Einrichtung

Die folgenden Methoden werden von der [**imscepsetup**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) -Schnittstelle definiert. Die Eigenschaften Zugriffsmethoden werden hier nicht angezeigt. Informationen zu den Eigenschaften für **imscepsetup** finden Sie unter [Eigenschaften von imscepsetup](properties-of-imscepsetup.md).



| Methode                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getkeylängen List**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Ruft die Liste der vom angegebenen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) unterstützten [*Schlüssellängen*](../secgloss/k-gly.md) ab. |
| [**Getmscepsetupproperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Ruft einen Eigenschafts Wert für eine NDES-Konfiguration (Netzwerkgeräte Registrierungsdienst) ab.                                                                                                                                                                                               |
| [**Getprovidernamelist**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Ruft die Liste der CSPs ab, die auf dem Computer asymmetrische Schlüssel Signatur-und-Austausch Algorithmen bereitstellen.                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Initialisiert ein **cmscepsetup** -Objekt mit Standardwerten, um die Installation einer NDES-Rolle zu aktivieren.                                                                                                                                                                                  |
| [**Installieren**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Installiert eine Rolle gemäß der Konfiguration im **cmscepsetup** -Objekt.                                                                                                                                                                                                                      |
| [**Ismscepstoreempty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Gibt immer **Variant \_ true** zurück und sollte nicht verwendet werden.                                                                                                                                                                                                                          |
| [**"Postuninstall"**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Diese Methode ist nicht implementiert. Sie ist für eine zukünftige Verwendung reserviert.                                                                                                                                                                                                                    |
| [**Vordeinstallieren**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Entfernt die Registrierungs-und IIS-Einstellungen für die NDES-Rolle.                                                                                                                                                                                                                              |
| [**Setaccountinformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Legt die Benutzerkontoinformationen fest, die von der IIS NDES-Erweiterung zum Durchführen der Registrierung im Namen von Netzwerkgeräten verwendet werden.                                                                                                                                                              |
| [**Setmscepsetupproperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Legt einen Eigenschafts Wert für eine NDES-Konfiguration fest.                                                                                                                                                                                                                                  |



 

 

 
