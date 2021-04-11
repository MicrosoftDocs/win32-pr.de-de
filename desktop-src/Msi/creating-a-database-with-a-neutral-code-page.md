---
description: Die empfohlene Vorgehensweise für die Verarbeitung von Codepages besteht darin, eine neutrale Basisdatenbank zu erstellen, die nur Zeichen enthält, die in eine beliebige Codepage übersetzt werden können.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Erstellen einer Datenbank mit einer neutralen Codepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042404"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>Erstellen einer Datenbank mit einer neutralen Codepage

Die empfohlene Vorgehensweise für die Verarbeitung von Codepages besteht darin, eine neutrale Basisdatenbank zu erstellen, die nur Zeichen enthält, die in eine beliebige Codepage übersetzt werden können. Die Datenbank kann dann auf die Codepage der Lokalisierung festgelegt werden, und die Lokalisierungs Informationen können wie unter [lokalisieren eines Windows Installer Pakets](localizing-a-windows-installer-package.md)beschrieben hinzugefügt werden.

Vermeiden Sie zum Erstellen einer neutralen Datenbank erweiterte Zeichen, die nicht zum ASCII-Zeichensatz gehören und daher eine spezielle Codepage erfordern. Beispielsweise sind das Copyright Vorzeichen, © und das eingetragene Markenzeichen,, keine ASCII-Zeichen und erfordern eine spezielle ANSI-Codepage für die richtige Anzeige. Verwenden Sie stattdessen (c) und (r), da diese Zeichen in die Symbole für die englischsprachige Version übersetzt oder transformiert werden können. Diese neutrale Datenbank kann dann durch Festlegen der Codepage und durch das Hinzufügen von Lokalisierungs Informationen durch Tabellen Bearbeitung oder durch Importieren von Textarchiv Dateien lokalisiert werden.

 

 



