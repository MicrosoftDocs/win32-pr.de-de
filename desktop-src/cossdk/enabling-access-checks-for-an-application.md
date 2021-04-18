---
description: Das Ausführen dieses Schritts ermöglicht entweder Prozess Zugriffs Überprüfungen oder vollständige rollenbasierte Sicherheit, je nachdem, welche Sicherheitsstufe Sie auswählen und ob Sie die Zugriffs Überprüfung für einzelne Komponenten aktivieren.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Aktivieren von Zugriffs Überprüfungen für eine Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344814"
---
# <a name="enabling-access-checks-for-an-application"></a>Aktivieren von Zugriffs Überprüfungen für eine Anwendung

Das Ausführen dieses Schritts ermöglicht entweder Prozess Zugriffs Überprüfungen oder vollständige rollenbasierte Sicherheit, je nachdem, welche Sicherheitsstufe Sie auswählen und ob Sie die Zugriffs Überprüfung für einzelne Komponenten aktivieren.

**So aktivieren Sie Zugriffs Überprüfungen für eine Anwendung**

1.  Klicken Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Zugriffs Überprüfungen aktivieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .

3.  Aktivieren Sie das Kontrollkästchen **Zugriffs Überprüfungen für diese Anwendung erzwingen** .

4.  Klicken Sie auf **OK**.

> [!Note]  
> Ab Windows Server 2003 sind Zugriffs Überprüfungen beim Erstellen einer COM+-Anwendung standardmäßig aktiviert. Zugriffs Überprüfungen werden standardmäßig auf Anwendungsebene aktiviert und auf Komponentenebene standardmäßig deaktiviert. Zuvor waren Zugriffs Überprüfungen standardmäßig auf Anwendungsebene deaktiviert und auf Komponentenebene standardmäßig aktiviert.

 

Nachdem Sie die Zugriffs Überprüfungen aktiviert haben, sollten Sie die entsprechende Sicherheitsstufe auswählen. Weitere Informationen finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md). Außerdem müssen Sie sicherstellen, dass Sie Rollen definieren und Sie der Anwendung hinzufügen. Wenn Zugriffs Überprüfungen aktiviert sind, aber keine Rollen hinzugefügt wurden, schlagen alle Aufrufe der Anwendung fehl. Weitere Informationen finden Sie unter [Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md).

> [!Note]  
> Beim Debuggen Ihrer Anwendung ist es möglicherweise hilfreich, die Sicherheit zu deaktivieren, sodass Sie sich auf andere Aspekte des Verhaltens und Entwurfs des Programms konzentrieren können.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md)
</dt> <dt>

[Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffs Überprüfungen auf Komponentenebene](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



