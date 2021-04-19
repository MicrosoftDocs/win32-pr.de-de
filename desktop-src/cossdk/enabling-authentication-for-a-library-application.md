---
description: Aktivieren der Authentifizierung für eine Bibliotheks Anwendung
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Aktivieren der Authentifizierung für eine Bibliotheks Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346029"
---
# <a name="enabling-authentication-for-a-library-application"></a>Aktivieren der Authentifizierung für eine Bibliotheks Anwendung

Da com+-Bibliotheksanwendungen von anderen Prozessen gehostet werden, unterscheiden sich die Sicherheitsanforderungen möglicherweise von denen der Server Anwendungen. Wenn die Bibliotheks Anwendung von einem Browser gehostet wird, muss Sie möglicherweise nicht authentifizierte Rückrufe empfangen.

Um diese Anforderung zu erfüllen, können Sie die Authentifizierung deaktivieren, sodass der Hostingprozess keine Sicherheitsüberprüfungen für Aufrufer der Bibliotheks Anwendung ausführt. Wenn Sie die Authentifizierung deaktivieren, werden Aufrufe der Bibliotheks Anwendung nicht authentifiziert – alle Aufrufe an diese werden erfolgreich ausgeführt. Weitere Informationen finden Sie unter [Bibliotheks Anwendungssicherheit](library-application-security.md).

**So aktivieren (oder deaktivieren) Sie die Authentifizierung für eine Bibliotheks Anwendung**

1.  Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Authentifizierung aktivieren bzw. deaktivieren, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .

3.  Aktivieren Sie unter **Authentifizierung** das Kontrollkästchen **Authentifizierung aktivieren** , um die Authentifizierung zu aktivieren. durch Deaktivieren des Kontrollkästchens wird die Authentifizierung deaktiviert.

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen einer Authentifizierungs Ebene für eine Server Anwendung](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



