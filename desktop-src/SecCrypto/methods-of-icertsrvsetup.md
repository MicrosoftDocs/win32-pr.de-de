---
description: Die folgenden Methoden werden von der ICertSrvSetup-Schnittstelle definiert. Die Methoden für den Eigenschaftenzugriff werden hier nicht angezeigt. Die Eigenschaften für ICertSrvSetup finden Sie unter Eigenschaften von ICertSrvSetup.
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: Methoden von ICertSrvSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28274e1f59a4c229587f7e9f73222381ca89cff1a112ef7dc633f7a0c32dd434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407890"
---
# <a name="methods-of-icertsrvsetup"></a>Methoden von ICertSrvSetup

Die folgenden Methoden werden von der [**ICertSrvSetup-Schnittstelle**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) definiert. Die Methoden für den Eigenschaftenzugriff werden hier nicht angezeigt. Die Eigenschaften für **ICertSrvSetup** finden Sie unter [Eigenschaften von ICertSrvSetup.](properties-of-icertsrvsetup.md)



| Methode                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAImportPFX**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | Importiert ein Zertifizierungsstellenzertifikat und den zugehörigen privaten Schlüssel in den Speicher "LocalMachine".                                                                                                                                          |
| [**GetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | Ruft einen Eigenschaftswert für eine Zertifizierungsstellenkonfiguration ab.                                                                                                                                                                                                             |
| [**GetExistingCACertificates**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | Ruft die Auflistung von **CCertSrvSetupKeyInformation-Objekten** ab, die gültige Zertifizierungsstellenzertifikate darstellen, die derzeit auf dem Computer installiert sind.                                                                                                                  |
| [**GetHashAlgorithmList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | Ruft die Liste der Hashalgorithmen ab, die vom angegebenen [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) für einen Algorithmus für die asymmetrische Schlüsselsignatur unterstützt werden. |
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | Ruft die Liste der Schlüssellängen ab, die vom angegebenen CSP unterstützt werden.                                                                                                                                                                                              |
| [**GetPrivateKeyContainerList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | Ruft die Liste der Schlüsselcontainernamen ab, die vom angegebenen CSP für asymmetrische Signaturschlüsselalgorithmen gespeichert werden.                                                                                                                                                 |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | Ruft die Liste der CSPs ab, die asymmetrische Schlüsselsignaturalgorithmen auf dem Computer bereitstellen.                                                                                                                                                                   |
| [**GetSupportedCATypes**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | Ruft die Typen von ZS ab, die auf einem Computer unter dem Aufruferkontext installiert werden können.                                                                                                                                                                       |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | Initialisiert ein **CCertSrvSetup-Objekt** mit Standardwerten, um die Installation einer Zertifizierungsstellenrolle zu ermöglichen.                                                                                                                                                           |
| [**Installieren**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | Installiert eine Zertifizierungsstellenrolle, wie im **CCertSrvSetup-Objekt** konfiguriert.                                                                                                                                                                                         |
| [**IsPropertyEditable**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | Gibt dem Aufrufer an, ob eine angegebene Eigenschaft bearbeitet werden kann.                                                                                                                                                                                       |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | Ist nicht implementiert und für die zukünftige Verwendung reserviert.                                                                                                                                                                                                        |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | Speichert vorübergehend rollenspezifische Zustandsinformationen.                                                                                                                                                                                                        |
| [**SetCADistinguishedName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | Legt einen allgemeinen Namen der Zertifizierungsstelle und ein optionales Distinguished Name-Suffix fest.                                                                                                                                                                                          |
| [**SetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | Legt einen Eigenschaftswert für eine Zertifizierungsstellenkonfiguration fest.                                                                                                                                                                                                             |
| [**SetDatabaseInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | Legt die datenbankbezogenen Informationen für die Zertifizierungsstellenrolle fest.                                                                                                                                                                                                    |
| [**SetParentCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | Legt die Informationen der übergeordneten Zertifizierungsstelle für eine untergeordnete Zertifizierungsstellenkonfiguration fest.                                                                                                                                                                                        |
| [**SetWebCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | Legt die Informationen zur Zertifizierungsstelle für die Rolle ZS-Webregistrierung fest.                                                                                                                                                                                                   |



 

 

 
