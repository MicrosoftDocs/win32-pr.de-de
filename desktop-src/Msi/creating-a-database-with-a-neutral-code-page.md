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
# <a name="creating-a-database-with-a-neutral-code-page"></a><span data-ttu-id="ec4a2-103">Erstellen einer Datenbank mit einer neutralen Codepage</span><span class="sxs-lookup"><span data-stu-id="ec4a2-103">Creating a Database with a Neutral Code Page</span></span>

<span data-ttu-id="ec4a2-104">Die empfohlene Vorgehensweise für die Verarbeitung von Codepages besteht darin, eine neutrale Basisdatenbank zu erstellen, die nur Zeichen enthält, die in eine beliebige Codepage übersetzt werden können.</span><span class="sxs-lookup"><span data-stu-id="ec4a2-104">The recommended approach for handling code pages is to author a neutral base database that only contains characters that can be translated into any code page.</span></span> <span data-ttu-id="ec4a2-105">Die Datenbank kann dann auf die Codepage der Lokalisierung festgelegt werden, und die Lokalisierungs Informationen können wie unter [lokalisieren eines Windows Installer Pakets](localizing-a-windows-installer-package.md)beschrieben hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ec4a2-105">The database may then be set to the code page of the localization and the localization information can be added as described in [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="ec4a2-106">Vermeiden Sie zum Erstellen einer neutralen Datenbank erweiterte Zeichen, die nicht zum ASCII-Zeichensatz gehören und daher eine spezielle Codepage erfordern.</span><span class="sxs-lookup"><span data-stu-id="ec4a2-106">To author a neutral database, avoid extended characters that do not belong to the ASCII character set and therefore require a special code page.</span></span> <span data-ttu-id="ec4a2-107">Beispielsweise sind das Copyright Vorzeichen, © und das eingetragene Markenzeichen,, keine ASCII-Zeichen und erfordern eine spezielle ANSI-Codepage für die richtige Anzeige.</span><span class="sxs-lookup"><span data-stu-id="ec4a2-107">For example, the copyright sign, ©, and the registered trademark sign, , are not ASCII characters, and require a special ANSI code page for proper display.</span></span> <span data-ttu-id="ec4a2-108">Verwenden Sie stattdessen (c) und (r), da diese Zeichen in die Symbole für die englischsprachige Version übersetzt oder transformiert werden können.</span><span class="sxs-lookup"><span data-stu-id="ec4a2-108">Instead use (c) and (r), because these characters can be translated or transformed to the symbols for the English-language version.</span></span> <span data-ttu-id="ec4a2-109">Diese neutrale Datenbank kann dann durch Festlegen der Codepage und durch das Hinzufügen von Lokalisierungs Informationen durch Tabellen Bearbeitung oder durch Importieren von Textarchiv Dateien lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec4a2-109">This neutral database can then be localized by setting its code page and adding localization information by table editing or by importing text archive files.</span></span>

 

 



