---
description: Wichtige Entwurfsentscheidungen für Eltern Steuerelemente
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Wichtige Entwurfsentscheidungen für Eltern Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050496"
---
# <a name="parental-controls-key-design-decisions"></a>Wichtige Entwurfsentscheidungen für Eltern Steuerelemente

Wichtige Entwurfsentscheidungen bei der Entwicklung von Windows Vista-Jugendschutz-Steuerelementen:

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Wesentliche Abhängigkeit von der Windows Vista-Benutzerkontensteuerung (User Account Control, UAC)

Eine wichtige Entscheidung für die Jugendschutzbestimmungen in Windows Vista besteht darin, dass Sie sich auf die neue Benutzerkontensteuerung (User Account Control, UAC) stützen, um die eingeschränkten Rechte Konto Identitäten zu implementieren, die besonders für Offline Beschränkungen bei kontrollierten Benutzern Weitere Informationen zur [Benutzerkontensteuerung finden Sie unter Windows Vista und Windows Server 2008 Developer Story: Anforderungen für die Windows Vista-Anwendungsentwicklung für die Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905330(v=msdn.10)). Zusammenfassend gilt: jedes Konto mit Administratorrechten verfügt über Berechtigungen zum Ausführen der übergeordneten Rolle oder der Rolle "Wächter" zum Anzeigen von Protokolldaten und Festlegen von Richtlinien. Eltern Steuerelemente können nur für Benutzer mit Standard rechten (früher als Benutzerkonten mit den geringsten Rechten bezeichnet) festgelegt werden, da Sie nur Protokolle und Einstellungen mit Access Control Listen ändern können, die nur für Administratoren konfiguriert sind. Anders gesagt:

-   Eine übergeordnete Identität oder eine Überwachungs Identität ist implizit mit einem Konto mit rechten eines Administrators gleich.
-   Der Benutzer muss Standardbenutzer sein.

## <a name="nearly-all-settings-are-available-by-apis"></a>Fast alle Einstellungen sind über APIs verfügbar.

Mit Ausnahme von Elementen wie z. b. Bewertungssystem Definitionen können von der Benutzeroberfläche für die Jugend Kontrollen verfügbare Einstellungen auch durch verfügbar gemachte APIs geändert werden. Es ist erforderlich, dass Programme Erweiterungen in Administratorrechte implementieren, um die Einstellungen zu ändern, wie oben für die UAC erwähnt.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Die Jugend Steuerungselemente von Windows Vista sind eine reine consumertechnologie.

Die Jugend Steuerungselemente von Windows Vista sind nicht für die Verwendung mit Domänen Konten vorgesehen. Als consumertechnologie werden Eltern Kontrollen nicht in Geschäfts-SKUs von Windows Vista bereitgestellt. Wenn ein Computer einer Domäne hinzugefügt wird, werden die Links für die Benutzeroberfläche der Familien Sicherheit unterdrückt.

Es wird ein Mechanismus bereitgestellt, um die Funktionalität für den in die Domäne eingebundenen Fall verfügbar zu machen, aber nur nicht-Domänen Benutzerkonten können mit Jugendschutz-Steuerelementen konfiguriert werden.

 

 
