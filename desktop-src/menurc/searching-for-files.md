---
title: Dateien werden gesucht
description: Standardmäßig sucht RC nach Header Dateien und Ressourcen Dateien (z. b. Symbol-und Cursor Dateien) zuerst im aktuellen Verzeichnis und dann in den Verzeichnissen, die durch die include-Umgebungsvariable angegeben werden.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342073"
---
# <a name="searching-for-files"></a><span data-ttu-id="6faf9-103">Dateien werden gesucht</span><span class="sxs-lookup"><span data-stu-id="6faf9-103">Searching for Files</span></span>

<span data-ttu-id="6faf9-104">Standardmäßig sucht RC nach Header Dateien und Ressourcen Dateien (z. b. Symbol-und Cursor Dateien) zuerst im aktuellen Verzeichnis und dann in den Verzeichnissen, die durch die include-Umgebungsvariable angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6faf9-104">By default, RC searches for header files and resource files (such as icon and cursor files) first in the current directory and then in the directories specified by the INCLUDE environment variable.</span></span> <span data-ttu-id="6faf9-105">(Die PATH-Umgebungsvariable hat keine Auswirkung darauf, welche Verzeichnisse RC durchsucht.)</span><span class="sxs-lookup"><span data-stu-id="6faf9-105">(The PATH environment variable has no effect on which directories RC searches.)</span></span>

## <a name="adding-a-directory-to-search"></a><span data-ttu-id="6faf9-106">Hinzufügen eines zu suchenden Verzeichnisses</span><span class="sxs-lookup"><span data-stu-id="6faf9-106">Adding a Directory to Search</span></span>

<span data-ttu-id="6faf9-107">Sie können die **/i** -Option verwenden, um ein Verzeichnis zur Liste der Verzeichnisse RC-Suchvorgänge hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6faf9-107">You can use the **/i** option to add a directory to the list of directories RC searches.</span></span> <span data-ttu-id="6faf9-108">Der Compiler durchsucht dann die Verzeichnisse in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="6faf9-108">The compiler then searches the directories in the following order:</span></span>

1.  <span data-ttu-id="6faf9-109">Das aktuelle Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="6faf9-109">The current directory</span></span>
2.  <span data-ttu-id="6faf9-110">Das Verzeichnis oder die Verzeichnisse, die Sie mithilfe der **/i** -Option angeben, in der Reihenfolge, in der Sie in der RC-Befehlszeile angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6faf9-110">The directory or directories you specify by using the **/i** option, in the order in which they appear on the RC command line</span></span>
3.  <span data-ttu-id="6faf9-111">Die Liste der von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse in der Reihenfolge, in der Sie von der Variablen aufgelistet werden, es sei denn, Sie geben die Option **/x** an.</span><span class="sxs-lookup"><span data-stu-id="6faf9-111">The list of directories specified by the INCLUDE environment variable, in the order in which the variable lists them, unless you specify the **/x** option</span></span>

<span data-ttu-id="6faf9-112">Im folgenden Beispiel wird die Ressourcen Definitionsdatei MyApp. RC kompiliert:</span><span class="sxs-lookup"><span data-stu-id="6faf9-112">The following example compiles the resource-definition file MyApp.rc:</span></span>

<span data-ttu-id="6faf9-113">**RC/i c: \\ Source \\ stuff/i d: \\ Ressourcen MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="6faf9-113">**rc /i c:\\source\\stuff /i d:\\resources myapp.rc**</span></span>

<span data-ttu-id="6faf9-114">Beim Kompilieren des Skripts MyApp. RC sucht RC zunächst im aktuellen Verzeichnis nach Header Dateien und Ressourcen Dateien, dann in C: \\ Quell \\ Sachen und D: \\ Ressourcen und dann in den Verzeichnissen, die durch die include-Umgebungsvariable angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6faf9-114">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory, then in C:\\Source\\Stuff and D:\\Resources, and then in the directories specified by the INCLUDE environment variable.</span></span>

## <a name="ignoring-the-include-environment-variable"></a><span data-ttu-id="6faf9-115">Die include-Umgebungs Variable wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6faf9-115">Ignoring the INCLUDE Environment Variable</span></span>

<span data-ttu-id="6faf9-116">Sie können verhindern, dass RC die include-Umgebungsvariable verwendet, wenn Sie die zu durchsuchenden Verzeichnisse ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6faf9-116">You can prevent RC from using the INCLUDE environment variable when determining the directories to search.</span></span> <span data-ttu-id="6faf9-117">Verwenden Sie hierzu die Option **/x** .</span><span class="sxs-lookup"><span data-stu-id="6faf9-117">To do so, use the **/x** option.</span></span> <span data-ttu-id="6faf9-118">Der Compiler sucht dann nur im aktuellen Verzeichnis und in den Verzeichnissen, die Sie mithilfe der **/i** -Option angeben, nach Dateien.</span><span class="sxs-lookup"><span data-stu-id="6faf9-118">The compiler then searches for files only in the current directory and in any directories you specify by using the **/i** option.</span></span>

<span data-ttu-id="6faf9-119">Mit dem folgenden Befehl wird die Skriptdatei "MyApp. RC" kompiliert:</span><span class="sxs-lookup"><span data-stu-id="6faf9-119">The following command compiles the script file MyApp.rc:</span></span>

<span data-ttu-id="6faf9-120">**RC/x/i c: \\ Source \\ Sachen MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="6faf9-120">**rc /x /i c:\\source\\stuff myapp.rc**</span></span>

<span data-ttu-id="6faf9-121">Beim Kompilieren des Skripts MyApp. RC sucht RC zunächst im aktuellen Verzeichnis nach Header Dateien und Ressourcen Dateien und dann in C: \\ Source \\ .</span><span class="sxs-lookup"><span data-stu-id="6faf9-121">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory and then in C:\\Source\\Stuff.</span></span> <span data-ttu-id="6faf9-122">Die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse werden nicht durchsucht.</span><span class="sxs-lookup"><span data-stu-id="6faf9-122">It does not search the directories specified by the INCLUDE environment variable.</span></span>

 

 




