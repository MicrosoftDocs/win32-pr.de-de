---
description: Um zu ermitteln, ob es sich um einen eigenständigen oder absoluten Sicherheits Deskriptor handelt, müssen Sie die getsecuritydescriptorcontrol-Funktion aufrufen und das SE \_ Self \_ relative-Flag des \_ sicherheitsbeschreibungssteuerungsparameters überprüfen \_ .
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Absolute und Self-Relative Sicherheits Deskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57406e194a31e79594394913055609e2981e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959963"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Absolute und Self-Relative Sicherheits Deskriptoren

Eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) kann entweder das [*absolute*](/windows/desktop/SecGloss/a-gly) oder das [*selbst relative*](/windows/desktop/SecGloss/s-gly) Format aufweisen. Im absoluten Format enthält eine Sicherheits Beschreibung Zeiger auf Ihre Informationen, nicht auf die Informationen selbst. In einem selbst relativen Format speichert eine Sicherheits Beschreibung eine [**Sicherheits \_ beschreibungerstruktur**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) und zugehörige Sicherheitsinformationen in einem zusammenhängenden Speicherblock. Um zu ermitteln, ob es sich um einen eigenständigen oder absoluten Sicherheits Deskriptor handelt, müssen Sie die [**getsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) -Funktion aufrufen und das SE \_ Self \_ relative-Flag des [**\_ sicherheitsbeschreibungssteuerungsparameters \_**](security-descriptor-control.md) überprüfen. Sie können die Funktionen [**makeselfrelativesd**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) und [**makeabsolutesd**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) verwenden, um zwischen diesen beiden Formaten zu wechseln.

Das absolute Format ist hilfreich, wenn Sie eine Sicherheits Beschreibung entwickeln und Zeiger auf alle Komponenten haben, z. b. wenn die Standardeinstellungen für den Besitzer, die Gruppe und die freigegebene Zugriffs Steuerungs Liste verfügbar sind. In diesem Fall können Sie die [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) -Funktion aufrufen, um eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) zu initialisieren, und dann Funktionen wie " [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) " aufrufen, um der Sicherheits Beschreibung ACL-und sid-Zeiger zuzuweisen.

In einem selbst relativen Format beginnt eine Sicherheits Beschreibung immer mit einer [**\_ sicherheitsbeschreibungstruktur**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , aber die anderen Komponenten der Sicherheits Beschreibung können der Struktur in beliebiger Reihenfolge folgen. Anstatt Speicheradressen zu verwenden, werden die Komponenten der Sicherheits Beschreibung durch Offsets vom Anfang des Deskriptors identifiziert. Dieses Format ist nützlich, wenn eine Sicherheits Beschreibung auf einem Datenträger gespeichert, über ein Kommunikationsprotokoll übertragen oder in den Arbeitsspeicher kopiert werden muss.

Mit Ausnahme von [**makeabsolutesd**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd)wird bei allen Funktionen, die eine Sicherheits Beschreibung zurückgeben, das selbst relative Format verwendet. Sicherheits Deskriptoren, die als Argumente an eine Funktion übermittelt werden, können entweder ein selbst relativer oder ein absolutes Formular sein. Weitere Informationen finden Sie in der Dokumentation für die-Funktion.

 

 
