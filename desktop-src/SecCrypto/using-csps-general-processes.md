---
description: Beachten Sie bei der Verwendung von Kryptografiedienstanbietern (CSPs) die folgenden Konventionen.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Verwenden von CSPs: allgemeine Prozesse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343751"
---
# <a name="using-csps-general-processes"></a>Verwenden von CSPs: allgemeine Prozesse

Beachten Sie bei der Verwendung von [*Kryptografiedienstanbietern*](../secgloss/c-gly.md) (CSPs) die folgenden Konventionen.

## <a name="private-key-caching"></a>Zwischenspeichern von privaten Schlüsseln

Ein CSP kann einige [*private Schlüssel*](../secgloss/p-gly.md)Zwischenspeichern. Es ist möglich, diese private Schlüssel Zwischenspeicherung auf globaler, aber nicht auf anwendungsspezifischer Basis zu steuern. Das Zwischenspeichern von Änderungen wird durch Ändern bestimmter Registrierungs Einstellungen vorgenommen. Weitere Informationen finden Sie unter Caching für die Zwischenspeicherung von [**privaten Schlüsseln**](private-key-caching-constants.md).

## <a name="example-code-conventions"></a>Beispiel Code Konventionen

Um präziseren, besser lesbaren Code bereitzustellen, werden in den Beispielen nicht immer einige Grundsätze von bewährten Programmierpraktiken befolgt. Dies gilt insbesondere für:

-   Nur eingeschränkte Fehler Antworten werden angezeigt. Ordnungsgemäß geschriebene, vollständige Programme überprüft zurückgegebene Fehlercodes und führt beim Auftreten eines Fehlers geeignete Aktionen aus.
-   Nur eingeschränkte Arbeitsspeicher-und Ressourcenverwaltung erfolgt. Gut geschriebene, vollständige Programme zerstören alle Schlüssel und Hashwerte, geben den gesamten zugeordneten Arbeitsspeicher frei, schließen alle [*Dateien und geben*](../secgloss/h-gly.md)alle Handles frei. In diesen Beispielen wird nur eine begrenzte Demonstration der Verwendung von Funktionen bereitgestellt, die diese Aufgaben ausführen. In diesen Beispielen werden keine Arbeitsspeicher-oder Ressourcen Verwaltungsaufgaben ausgeführt, wenn die Programm Beendigung aufgrund von Fehlern auftritt.

Die folgenden Themen enthalten allgemeine Informationen zu Prozedur Beispielen und Beispielcode.

-   [Abrufen von Daten mit unbekannter Länge](retrieving-data-of-unknown-length.md)
-   [Auflisten unterstützter Protokolle](enumerating-supported-protocols.md)

 

 
