---
description: Geschützter Modus
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Geschützter Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1b8b1e6931ed83ec59ccfe4c3c63d8e5b5eed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116448"
---
# <a name="protected-mode"></a>Geschützter Modus

Die meisten Windows Internet Explorer 8-Sicherheitsfeatures sind in Internet Explorer 8 für windows XP mit dem Betriebssystem Service Pack 2 (SP2) und höher verfügbar. Der geschützte Modus ist nur für Windows Vista oder höhere Versionen verfügbar, da er auf den folgenden Sicherheitsfeatures basiert, die für Windows Vista neu sind:

-   [Die Benutzerkontensteuerung (User Account Control, UAC)](https://msdn.microsoft.com/library/aa511445.aspx) erleichtert die Ausführung ohne Administratorrechte. Wenn Benutzer Programme mit eingeschränkten Benutzerberechtigungen ausführen, sind sie sicherer vor Angriffen als bei der Ausführung mit Administratorrechten. Das Windows-Betriebssystem kann verhindern, dass bösartiger Code schädliche Aktionen ausführt.
-   Ein Integritätsmechanismus schränkt den Schreibzugriff auf [sicherungsfähige Objekte](../secauthz/securable-objects.md) durch Prozesse mit niedrigerer Integrität ein, genauso wie die Mitgliedschaft in Benutzerkontengruppen die Rechte von Benutzern auf den Zugriff auf sensible Systemkomponenten einschränkt.
-   [Benutzeroberfläche Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) verhindert, dass Prozesse ausgewählte Fenstermeldungen und andere USER-APIs an Prozesse senden, die mit höherer Integrität ausgeführt werden.

Die Sicherheitsinfrastruktur des Windows-Integritätsmechanismus ermöglicht es dem geschützten Modus, Windows Internet Explorer die Berechtigungen zur Verfügung zu stellen, die Benutzer zum Durchsuchen des Webs benötigen, während Benutzer Berechtigungen einbehalten, die Benutzer benötigen, um Programme unbeaufsichtigt zu installieren oder sensible Systemdaten zu ändern.

Benutzer können dieses Feature über ein Kontrollkästchen deaktivieren, und Administratoren können es mithilfe von Gruppenrichtlinie deaktivieren.

> [!IMPORTANT]
> Sie sollten das Feature während der Problembehandlung nur als temporäres Measure deaktivieren, um das Verhalten der Anwendung zu vergleichen, wenn das Feature aktiviert ist oder nicht. Es wird empfohlen, dieses Feature dauerhaft zu aktivieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
