---
description: Die folgenden Methoden werden von der icerzrvsetup-Schnittstelle definiert. Die Eigenschaften Zugriffsmethoden werden hier nicht angezeigt. Informationen zu den Eigenschaften von icerprvsetup finden Sie unter Eigenschaften von icerzrvsetup.
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: Methoden von icerzrvsetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a4e3482de2c8c62db854b86d21e739993bc3bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862839"
---
# <a name="methods-of-icertsrvsetup"></a>Methoden von icerzrvsetup

Die folgenden Methoden werden von der [**icerzrvsetup**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) -Schnittstelle definiert. Die Eigenschaften Zugriffsmethoden werden hier nicht angezeigt. Informationen zu den Eigenschaften von **icerprvsetup** finden Sie unter [Eigenschaften von icerzrvsetup](properties-of-icertsrvsetup.md).



| Methode                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Caimportpfx**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | Importiert ein Zertifizierungsstellen Zertifikat und den zugehörigen privaten Schlüssel in den Speicher "LocalMachine".                                                                                                                                          |
| [**Getcasetupproperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | Ruft einen Eigenschafts Wert für eine Zertifizierungsstellen Konfiguration ab.                                                                                                                                                                                                             |
| [**Getexistingcacertificates**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | Ruft die Auflistung von **ccertrvsetupkeyinformation** -Objekten ab, die gültige Zertifizierungsstellen Zertifikate darstellen, die zurzeit auf dem Computer installiert sind.                                                                                                                  |
| [**Gethashalgorithmlist**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | Ruft die Liste der vom angegebenen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) für einen Algorithmus für die asymmetrischen Schlüssel Signatur unterstützten Hash Algorithmen ab. |
| [**Getkeylängen List**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | Ruft die Liste der vom angegebenen CSP unterstützten Schlüssellängen ab.                                                                                                                                                                                              |
| [**Getprivatekeycontainerlist**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | Ruft die Liste der Schlüssel Container Namen ab, die vom angegebenen CSP für asymmetrische Signatur Schlüssel Algorithmen gespeichert werden.                                                                                                                                                 |
| [**Getprovidernamelist**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | Ruft die Liste der CSPs ab, die auf dem Computer asymmetrische Schlüssel Signatur Algorithmen bereitstellen.                                                                                                                                                                   |
| [**Getsupported-YPES**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | Ruft die Typen von Zertifizierungsstellen ab, die auf einem Computer im Aufruferkontext installiert werden können.                                                                                                                                                                       |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | Initialisiert ein **ccertrvsetup** -Objekt mit Standardwerten, um die Installation einer Zertifizierungsstellen Rolle zu aktivieren.                                                                                                                                                           |
| [**Installieren**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | Installiert eine Zertifizierungsstellen Rolle, wie im **ccerzrvsetup** -Objekt konfiguriert.                                                                                                                                                                                         |
| [**Ispropertyeditable**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | Gibt dem Aufrufer an, ob eine angegebene Eigenschaft bearbeitet werden kann.                                                                                                                                                                                       |
| [**"Postuninstall"**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | Ist nicht implementiert und ist für die zukünftige Verwendung reserviert.                                                                                                                                                                                                        |
| [**Vordeinstallieren**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | Speichert temporär Rollen spezifische Zustandsinformationen.                                                                                                                                                                                                        |
| [**Setcaerkennbar shedname**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | Legt einen allgemeinen Namen für die Zertifizierungsstelle und ein optionales Distinguished Name-Suffix fest.                                                                                                                                                                                          |
| [**Setcasetupproperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | Legt einen Eigenschafts Wert für eine Zertifizierungsstellen Konfiguration fest.                                                                                                                                                                                                             |
| [**Setdatabaseinformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | Legt die Daten Bank bezogenen Informationen für die Zertifizierungsstellen Rolle fest.                                                                                                                                                                                                    |
| [**SetParser**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | Legt die Informationen der übergeordneten Zertifizierungsstelle für eine untergeordnete Zertifizierungsstellen Konfiguration fest                                                                                                                                                                                        |
| [**Setwebcainformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | Legt die Zertifizierungsstellen Informationen für die ZS-Webregistrierungs Rolle fest.                                                                                                                                                                                                   |



 

 

 
