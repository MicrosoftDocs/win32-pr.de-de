---
description: Erstellen der Ressourcen Datei für die Basis Sprache
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Erstellen der Ressourcen Datei für die Basis Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050394"
---
# <a name="creating-the-base-language-resource-file"></a><span data-ttu-id="ada82-103">Erstellen der Ressourcen Datei für die Basis Sprache</span><span class="sxs-lookup"><span data-stu-id="ada82-103">Creating the Base Language Resource File</span></span>

<span data-ttu-id="ada82-104">Ressourcen für Elemente der Benutzeroberfläche werden für die grundlegende Sprache definiert, die von der Anwendung unterstützt wird, z. b. Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="ada82-104">Resources for user interface elements are defined for the basic language that the application supports, for example, English (United States).</span></span> <span data-ttu-id="ada82-105">Ein Beispiel für eine Win32 PE-Ressourcen Datei ist eine RC-Datei, die mit dem RC-Compiler erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ada82-105">An example of a Win32 PE resource file is an .rc file, created using RC Compiler.</span></span> <span data-ttu-id="ada82-106">Ausführliche Informationen zum Erstellen von RC-Dateien finden Sie unter Informationen [zu Ressourcen Dateien](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="ada82-106">For details of .rc file creation, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="ada82-107">Wenn Sie eine RC-Datei für die Basis Sprachen Ressourcen verwenden, haben Sie die Möglichkeit, eine Ressourcen Konfigurationsdatei für eine XML-Darstellung der Ressourcen Konfigurationsdaten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ada82-107">If using an .rc file for the base language resources, you have the option of using a resource configuration file for an XML representation of resource configuration data.</span></span> <span data-ttu-id="ada82-108">Informationen zum Erstellen dieser Datei finden Sie unter [Vorbereiten einer Ressourcen Konfigurationsdatei](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="ada82-108">To create this file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="ada82-109">Sie können auch eine nicht-Win32 PE-Datei verwenden, um Basis Sprachen Ressourcen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ada82-109">You can also use a non-Win32 PE file to define base language resources.</span></span> <span data-ttu-id="ada82-110">Beispielsweise können Sie eine XML-Datei oder eine txt-Datei zu diesem Zweck verwenden.</span><span class="sxs-lookup"><span data-stu-id="ada82-110">For example, you might use an .xml file or .txt file for this purpose.</span></span>

> [!Note]  
> <span data-ttu-id="ada82-111">Wenn Sie Basis Sprachen Ressourcen mit einer nicht-Win32-PE-Datei definieren, können Sie den RC-Compiler nicht für die Ressourcendefinition verwenden.</span><span class="sxs-lookup"><span data-stu-id="ada82-111">When you define base language resources using a non-Win32 PE file, you cannot use RC Compiler for resource definition.</span></span> <span data-ttu-id="ada82-112">Stattdessen definieren Sie ein eigenes Ressourcen Format, und Ihre Anwendung muss Ihre eigene Funktionalität bereitstellen, um die erforderlichen Ressourcen zu suchen und zu laden.</span><span class="sxs-lookup"><span data-stu-id="ada82-112">Instead, you define your own resource format, and your application must provide its own functionality to find and load the required resources.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ada82-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ada82-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ada82-114">Vorbereiten von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ada82-114">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="ada82-115">Vorbereiten einer Ressourcen Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="ada82-115">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
