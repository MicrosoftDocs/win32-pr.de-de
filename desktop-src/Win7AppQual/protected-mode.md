---
description: .
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Geschützter Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace82e27bbec3bb97a9ffbd3b64c9c6cee9e11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865967"
---
# <a name="protected-mode"></a>Geschützter Modus

Die meisten Windows Internet Explorer 8-Sicherheitsfeatures sind in Internet Explorer 8 für das Betriebssystem Windows XP mit Service Pack 2 (SP2) und spätere Versionen verfügbar. Der geschützte Modus ist nur für Windows Vista oder spätere Versionen verfügbar, da er auf den folgenden Sicherheitsfeatures basiert, die für Windows Vista neu sind:

-   Die [Benutzerkontensteuerung (User Account Control, UAC)](https://msdn.microsoft.com/library/aa511445.aspx) erleichtert die Ausführung ohne Administratorrechte. Wenn Benutzer Programme mit eingeschränkten Benutzerberechtigungen ausführen, sind Sie vor Angriffen sicherer, als wenn Sie mit Administratorrechten ausgeführt werden. Das Windows-Betriebssystem kann verhindern, dass böswillige Code schädliche Aktionen ausführt.
-   Ein Integritäts Mechanismus schränkt den Schreibzugriff auf Sicherungs [fähige Objekte](../secauthz/securable-objects.md) durch Prozesse mit niedrigerer Integrität auf die gleiche Weise ein, wie die Benutzerkonten Gruppen-Mitgliedschaft die Rechte von Benutzern für den Zugriff auf sensible Systemkomponenten einschränkt.
-   Die [Benutzeroberflächen-Berechtigungs Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) verhindert, dass Prozesse ausgewählte Fenster Nachrichten und andere Benutzer-APIs an Prozesse senden, die mit höherer Integrität ausgeführt werden.

Mit der Sicherheitsinfrastruktur des Windows-Integritäts Mechanismus kann der geschützte Modus Windows Internet Explorer die Berechtigungen bereitstellen, die Benutzer zum Durchsuchen des Internets benötigen, während gleichzeitig die Berechtigungen, die Benutzer zum unbeaufsichtigten Installieren von Programmen oder zum Ändern sensibler Systemdaten benötigen

Benutzer können diese Funktion mithilfe eines Kontrollkästchens deaktivieren, und Administratoren können Sie mithilfe von Gruppenrichtlinie deaktivieren.

> [!IMPORTANT]
> Sie sollten die Funktion nur als temporäre Maßnahme bei der Problembehandlung deaktivieren, um das Verhalten der Anwendung zu vergleichen, wenn die Funktion aktiviert ist. Es wird empfohlen, diese Funktion dauerhaft zu aktivieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
