---
description: Funktionen zum Erstellen einer Sicherheits Beschreibung und zum erhalten und Festlegen der Komponenten einer Sicherheits Beschreibung.
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: Erstellung von Sicherheits Deskriptoren auf niedriger Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdafc99fe4d01c24e68a076aecc035843452205b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363690"
---
# <a name="low-level-security-descriptor-creation"></a>Erstellung von Sicherheits Deskriptoren auf niedriger Ebene

Die Zugriffs Steuerung auf niedrigerer Ebene bietet eine Reihe von Funktionen zum Erstellen einer [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) und zum Abrufen und Festlegen der Komponenten einer Sicherheits Beschreibung. Die Funktionen auf niedriger Ebene für die Initialisierung und das Festlegen der Komponenten einer Sicherheits Beschreibung funktionieren nur mit absoluten Formatierungs Deskriptoren. Die Funktionen auf niedriger Ebene zum erhalten der Komponenten einer Sicherheits Beschreibung funktionieren sowohl für [absolute als auch für selbst relative Sicherheits Deskriptoren](absolute-and-self-relative-security-descriptors.md).

Die [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) -Funktion initialisiert [**einen \_ sicherheitsbeschreibungerpuffer**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) . Die initialisierte Sicherheits Beschreibung weist das [*absolute*](/windows/desktop/SecGloss/a-gly) Format auf und hat keinen Besitzer, keine primäre Gruppe, keine DACL (freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) ) oder [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL). Sie können die folgenden Low-Level-Funktionen verwenden, um bestimmte Komponenten einer angegebenen Sicherheits Beschreibung zu erhalten oder festzulegen.



| Funktion                                                             | BESCHREIBUNG                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getsecuritydescriptor Control**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | Ruft Revisions-und Steuerungsinformationen aus einer Sicherheits Beschreibung ab.                                                                                                    |
| [**Getsecuritydescriptor DACL**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | Ruft die DACL aus einer Sicherheits Beschreibung ab.                                                                                                                            |
| [**Getsecuritydescriptorgroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | Ruft die primäre Gruppen [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) aus einer Sicherheits Beschreibung ab. |
| [**Getsecuritydescriptor length**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | Gibt die Länge eines Sicherheits Deskriptors zurück.                                                                                                                              |
| [**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | Ruft die Besitzer-SID aus einer Sicherheits Beschreibung ab.                                                                                                                       |
| [**Getsecuritydescriptor SACL**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | Ruft die SACL aus einer Sicherheits Beschreibung ab.                                                                                                                            |
| [**"SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | Fügt eine DACL in eine Sicherheits Beschreibung ein, wobei alle vorhandenen DACL ersetzt werden.                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | Legt die primäre Gruppen-SID einer Sicherheits Beschreibung fest.                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | Legt die Besitzer-SID einer Sicherheits Beschreibung fest.                                                                                                                              |
| [**SETSECURITYDESCRIPTOR SACL**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | Platziert eine SACL in eine Sicherheits Beschreibung und ersetzt jede vorhandene SACL.                                                                                                    |



 

Um die Revisions Ebene und die strukturelle [*Integrität*](/windows/desktop/SecGloss/i-gly) einer Sicherheits Beschreibung zu überprüfen, wenden Sie die [**IsValidSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor) -Funktion an.

 

 
