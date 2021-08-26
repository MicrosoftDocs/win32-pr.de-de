---
description: Wichtige Entwurfsentscheidungen zu Jugendkontrollen
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Wichtige Entwurfsentscheidungen zu Jugendkontrollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef8f1e1d1b629c9fbb4354fb266376453938a35bde80e7b60f57be8f77da70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939290"
---
# <a name="parental-controls-key-design-decisions"></a>Wichtige Entwurfsentscheidungen zu Jugendkontrollen

Wichtige Entwurfsentscheidungen bei der Entwicklung von Windows Vista-Jugendschutz sind:

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Grundlegende Abhängigkeit von der Windows Vista-Benutzerkontensteuerung (UAC)

Eine wichtige Entscheidung für Windows Vista-Jugendschutz besteht in der Verwendung des neuen Features benutzerkontensteuerung (User Account Control, UAC), um die reduzierten Rechtekontoidentitäten zu implementieren, die insbesondere für Offlineeinschränkungen für kontrollierte Benutzer erforderlich sind. Weitere Informationen zur Benutzerkontensteuerung finden Sie unter [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)). Zusammengefasst verfügt jedes Konto mit Administratorrechten effektiv über Berechtigungen zum Ausführen der übergeordneten Oder-Wächterrolle zum Anzeigen von Protokolldaten und Festlegen von Richtlinien. Die Jugendschutzkontrollen können nur für Benutzer mit Standardrechten (früher als Benutzerkonten mit geringsten Berechtigungen oder LUAs bezeichnet) festgelegt werden, da nur sie Protokolle und Einstellungen nicht ändern können, wenn Access Control-Listen (ACLs) nur für Administratoren zum Schreiben konfiguriert sind. Anders gesagt:

-   Eine übergeordnete oder Wächteridentität entspricht implizit einem Konto, das über Rechte eines Administrators verfügt.
-   Benutzer mit Jugendschutz müssen Standardbenutzer sein.

## <a name="nearly-all-settings-are-available-by-apis"></a>Fast alle Einstellungen von APIs verfügbar

Mit Ausnahme von Elementen wie Bewertungssystemdefinitionen können einstellungen, die für die Bearbeitung durch die Jugendschutz-Benutzeroberfläche verfügbar sind, auch durch verfügbar gemachte APIs geändert werden. Es ist erforderlich, dass Programme Rechteerweiterungen für Administratorrechte implementieren, um Einstellungen zu ändern, wie oben für die UAC beschrieben.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Windows Vista-Jugendschutz ist eine nur für Verbraucher bestimmte Technologie

Windows Vista-Jugendschutz ist nicht für die Verwendung mit Domänenkonten vorgesehen. Als Verbrauchertechnologie wird die Jugendschutzsteuerung nicht in Geschäfts-SKUs von Windows Vista bereitgestellt. Wenn ein Computer einer Domäne beigetreten ist, werden die Family Safety-Benutzeroberflächenlinks unterdrückt.

Es wird ein Mechanismus bereitgestellt, um die Funktionalität für den In die Domäne beigetretenen Fall verfügbar zu machen, aber nur Nicht-Domänenbenutzerkonten können mit Der Jugendschutz konfiguriert werden.

 

 
