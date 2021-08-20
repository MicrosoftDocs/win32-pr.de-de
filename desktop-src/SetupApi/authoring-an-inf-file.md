---
description: Beim Erstellen einer INF-Datei für eine Setupanwendung sollten Sie auch das INF-Dateiformat lesen, das in den Abschnitten Allgemeine Richtlinien für INF-Dateien und INF-Dateien und Anweisungen des Microsoft Windows 2000 Driver Development Kit dokumentiert ist.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Erstellen einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3745dc16a14f603de780b15d708fbb4542ea4503052aeb2b7edb3486c5b5fc51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966368"
---
# <a name="authoring-an-inf-file"></a>Erstellen einer INF-Datei

Beim Erstellen einer INF-Datei für eine Setupanwendung sollten Sie auch das INF-Dateiformat lesen, das in den Abschnitten Allgemeine Richtlinien für *INF-Dateien* und *INF-Dateien* und Anweisungen des Microsoft Windows 2000 Driver Development Kit dokumentiert ist.

Beachten Sie beim Erstellen von INF-Dateien für eine Setupanwendung die folgenden Regeln.

-   In **jeder** INF-Datei ist ein Abschnitt Version erforderlich.
-   Abschnitte müssen mit dem Abschnittsnamen beginnen, der in eckige Klammern () eingeschlossen \[ \] ist.
-   Die Namen **der Abschnitte DestinationDirs,** **SourceDisksFiles,** **SourceDisksNames,** **Strings** und **Version** müssen mit dem Abschnittstyp identisch sein. Verwenden Sie beispielsweise \[ DestinationDirs. \] Autoren können die Namen anderer Arten von Abschnitten angeben.
-   Namen der **Abschnitte SourceDisksNames** und **SourceDisksFiles** können mit einem plattformspezifischen Suffix angefügt werden. Um beispielsweise einen Intel-spezifischen **SourceDisksNames-Abschnitt** zu zeigen, verwenden \[ Sie SourceDisksNames.x86 \] . Wenn die Setupfunktionen plattformspezifische **SourceDisksNames-** und **SourceDisksFiles-Abschnitte** finden, die mit der Plattform des Benutzers übereinstimmen, verwenden die Funktionen die plattformspezifischen Abschnitte. Andernfalls verwenden die Setupfunktionen die Abschnitte **SourceDisksNames** und **SourceDisksFiles** ohne Suffix. Die Setupfunktionen können programmgesteuert das System des Benutzers bestimmen. Weitere Informationen finden [Sie in den Abschnitten INF SourceDisksNames und SourceDisksFiles – Beispiel.](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md)
-   Werte können als ersetzbare Zeichenfolgen ausgedrückt werden, indem die Form % strkey %*verwendet wird.* Um ein %-Zeichen in der Zeichenfolge zu verwenden, verwenden Sie %%. Der Strkey muss in  einem Zeichenfolgenabschnitt der INF-Datei definiert werden.

 

 



