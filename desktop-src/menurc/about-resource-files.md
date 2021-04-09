---
title: Informationen zu Ressourcen Dateien
description: Hier wird beschrieben, wie Sie Ressourcen in die Windows-basierte Anwendung mit RC einbinden.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036967"
---
# <a name="about-resource-files"></a><span data-ttu-id="6c283-103">Informationen zu Ressourcen Dateien</span><span class="sxs-lookup"><span data-stu-id="6c283-103">About Resource Files</span></span>

<span data-ttu-id="6c283-104">Gehen Sie folgendermaßen vor, um Ressourcen in die Windows-basierte Anwendung mit RC einzuschließen:</span><span class="sxs-lookup"><span data-stu-id="6c283-104">To include resources in your Windows-based application with RC, do the following:</span></span>

1.  <span data-ttu-id="6c283-105">Erstellen Sie einzelne Dateien für Ihre Cursor, Symbole, Bitmaps, Dialogfelder und Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="6c283-105">Create individual files for your cursors, icons, bitmaps, dialog boxes, and fonts.</span></span>
2.  <span data-ttu-id="6c283-106">Erstellen Sie ein Ressourcen Definitions Skript (RC-Datei), das die von der Anwendung verwendeten Ressourcen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6c283-106">Create a resource-definition script (.rc file) that describes the resources used by your application.</span></span>
3.  <span data-ttu-id="6c283-107">Kompilieren Sie das Skript mit RC.</span><span class="sxs-lookup"><span data-stu-id="6c283-107">Compile the script with RC.</span></span> <span data-ttu-id="6c283-108">Weitere Informationen finden Sie unter [Verwenden von RC (RC-Befehlszeile)](using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="6c283-108">For more information, see [Using RC (The RC Command Line)](using-rc-the-rc-command-line-.md).</span></span>
4.  <span data-ttu-id="6c283-109">Verknüpfen Sie die kompilierte Ressourcen Datei (. res) mit dem Linker in der ausführbaren Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c283-109">Link the compiled resource (.res) file into the application's executable file with your linker.</span></span>

<span data-ttu-id="6c283-110">Eine Ressourcen Datei ist eine Textdatei mit der Erweiterung. rc.</span><span class="sxs-lookup"><span data-stu-id="6c283-110">A resource file is a text file with the extension .rc.</span></span> <span data-ttu-id="6c283-111">Die Datei kann Einzel Byte-, Doppelbyte-oder Unicode-Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c283-111">The file can use single-byte, double-byte, or Unicode characters.</span></span> <span data-ttu-id="6c283-112">Die Syntax und die Semantik für den RC-Präprozessor ähneln denen des Microsoft C/C++-Compilers.</span><span class="sxs-lookup"><span data-stu-id="6c283-112">The syntax and semantics for the RC preprocessor are similar to those of the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="6c283-113">RC unterstützt jedoch eine Teilmenge der Präprozessordirektiven, Definitionen und Pragmas in einem Skript.</span><span class="sxs-lookup"><span data-stu-id="6c283-113">However, RC supports a subset of the preprocessor directives, defines, and pragmas in a script.</span></span>

<span data-ttu-id="6c283-114">Die Skriptdatei definiert Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6c283-114">The script file defines resources.</span></span> <span data-ttu-id="6c283-115">Für eine Ressource, die in einer separaten Datei vorhanden ist, z. b. ein Symbol oder einen Cursor, gibt das Skript die Ressource und die Datei an, in der Sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6c283-115">For a resource that exists in a separate file, such as an icon or cursor, the script specifies the resource and the file that contains it.</span></span> <span data-ttu-id="6c283-116">Bei einigen Ressourcen, z. b. einem Menü, ist die gesamte Definition der Ressource im Skript vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c283-116">For some resources, such as a menu, the entire definition of the resource exists within the script.</span></span>

<span data-ttu-id="6c283-117">In den folgenden Themen werden die Informationen beschrieben, die eine Skriptdatei enthalten kann:</span><span class="sxs-lookup"><span data-stu-id="6c283-117">The following topics describe the information a script file can contain:</span></span>

-   <span data-ttu-id="6c283-118">[Kommentare](comments.md), bei denen es sich um Notizen handelt, die von RC ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="6c283-118">[Comments](comments.md), which are notes to be ignored by RC.</span></span>
-   <span data-ttu-id="6c283-119">[Vordefinierte Makros](predefined-macros.md), die keine Argumente annehmen und nicht neu definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="6c283-119">[Predefined macros](predefined-macros.md), which take no arguments and cannot be redefined.</span></span>
-   <span data-ttu-id="6c283-120">[Präprozessordirektiven](preprocessor-directives.md), die RC anweisen, vor dem Kompilieren Aktionen für das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6c283-120">[Preprocessor directives](preprocessor-directives.md), which instruct RC to perform actions on the script before compiling it.</span></span>
-   <span data-ttu-id="6c283-121">[Präprozessoroperatoren](preprocessor-operators.md), die mit der **\# define** -Direktive verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c283-121">[Preprocessor operators](preprocessor-operators.md), which are used with the **\#define** directive.</span></span>
-   [<span data-ttu-id="6c283-122">Pragma-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="6c283-122">Pragma directives</span></span>](pragma-directives.md)
-   <span data-ttu-id="6c283-123">[Ressourcen Definitions Anweisungen](resource-definition-statements.md), die Ressourcen benennen und beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6c283-123">[Resource-definition statements](resource-definition-statements.md), which name and describe resources.</span></span>

 

 




