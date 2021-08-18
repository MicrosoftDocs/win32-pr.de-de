---
description: Geschützter Modus
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Geschützter Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2f16b9f923215af6c2211339859d8eab4803e6793be248a83760e298ed084c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994780"
---
# <a name="protected-mode"></a>Geschützter Modus

Die meisten sicherheitsfeatures Windows Internet Explorer 8 sind in Internet Explorer 8 für Windows XP mit dem Betriebssystem Service Pack 2 (SP2) und höher verfügbar. Der geschützte Modus ist nur für Windows Vista oder höhere Versionen verfügbar, da er auf den folgenden Sicherheitsfeatures basiert, die für Windows Vista neu sind:

-   [Die Benutzerkontensteuerung (User Account Control, UAC)](https://msdn.microsoft.com/library/aa511445.aspx) erleichtert die Ausführung ohne Administratorrechte. Wenn Benutzer Programme mit eingeschränkten Benutzerberechtigungen ausführen, sind sie sicherer vor Angriffen als bei der Ausführung mit Administratorrechten. Das Windows Betriebssystem kann verhindern, dass schädliche Aktionen durch schädlichen Code ausgeführt werden.
-   Ein Integritätsmechanismus schränkt den Schreibzugriff auf [sicherungsfähige Objekte](../secauthz/securable-objects.md) durch Prozesse mit niedrigerer Integrität ein, genauso wie die Mitgliedschaft in Benutzerkontengruppen die Rechte von Benutzern auf den Zugriff auf sensible Systemkomponenten einschränkt.
-   [Benutzeroberfläche Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) verhindert, dass Prozesse ausgewählte Fenstermeldungen und andere USER-APIs an Prozesse senden, die mit höherer Integrität ausgeführt werden.

Die Sicherheitsinfrastruktur Windows Integritätsmechanismus ermöglicht es dem geschützten Modus, Windows Internet Explorer mit den Berechtigungen bereitzustellen, die Benutzer zum Durchsuchen des Webs benötigen, während Berechtigungen, die Benutzer benötigen, um Programme automatisch zu installieren oder vertrauliche Systemdaten zu ändern, einbehalten werden.

Benutzer können dieses Feature über ein Kontrollkästchen deaktivieren, und Administratoren können es mithilfe von Gruppenrichtlinie deaktivieren.

> [!IMPORTANT]
> Sie sollten das Feature während der Problembehandlung nur als temporäres Measure deaktivieren, um das Verhalten der Anwendung zu vergleichen, wenn das Feature aktiviert ist oder nicht. Es wird empfohlen, dieses Feature dauerhaft zu aktivieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
