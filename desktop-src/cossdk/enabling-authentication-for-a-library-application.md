---
description: Aktivieren der Authentifizierung für eine Bibliotheksanwendung
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Aktivieren der Authentifizierung für eine Bibliotheksanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bceb3d5799ee8fac1d8eb266e6513c4d2a759adb10b78b2117424b08f8c5d6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736419"
---
# <a name="enabling-authentication-for-a-library-application"></a>Aktivieren der Authentifizierung für eine Bibliotheksanwendung

Da COM+-Bibliotheksanwendungen von anderen Prozessen gehostet werden, können sich ihre Sicherheitsanforderungen von denen von Serveranwendungen unterscheiden. Wenn die Bibliotheksanwendung von einem Browser gehostet wird, muss sie möglicherweise nicht authentifizierte Rückrufe empfangen.

Um diesen Bedarf zu erfüllen, können Sie die Authentifizierung deaktivieren, sodass der Hostingprozess keine Sicherheitsüberprüfungen für Aufrufer der Bibliotheksanwendung durchführt. Wenn Sie die Authentifizierung deaktivieren, werden Aufrufe der Bibliotheksanwendung effektiv nicht authentifiziert, da alle Aufrufe erfolgreich sind. Weitere Informationen finden Sie unter [Bibliotheksanwendungssicherheit.](library-application-security.md)

**So aktivieren (oder deaktivieren) Sie die Authentifizierung für eine Bibliotheksanwendung**

1.  Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Authentifizierung aktivieren oder deaktivieren, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit.**

3.  Aktivieren Sie unter **Authentifizierung** das Kontrollkästchen **Authentifizierung aktivieren,** um die Authentifizierung zu aktivieren. Wenn Sie das Kontrollkästchen deaktivieren, wird die Authentifizierung deaktiviert.

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen einer Authentifizierungsebene für eine Serveranwendung](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



