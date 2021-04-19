---
description: Aktivieren von Zugriffs Überprüfungen auf Komponentenebene
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Aktivieren von Zugriffs Überprüfungen auf Komponentenebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342982"
---
# <a name="enabling-access-checks-at-the-component-level"></a>Aktivieren von Zugriffs Überprüfungen auf Komponentenebene

Wenn Ihre Anwendung eine Komponente enthält, die keine Sicherheitsüberprüfungen benötigt, können Sie die Rollen Überprüfung für diese Komponente deaktivieren, um die Leistung zu verbessern. Oder beim Debuggen ist es möglicherweise hilfreich, die Sicherheit zu deaktivieren, sodass Sie sich auf andere Aspekte der Programmfunktionalität konzentrieren können.

Wenn Sie eine Komponente installieren, werden standardmäßig Zugriffs Überprüfungen auf Komponentenebene aktiviert. Dies wird jedoch nur wirksam, wenn [Zugriffs Überprüfungen auf Anwendungsebene](enabling-access-checks-for-an-application.md) aktiviert sind und die [Sicherheitsstufe](setting-a-security-level-for-access-checks.md) festgelegt ist, um **Zugriffs Überprüfungen auf Prozess-und Komponentenebene durchzuführen**.

**So aktivieren oder deaktivieren Sie Zugriffs Überprüfungen auf Komponentenebene**

1.  Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, die die Komponente enthält, für die Sie Rollen Überprüfungen deaktivieren (oder aktivieren) möchten. Erweitern Sie die Ansicht in der Struktur, um die Komponenten im Ordner **Komponenten** anzuzeigen.

2.  Klicken Sie mit der rechten Maustaste auf die Komponente, für die Sie Rollen Überprüfungen aktivieren möchten, und klicken Sie dann auf **Eigenschaften**.

3.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Sicherheit** .

4.  Wählen Sie **Zugriffs Überprüfungen auf Komponentenebene erzwingen** , um Überprüfungen auf Komponentenebene zu erzwingen.

5.  Klicken Sie auf **OK**.

Die neue Einstellung wird wirksam, wenn die Anwendung das nächste Mal gestartet wird.

> [!Note]  
> Ab Windows Server 2003 sind Zugriffs Überprüfungen auf Komponentenebene beim Erstellen einer COM+-Anwendung standardmäßig deaktiviert. Zugriffs Überprüfungen werden standardmäßig auf Anwendungsebene aktiviert und auf Komponentenebene standardmäßig deaktiviert. Zuvor waren Zugriffs Überprüfungen standardmäßig auf Anwendungsebene deaktiviert und auf Komponentenebene standardmäßig aktiviert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md)
</dt> <dt>

[Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffs Überprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



