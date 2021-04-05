---
title: Erstellen einer Geräte Beschreibung
description: Eine UPnP-basierte Geräte Beschreibung ist ein XML-Dokument, in dem die Eigenschaften eines Geräts und die Hierarchie der geschachtelten Geräte beschrieben werden.
ms.assetid: b2a7d342-958c-439d-8b17-b4fdc5fbad12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52df95de15481c7004704b6f67cd9478083ac88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947588"
---
# <a name="creating-a-device-description"></a>Erstellen einer Geräte Beschreibung

Eine UPnP-basierte [*Geräte Beschreibung*](d-gly.md) ist ein XML-Dokument, in dem die Eigenschaften eines Geräts und die Hierarchie der geschachtelten Geräte beschrieben werden. Das Schema für UPnP-basierte Geräte Beschreibungen, die als UPnP-Vorlagen Sprache (UTL) für Geräte bezeichnet wird, ist in der UPnP-Geräte Architektur definiert. Geräte Beschreibungen enthalten Links zu [*Dienst Beschreibungen*](s-gly.md). Das Schema für Dienst Beschreibungen und die UTL für Dienste werden auch in der Spezifikation "UPnP-Geräte Architektur" definiert.

> [!Note]  
> Es können Probleme auftreten, wenn Sie die Dienst Beschreibung von www.UPnP.org verwenden.

 

Der Entwickler eines Geräts muss Geräte-und Dienst Beschreibungen für das Gerät bereitstellen.

Die Elemente einer Geräte Beschreibung, die der Entwickler eines gehosteten Geräts bereitstellen muss, entsprechen den Elementen, die in der Spezifikation "UPnP-Geräte Architektur" definiert sind, mit den folgenden Ausnahmen:

-   Die **controlurl** -und **eventsuburl** -Elemente sind erforderlich und müssen leer sein. Der Geräte Host füllt Werte für diese Felder aus, wenn das Gerät veröffentlicht und angekündigt wird.
-   Das **udn** -Element muss einen Bezeichner enthalten, der für das Geräte Beschreibungs Dokument eindeutig ist (d. h., er muss nicht global eindeutig sein). Dieser Bezeichner wird verwendet, um nach dem vom Geräte Host generierten udn zu suchen.
-   Die **scpdurl** -Elemente dürfen keine URLs für Dienst Beschreibungen enthalten. Stattdessen müssen Sie den Namen der Dienst Beschreibungsdatei enthalten. Die Dienst Beschreibungsdatei muss sich im [*Ressourcenverzeichnis*](r-gly.md)befinden. Der Speicherort dieses Verzeichnisses muss für den Geräte Host während des Registrierungsvorgangs bereitgestellt werden, z. b. durch die Verwendung eines Setup Programms. Dieser Pfad und alle untergeordneten Pfade sind relative Pfade, basierend auf dem registrierten Pfad.
-   Das **URL** -Element innerhalb des **Icon** -Elements darf keine URLs für Geräte Symbole enthalten. Stattdessen müssen Sie den Namen der Symbol Datei enthalten. Falls vorhanden, muss sich die Symbol Datei im Ressourcenverzeichnis befinden. Dieser Pfad und alle untergeordneten Pfade sind relative Pfade, basierend auf dem registrierten Pfad.
-   Das **URLBase** -Element darf nicht vorhanden sein.

> [!Note]  
> Alle vom Geräte Host generierten URLs sind relative URLs. Die URLs sind relativ zum Speicherort des Dokuments für die Geräte Beschreibung, das in der erst Ankündigung des Geräts gesendet wird.

 

> [!IMPORTANT]
> Fügen Sie Ihrem Dokument Beschreibungs Dokument keine Kommentare hinzu, da dies zu Registrierungs Fehlern führen kann, wenn der universelle Plug & Play Geräte Host versucht, das Dokument zu analysieren.

 

## <a name="string-length-limitations"></a>Einschränkungen der Zeichen folgen Länge

Die folgenden Zeichen folgen Längen werden in der Geräte Host-API mit der UPnP-Technologie verwendet:

-   Geräte- **ype** – 64 Bytes
-   **FriendlyName** – 64 Bytes
-   **Hersteller** – 64 Bytes
-   **modeldescription** – 128 Bytes
-   **modelname** – 32 Bytes
-   **modelnumber** – 32 Bytes
-   **serialNumber** – 64 Bytes
-   **UPC** – 12 Bytes
-   **serviceType** – 64 Bytes
-   **serviceid** – 64 Bytes

 

 




