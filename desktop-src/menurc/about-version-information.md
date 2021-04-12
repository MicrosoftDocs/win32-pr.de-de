---
title: Informationen zu Versionsinformationen
description: In diesem Thema werden die Funktionen der Versionsinformationen erläutert.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- Ressourcen, Versionsinformationen
- Versionsinformationen
- Hinzufügen von Versionsinformationen
- Dateikonflikte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390212"
---
# <a name="about-version-information"></a>Informationen zu Versionsinformationen

Sie können die Versions Informationsfunktionen verwenden, um zu bestimmen, wo eine Datei installiert werden soll, und um Konflikte mit den derzeit installierten Dateien zu identifizieren. Diese Funktionen ermöglichen es Ihnen, die folgenden Probleme zu vermeiden:

-   Installieren älterer Versionen von Komponenten in neueren Versionen
-   Ändern der Sprache in einem System mit gemischter Sprache ohne Benachrichtigung
-   Installieren mehrerer Kopien einer Bibliothek in verschiedenen Verzeichnissen
-   Kopieren von Dateien in Netzwerk Verzeichnisse, die von mehreren Benutzern gemeinsam genutzt werden

Mit den Versions Informationsfunktionen können Anwendungen eine Versions Ressource nach Dateiinformationen Abfragen und die Informationen in einem klaren Format darstellen. Zu diesen Informationen gehören der Zweck der Datei, der Autor, die Versionsnummer usw.

Sie können allen Dateien, die über Windows-Ressourcen verfügen, z. b. DLLs, ausführbare Dateien oder. FON-Schriftart Dateien, Versionsinformationen hinzufügen. Um die Informationen hinzuzufügen, erstellen Sie eine [VERSIONINFO-Ressource](/windows/desktop/menurc/versioninfo-resource) , und kompilieren Sie die Ressource mit dem Ressourcen Compiler.

 

 