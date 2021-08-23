---
title: Sicherheitsbeschreibungskomponenten
description: Nachdem Sie die IADs.Get-Methode zum Abrufen eines IADsSecurityDescriptor-Schnittstellenzeigers verwendet haben, können Sie die IADsSecurityDescriptor-Eigenschaften verwenden, um die Komponenten des Sicherheitsdeskriptors eines Verzeichnisobjekts zu lesen oder zu schreiben.
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- Sicherheitsbeschreibungskomponenten AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aa5ec61507e56c03bcc3809a2a5eebcb2cbcd36e18f63119aca53448c8a0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024918"
---
# <a name="security-descriptor-components"></a>Sicherheitsbeschreibungskomponenten

Nachdem Sie die [**IADs.Get-Methode**](/windows/desktop/api/iads/nf-iads-iads-get) zum Abrufen eines [**IADsSecurityDescriptor-Schnittstellenzeigers**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) verwendet haben, können Sie die **IADsSecurityDescriptor-Eigenschaften** verwenden, um die Komponenten des Sicherheitsdeskriptors eines Verzeichnisobjekts zu lesen oder zu schreiben. Verwenden Sie beispielsweise die [**DiscretionaryAcl-Eigenschaft,**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) um die DACL des Objekts zu erhalten oder zu festlegen.

Ein Sicherheitsdeskriptor kann die folgenden Daten speichern:

-   Eine Sicherheits-ID (SID), die den Besitzer des Objekts identifiziert: Der Besitzer eines Objekts hat das implizite Recht, die DACL- und Besitzerdaten in der Sicherheitsbeschreibung des Objekts zu ändern.
-   Eine DACL (Discretionary Access Control List), die die Benutzer und Gruppen identifiziert, die verschiedene Vorgänge für das Objekt ausführen können: Eine DACL enthält eine Liste mit Zugriffssteuerungseinträgen (ACEs). Jeder ACE lässt einen angegebenen Satz von Zugriffsrechten für ein angegebenes Benutzerkonto, gruppenkonto oder einen anderen Vertrauenshänder zu oder verweigert diesen. Weitere Informationen finden Sie unter [Abrufen der DACL eines Objekts.](retrieving-an-objectampaposs-dacl.md)
-   Eine Systemzugriffssteuerungsliste (SACL), die steuert, wie das System versucht, auf das Objekt zu zugreifen: Jeder ACE in einer SACL gibt die Zugriffsversuche an, die einen Überwachungsprotokolleintrag für ein angegebenes Benutzerkonto, Gruppenkonto oder einen anderen Vertrauensinhaber generieren. Weitere Informationen finden Sie unter [Abrufen der SACL eines Objekts.](retrieving-an-objectampaposs-sacl.md)
-   Ein Satz von **SECURITY \_ DESCRIPTOR CONTROL-Steuerelementflags, \_** die die Bedeutung eines Sicherheitsdeskriptors oder seiner Komponenten qualifizieren: Beispielsweise schützt das **\_ DACL \_** PROTECTED-Flag von SE die DACL des Sicherheitsdeskriptors vor dem Erben von ACEs von seinem übergeordneten Objekt.
-   Eine Sicherheits-ID (SID), die die primäre Gruppe des Objekts identifiziert: Active Directory Domain Services diese Komponente nicht verwenden.

Weitere Informationen und ein Codebeispiel, das zum Lesen und Anzeigen der Daten in einem Objektsicherheitsdeskriptor und einer DACL verwendet werden kann, finden Sie unter Lesen des Sicherheitsdeskriptors eines [Objekts.](reading-an-objectampaposs-security-descriptor.md)

 

 