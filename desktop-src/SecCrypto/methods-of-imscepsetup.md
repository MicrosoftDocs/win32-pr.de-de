---
description: Von der IMSCEPSetup-Schnittstelle definierte Methoden.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Methoden von IMSCEPSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7dcadeb6c3815a37f1b1e87453a7ff737c70f53d76e0904bc67211ed7028f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622230"
---
# <a name="methods-of-imscepsetup"></a>Methoden von IMSCEPSetup

Die folgenden Methoden werden von der [**IMSCEPSetup-Schnittstelle**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) definiert. Die Methoden für den Eigenschaftenzugriff werden hier nicht angezeigt. Die Eigenschaften für **IMSCEPSetup** finden Sie unter [Eigenschaften von IMSCEPSetup](properties-of-imscepsetup.md).



| Methode                                                             | Beschreibung                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Ruft die Liste der [*Schlüssellängen ab,*](../secgloss/k-gly.md) die vom angegebenen [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) unterstützt werden. |
| [**GetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Ruft einen Eigenschaftswert für eine NDES-Konfiguration (Registrierungsdienst für Netzwerkgeräte) ab.                                                                                                                                                                                               |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Ruft die Liste der CSPs ab, die asymmetrische Schlüsselsignaturen und Austauschalgorithmen auf dem Computer bereitstellen.                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Initialisiert ein **CMSCEPSetup-Objekt** mit Standardwerten, um die Installation einer NDES-Rolle zu ermöglichen.                                                                                                                                                                                  |
| [**Installieren**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Installiert eine Rolle wie im **CMSCEPSetup-Objekt** konfiguriert.                                                                                                                                                                                                                      |
| [**IsMSCEPStoreEmpty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Gibt immer **VARIANT \_ TRUE** zurück und sollte nicht verwendet werden.                                                                                                                                                                                                                          |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Diese Methode ist nicht implementiert. Sie ist für eine zukünftige Verwendung reserviert.                                                                                                                                                                                                                    |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Entfernt die Registrierungs- und IIS-Einstellungen für die NDES-Rolle.                                                                                                                                                                                                                              |
| [**SetAccountInformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Legt die Benutzerkontoinformationen fest, die von der IIS-NDES-Erweiterung zum Durchführen der Registrierung für Netzwerkgeräte verwendet werden.                                                                                                                                                              |
| [**SetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Legt einen Eigenschaftswert für eine NDES-Konfiguration fest.                                                                                                                                                                                                                                  |



 

 

 
