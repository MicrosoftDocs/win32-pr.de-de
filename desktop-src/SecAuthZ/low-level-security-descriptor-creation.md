---
description: Funktionen zum Erstellen eines Sicherheitsdeskriptors und Abrufen und Festlegen der Komponenten eines Sicherheitsdeskriptors.
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: Erstellen eines Low-Level-Sicherheitsdeskriptors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6462dcd7672836df5f2c1f6b368723bc3a9488eff290dc22a071ce40279def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781483"
---
# <a name="low-level-security-descriptor-creation"></a>Erstellen eines Low-Level-Sicherheitsdeskriptors

Die Zugriffssteuerung auf niedriger Ebene stellt [](/windows/desktop/SecGloss/s-gly) eine Reihe von Funktionen zum Erstellen eines Sicherheitsdeskriptors sowie zum Abrufen und Festlegen der Komponenten eines Sicherheitsdeskriptors zur Verfügung. Die Funktionen auf niedriger Ebene zum Initialisieren und Festlegen der Komponenten eines Sicherheitsdeskriptors funktionieren nur mit Sicherheitsdeskriptoren im absoluten Format. Die Funktionen auf niedriger Ebene zum Abrufen der Komponenten eines Sicherheitsdeskriptors funktionieren sowohl mit absoluten als auch [mit selbst relativen Sicherheitsdeskriptoren.](absolute-and-self-relative-security-descriptors.md)

Die [**InitializeSecurityDescriptor-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) initialisiert einen [**SECURITY \_ DESCRIPTOR-Puffer.**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) Der initialisierte Sicherheitsdeskriptor hat das [*absolute*](/windows/desktop/SecGloss/a-gly) Format und verfügt über keinen Besitzer, keine primäre Gruppe, keine DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) oder keine SACL (System [*Access Control*](/windows/desktop/SecGloss/s-gly) List). Sie können die folgenden Funktionen auf niedriger Ebene verwenden, um bestimmte Komponenten eines angegebenen Sicherheitsdeskriptors zu erhalten oder festzulegen.



| Funktion                                                             | BESCHREIBUNG                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | Ruft Revisions- und Steuerungsinformationen aus einem Sicherheitsdeskriptor ab.                                                                                                    |
| [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | Ruft die DACL aus einem Sicherheitsdeskriptor ab.                                                                                                                            |
| [**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | Ruft die [*Sicherheits-ID*](/windows/desktop/SecGloss/s-gly) (SID) der primären Gruppe aus einem Sicherheitsdeskriptor ab. |
| [**GetSecurityDescriptorLength**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | Gibt die Länge eines Sicherheitsdeskriptors zurück.                                                                                                                              |
| [**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | Ruft die Besitzer-SID aus einem Sicherheitsdeskriptor ab.                                                                                                                       |
| [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | Ruft die SACL aus einem Sicherheitsdeskriptor ab.                                                                                                                            |
| [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | Setzt eine DACL in einen Sicherheitsdeskriptor und ersetzt alle vorhandenen DACL-                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | Legt die primäre Gruppen-SID eines Sicherheitsdeskriptors fest.                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | Legt die Besitzer-SID einer Sicherheitsbeschreibung fest.                                                                                                                              |
| [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | Setzt eine SACL in einen Sicherheitsdeskriptor und ersetzt alle vorhandenen SACL-Dateien.                                                                                                    |



 

Um die Revisionsebene [](/windows/desktop/SecGloss/i-gly) und die strukturelle Integrität eines Sicherheitsdeskriptors zu überprüfen, rufen Sie die [**IsValidSecurityDescriptor-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor) auf.

 

 
