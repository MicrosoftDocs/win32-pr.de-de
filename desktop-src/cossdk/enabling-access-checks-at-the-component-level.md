---
description: Aktivieren von Zugriffsüberprüfungen auf Komponentenebene
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Aktivieren von Zugriffsüberprüfungen auf Komponentenebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3063873923d3d4c491312ca4efccd9bcd665b46bf1bdfc882b69dbe4942757f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047468"
---
# <a name="enabling-access-checks-at-the-component-level"></a>Aktivieren von Zugriffsüberprüfungen auf Komponentenebene

Wenn Ihre Anwendung eine Komponente enthält, für die keine Sicherheitsüberprüfungen erforderlich sind, können Sie die Rollenüberprüfungen für diese Komponente deaktivieren, um die Leistung zu verbessern. Oder beim Debuggen kann es hilfreich sein, die Sicherheit zu deaktivieren, damit Sie sich auf andere Aspekte der Programmfunktionalität konzentrieren können.

Wenn Sie eine Komponente installieren, sind standardmäßig Zugriffsüberprüfungen auf Komponentenebene aktiviert. Dies wird jedoch nur wirksam, wenn [Zugriffsüberprüfungen auf Anwendungsebene](enabling-access-checks-for-an-application.md) aktiviert sind und die [Sicherheitsstufe](setting-a-security-level-for-access-checks.md) auf **Zugriffsüberprüfungen auf Prozess- und Komponentenebene ausführen** festgelegt ist.

**So aktivieren oder deaktivieren Sie Zugriffsüberprüfungen auf Komponentenebene**

1.  Suchen Sie in der Konsolenstruktur des Component Services-Verwaltungstools die COM+-Anwendung, die die Komponente enthält, für die Sie Rollenüberprüfungen deaktivieren (oder aktivieren) möchten. Erweitern Sie die Ansicht in der Struktur, um die Komponenten im Ordner **Komponenten** anzuzeigen.

2.  Klicken Sie mit der rechten Maustaste auf die Komponente, für die Sie Rollenüberprüfungen aktivieren möchten, und klicken Sie dann auf **Eigenschaften.**

3.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Sicherheit.**

4.  Wählen Sie **Zugriffsüberprüfungen auf Komponentenebene erzwingen** aus, um Überprüfungen auf Komponentenebene zu erzwingen.

5.  Klicken Sie auf **OK**.

Die neue Einstellung wird wirksam, wenn die Anwendung das nächste Mal gestartet wird.

> [!Note]  
> Ab Windows Server 2003 sind Zugriffsüberprüfungen auf Komponentenebene standardmäßig deaktiviert, wenn eine COM+-Anwendung erstellt wird. Zugriffsüberprüfungen sind standardmäßig auf Anwendungsebene aktiviert und auf Komponentenebene standardmäßig deaktiviert. Zuvor wurden Zugriffsüberprüfungen standardmäßig auf Anwendungsebene deaktiviert und standardmäßig auf Komponentenebene aktiviert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Konfigurieren von Role-Based Security](configuring-role-based-security.md)
</dt> <dt>

[Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffsüberprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



