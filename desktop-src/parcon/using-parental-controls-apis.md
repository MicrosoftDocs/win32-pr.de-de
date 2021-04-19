---
description: Verwenden von Eltern Steuerungs-APIs
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Verwenden von Eltern Steuerungs-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367915"
---
# <a name="using-parental-controls-apis"></a>Verwenden von Eltern Steuerungs-APIs

## <a name="api-selection"></a>API-Auswahl

Wie im Abschnitt Übersicht erwähnt, umfasst die Entwicklung die Verwendung von bis zu drei APIs:

-   Zugriff auf grundlegende Einstellungen: die in "wpcapi. h" definierte mindestrecompliance-com-API (Compliance-API) für den einfachen Zugriff auf eine Schlüssel Teilmenge des Zustands der Jugend Steuerungs Zustände.
-   Lese-/Schreibzugriff für vollständige Einstellungen: die Verwendung einer kleinen Teilmenge der WMI-com-API für den Vollzugriff ist nur erforderlich, wenn der ISV Einstellungen ändern muss. Das Hinzufügen eines Benutzeroberflächen-Erweiterbarkeits Links, das Ersetzen des Webinhalts Filters oder Ergänzungen der Computer weiten http-Anwendung oder der Ausnahmeliste für die URL-Filterung sind die Hauptgründe für die Verwendung der API. Da die Verwendung des Namespace für die WMI-Jugendschutz-Namespace Rohdaten Zugriff auf den zugrunde liegenden Einstellungs Speicher bietet, sollten die ISVs bei der Interpretation des Zustands aus den einzelnen Einstellungen, die tatsächlich möglicherweise Abhängigkeiten von anderen Einstellungen aufweisen, vorsichtig vorgehen. Daher wird empfohlen, die Kompatibilitäts-API zum Lesen des Zustands für alle Werte zu verwenden, die von dieser API verfügbar gemacht werden.
-   Protokollierung: die Ereignis Ablauf Verfolgung und die Berichterstattungs System-API von Windows Vista (auch als etw bezeichnet) zum Veröffentlichen von Aktivitäts Ereignissen in den Eltern Steuerungs Protokollen, zusammen mit Ereignis Deskriptoren und Array Enumerationen, die in wpcevent. h definiert sind.

Alle APIs können als Standardbenutzer aufgerufen werden. Für die Protokollierung kann jeder Benutzerprotokoll Ereignisse als Quelle durchsuchen. Das Aufrufen von zum Abrufen oder Ändern von Einstellungen für einen anderen Benutzer schlägt fehl, wenn der Aufrufer nicht über Administratorrechte verfügt. Anders ausgedrückt: ein Standardbenutzer kann nur auf seine eigenen Einstellungen zugreifen und nur zum Lesen.

Die Einstellungen und die Verwendung der Protokollierungs-API werden in den folgenden Abschnitten ausführlicher erläutert:

-   [Verwenden von Einstellungen für die Jugend Steuerungseinstellungen](using-parental-controls-settings-apis.md)
-   [Verwenden von Protokollierungs-APIs für Eltern Steuerelemente](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a>Entwicklungsumgebung

Die Entwicklung für Jugendschutz Steuerelemente erfordert Zugriff auf drei Header Dateien: wpc. h, wpcapi. h und wpcevent. h. WPC. h ist ein Collector, der die Einstellungen der öffentlichen Kompatibilitäts-API und der Ereignis Header enthält. Daher genügt es, wpc. h in den Anwendungscode einzubeziehen.

Lese-/Schreibberechtigungen für die WMI-API werden in der Datei "wpcsprov. mof" angegeben. Diese Datei wird im WBEM-Unterverzeichnis unter dem Verzeichnis Windows System32 installiert.

Das Microsoft Windows Software Development Kit (SDK) enthält Beispielcode, mit dem Sie den hier gezeigten Beispielcode verstärken und einfache Befehlszeilen gesteuerte Tools zum Durchsuchen von APIs und zum Integrieren von Tests bereitstellen können.

 

 



