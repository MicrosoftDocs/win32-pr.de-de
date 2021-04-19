---
description: Die Ressourcen Vorbereitung für eine MUI-Anwendung unterstützt sowohl Win32 PE-als auch nicht-Win32 PE-Modelle.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Vorbereiten von Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352663"
---
# <a name="preparing-resources"></a><span data-ttu-id="918df-103">Vorbereiten von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="918df-103">Preparing Resources</span></span>

<span data-ttu-id="918df-104">Die Ressourcen Vorbereitung für eine MUI-Anwendung unterstützt sowohl Win32 PE-als auch nicht-Win32 PE-Modelle.</span><span class="sxs-lookup"><span data-stu-id="918df-104">Resource preparation for a MUI application supports both Win32 PE and non-Win32 PE models.</span></span> <span data-ttu-id="918df-105">Win32 PE-Ressourcen werden in PE-basierten Dateien, z. b. dll-, exe-oder sys-Dateien, bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="918df-105">Win32 PE resources are provided in PE-based files, such as .dll, .exe, or .sys files.</span></span> <span data-ttu-id="918df-106">Nicht-Win32 PE-Ressourcen werden in einem benutzerdefinierten Modul Ihrer Wahl bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="918df-106">Non-Win32 PE resources are furnished in a customized module of your choosing.</span></span>

> [!Note]  
> <span data-ttu-id="918df-107">Es wird dringend empfohlen, Win32 PE-Ressourcen für Win32-MUI-Anwendungen zu verwenden, da diese Ressourcen vollständig von der MUI-Ressourcen Technologie unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="918df-107">It is highly recommended for you to use Win32 PE resources for Win32 MUI applications, as these resources are completely supported by the MUI resource technology.</span></span> <span data-ttu-id="918df-108">Nicht-Win32 PE-Ressourcen Dateien können durch Aufrufen der [**getfilemuipath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) -Funktion aufgerufen werden, wie in Suchen von [nicht-Win32 PE-Ressourcen](locating-non-win32-pe-resources.md)beschrieben, aber die Anwendung muss eigene Funktionen bereitstellen, um die erforderlichen Ressourcen zu finden und zu laden.</span><span class="sxs-lookup"><span data-stu-id="918df-108">Non-Win32 PE resource files can be located by calling the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function as described in [Locating Non-Win32 PE Resources](locating-non-win32-pe-resources.md), but the application must provide its own functionality to find and load the required resources.</span></span>

 

<span data-ttu-id="918df-109">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="918df-109">This section contains the following topics:</span></span>

-   [<span data-ttu-id="918df-110">Erstellen der Ressourcen Datei für die Basis Sprache</span><span class="sxs-lookup"><span data-stu-id="918df-110">Creating the Base Language Resource File</span></span>](creating-the-base-language-resource-file.md)
-   [<span data-ttu-id="918df-111">Verwenden von Registrierungs Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="918df-111">Using Registry String Redirection</span></span>](using-registry-string-redirection.md)
-   [<span data-ttu-id="918df-112">Vorbereiten einer Ressourcen Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="918df-112">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)

 

 



