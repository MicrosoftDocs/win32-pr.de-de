---
description: Konfigurieren der Software Einschränkungs Richtlinie
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Konfigurieren der Software Einschränkungs Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041505"
---
# <a name="configuring-the-software-restriction-policy"></a>Konfigurieren der Software Einschränkungs Richtlinie

Wenn Sie die Vertrauens Ebenen der Software Einschränkungs Richtlinie in einer COM+-Anwendung explizit festlegen, überschreiben Sie die standardmäßigen systemweiten-Einstellungen. Dies ist häufig für com+-Server Anwendungen erforderlich, da die systemweite Vertrauens Ebene für alle Server Anwendungen identisch ist (da Sie alle in derselben Datei ausgeführt werden, dllhost.exe). Wenn Sie jedoch die Vertrauens Ebene der Software Einschränkungs Richtlinie einer COM+-Bibliotheks Anwendung festlegen, wirkt sich dies auf die systemweite Konfiguration für diese Anwendung aus. Eine Erläuterung zur Verwendung der Software Einschränkungs Richtlinie in com+ finden [Sie unter Verwenden der Software Einschränkungs Richtlinie in com+](using-the-software-restriction-policy-in-com-.md).

**So legen Sie die Software Einschränkungs Richtlinie fest**

1.  Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Software Einschränkungs Richtlinie festlegen, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .

3.  Aktivieren Sie unter **Software Einschränkungs Richtlinie** das Kontrollkästchen **Software Einschränkungs Richtlinie anwenden** . Dies ermöglicht es Ihnen, die Vertrauens Ebene festzulegen. Das Deaktivieren des Kontrollkästchens bewirkt, dass com+ die systemweite Konfiguration der Software Einschränkungs Richtlinie für die Anwendung verwendet. Dieses Kontrollkästchen entspricht der srpabled-Eigenschaft der [**Applications**](applications.md) -Auflistung.

4.  Wählen Sie im Feld **Einschränkungs Ebene** die geeignete Ebene aus. Dieses Dropdown Feld entspricht der SRPTrustLevel-Eigenschaft der [**Applications**](applications.md) -Auflistung. Die folgenden Ebenen sind von der niedrigsten zum vertrauenswürdigsten:

    -   Nicht **zulässig**. Die Anwendung ist nicht berechtigt, die vollständigen Berechtigungen des Benutzers zu verwenden. Komponenten mit Vertrauens Ebene können darin geladen werden.
    -   **Uneingeschränkt**. Die Anwendung hat uneingeschränkten Zugriff auf die Berechtigungen des Benutzers. Es können nur Komponenten mit einer uneingeschränkten Vertrauens Ebene in diese geladen werden.

5.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md)
</dt> <dt>

[Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Festlegen einer Authentifizierungs Ebene für eine Server Anwendung](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[Festlegen einer Identitätswechsel Ebene](setting-an-impersonation-level.md)
</dt> </dl>

 

 



