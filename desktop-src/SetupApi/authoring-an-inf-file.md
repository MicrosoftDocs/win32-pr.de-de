---
description: Wenn Sie eine INF-Datei für eine Setup Anwendung erstellen, sollten Sie auch auf das INF-Dateiformat verweisen, das unter Allgemeine Richtlinien für INF-Dateien und INF-Datei Abschnitte und Direktiven des Microsoft Windows 2000 Driver Development Kit dokumentiert ist.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Erstellen einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347737"
---
# <a name="authoring-an-inf-file"></a>Erstellen einer INF-Datei

Wenn Sie eine INF-Datei für eine Setup Anwendung erstellen, sollten Sie auch auf das INF-Dateiformat verweisen, das unter *Allgemeine Richtlinien für INF-Dateien* und *INF-Datei Abschnitte und Direktiven* des Microsoft Windows 2000 Driver Development Kit dokumentiert ist.

Wenn Sie die INF-Dateien für eine Setup Anwendung erstellen, befolgen Sie die folgenden Regeln.

-   Ein **Versions** Abschnitt ist in jeder INF-Datei erforderlich.
-   Abschnitte müssen mit dem Abschnittsnamen beginnen, der von eckigen Klammern () eingeschlossen wird \[ \] .
-   Die Namen der Abschnitte **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings** und **Version** müssen mit dem Typ des Abschnitts identisch sein. Verwenden Sie beispielsweise \[ DestinationDirs \] . Autoren können die Namen anderer Abschnitts Typen angeben.
-   Die Namen der Abschnitte " **SourceDisksNames** " und " **SourceDisksFiles** " können mit einem plattformspezifischen Suffix angehängt werden. Verwenden Sie z. b. zum Anzeigen eines Intel-spezifischen **SourceDisksNames** -Abschnitts " \[ SourceDisksNames. x86" \] . Wenn die Setup Funktionen plattformspezifische **SourceDisksNames** -und **SourceDisksFiles** -Abschnitte finden, die mit der Plattform des Benutzers übereinstimmen, verwenden die Funktionen die plattformspezifischen Abschnitte. Andernfalls verwenden die Setup Funktionen die nicht-suffixt-Abschnitte " **SourceDisksNames** " und " **SourceDisksFiles** ". Mit den Setup Funktionen kann das System des Benutzers Programm gesteuert bestimmt werden. Weitere Informationen finden Sie im [Abschnitt INF SourceDisksNames und SourceDisksFiles](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).
-   Werte können mithilfe der Form%*strKey*% als ersetzbare Zeichenfolge ausgedrückt werden. Verwenden Sie%%, um ein%-Zeichen in der Zeichenfolge zu verwenden. Der ' strKey ' muss in einem **String** -Abschnitt der INF-Datei definiert werden.

 

 



