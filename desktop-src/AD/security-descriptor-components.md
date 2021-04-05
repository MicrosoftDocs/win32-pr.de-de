---
title: Sicherheitsbeschreibungenkomponenten
description: Wenn Sie die IADs. Get-Methode zum Abrufen eines IADsSecurityDescriptor-Schnittstellen Zeigers verwendet haben, können Sie die IADsSecurityDescriptor-Eigenschaften verwenden, um die Komponenten der Sicherheits Beschreibung eines Verzeichnis Objekts zu lesen oder zu schreiben.
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- Sicherheits Deskriptor-Komponenten AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef87b0e23f60fdbb4d0b03b421012d5918ed3c83
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724424"
---
# <a name="security-descriptor-components"></a>Sicherheitsbeschreibungenkomponenten

Wenn Sie die [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) -Methode zum Abrufen eines [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) -Schnittstellen Zeigers verwendet haben, können Sie die **IADsSecurityDescriptor** -Eigenschaften verwenden, um die Komponenten der Sicherheits Beschreibung eines Verzeichnis Objekts zu lesen oder zu schreiben. Um z. b. die DACL des Objekts zu erhalten oder festzulegen, verwenden Sie die Eigenschaft " [**diskretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) ".

In einer Sicherheits Beschreibung können die folgenden Daten gespeichert werden:

-   Eine Sicherheits-ID (SID), mit der der Besitzer des Objekts identifiziert wird: der Besitzer eines Objekts verfügt über das implizite Recht, die DACL-und Besitzer Daten in der Sicherheits Beschreibung des Objekts zu ändern.
-   Eine freigegebene Zugriffs Steuerungs Liste (DACL), mit der die Benutzer und Gruppen identifiziert werden, die verschiedene Vorgänge für das Objekt ausführen können: eine DACL enthält eine Liste von Zugriffs Steuerungs Einträgen (ACEs). Jeder ACE ermöglicht oder verweigert einem angegebenen Benutzerkonto, Gruppenkonto oder anderen Vertrauens nehmer einen angegebenen Satz von Zugriffsrechten. Weitere Informationen finden Sie unter [Abrufen der DACL eines Objekts](retrieving-an-objectampaposs-dacl.md).
-   Eine SACL (System Access-Control List), mit der gesteuert wird, wie die System Überwachungen versuchen, auf das Objekt zuzugreifen: Jeder ACE in einer SACL gibt die Arten von Zugriffsversuchen an, mit denen ein Überwachungs Protokolleintrag für ein bestimmtes Benutzerkonto, ein Gruppenkonto oder einen anderen Vertrauens nehmer generiert wird. Weitere Informationen finden Sie unter [Abrufen der SACL eines Objekts](retrieving-an-objectampaposs-sacl.md).
-   Ein Satz von steuerungssteuerungsflags für die **Sicherheits \_ \_ Beschreibung** , die die Bedeutung einer Sicherheits Beschreibung oder ihrer Komponenten qualifizieren. beispielsweise schützt das Flag " **SE \_ DACL \_ Protected** " die DACL der Sicherheits Beschreibung vor der Vererbung von ACEs von ihrem übergeordneten Objekt.
-   Eine Sicherheits-ID (SID), die die primäre Gruppe des Objekts identifiziert: Active Directory Domain Services diese Komponente nicht verwenden.

Weitere Informationen und ein Codebeispiel, das zum Lesen und Anzeigen der Daten in einer Objekt Sicherheits Beschreibung und DACL verwendet werden kann, finden Sie unter [Lesen der Sicherheits Beschreibung eines Objekts](reading-an-objectampaposs-security-descriptor.md).

 

 