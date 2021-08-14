---
title: Informationen zu Versionsinformationen
description: In diesem Thema werden die Versionsinformationsfunktionen erläutert.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- Ressourcen,Versionsinformationen
- Versionsinformationen
- Hinzufügen von Versionsinformationen
- Dateikonflikte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7b7916e77d29fa21aa6eb68e223d43a1415c36058fbe00e2d3abb9c4cae979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870716"
---
# <a name="about-version-information"></a>Informationen zu Versionsinformationen

Sie können die Versionsinformationsfunktionen verwenden, um zu bestimmen, wo eine Datei installiert werden soll, und Konflikte mit derzeit installierten Dateien zu identifizieren. Mit diesen Funktionen können Sie die folgenden Probleme vermeiden:

-   Installieren älterer Versionen von Komponenten über neuere Versionen
-   Ändern der Sprache in einem Gemischtsprachsystem ohne Benachrichtigung
-   Installieren mehrerer Kopien einer Bibliothek in verschiedenen Verzeichnissen
-   Kopieren von Dateien in Netzwerkverzeichnisse, die von mehreren Benutzern gemeinsam genutzt werden

Mit den Versionsinformationsfunktionen können Anwendungen eine Versionsressource nach Dateiinformationen abfragen und die Informationen in einem eindeutigen Format präsentieren. Diese Informationen umfassen den Zweck der Datei, den Autor, die Versionsnummer und so weiter.

Sie können Versionsinformationen zu allen Dateien hinzufügen, die über Windows verfügen können, z. B. DLLs, ausführbare Dateien oder FON-Schriftartdateien. Um die Informationen hinzuzufügen, erstellen Sie eine [VERSIONINFO-Ressource,](/windows/desktop/menurc/versioninfo-resource) und verwenden Sie den Ressourcencompiler, um die Ressource zu kompilieren.

 

 