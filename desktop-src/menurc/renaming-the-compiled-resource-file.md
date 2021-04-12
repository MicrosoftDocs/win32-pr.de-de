---
title: Umbenennen der kompilierten Ressourcen Datei
description: Bei der Ressourcen Kompilierung benennt RC die kompilierte Ressourcen Datei (. res) standardmäßig mit dem Basis Namen der RC-Datei und platziert Sie im gleichen Verzeichnis wie die RC-Datei.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206314"
---
# <a name="renaming-the-compiled-resource-file"></a><span data-ttu-id="0fa8f-103">Umbenennen der kompilierten Ressourcen Datei</span><span class="sxs-lookup"><span data-stu-id="0fa8f-103">Renaming the Compiled Resource File</span></span>

<span data-ttu-id="0fa8f-104">Bei der Ressourcen Kompilierung benennt RC die kompilierte Ressourcen Datei (. res) standardmäßig mit dem Basis Namen der RC-Datei und platziert Sie im gleichen Verzeichnis wie die RC-Datei.</span><span class="sxs-lookup"><span data-stu-id="0fa8f-104">By default, when compiling resources, RC names the compiled resource (.res) file with the base name of the .rc file and places it in the same directory as the .rc file.</span></span> <span data-ttu-id="0fa8f-105">CVTRES muss dann aufgerufen werden, um die res-Datei in ein binäres Ressourcen Format (. RBJ) zu konvertieren, das vom Linker interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0fa8f-105">CVTRES must then be invoked to convert the .res file to a binary resource (.rbj) format which can be understood by the linker.</span></span> <span data-ttu-id="0fa8f-106">Im folgenden Beispiel wird "MyApp. RC" kompiliert und eine kompilierte Ressourcen Datei mit dem Namen "MyApp. res" im selben Verzeichnis wie "MyApp. RC" erstellt:</span><span class="sxs-lookup"><span data-stu-id="0fa8f-106">The following example compiles MyApp.rc and creates a compiled resource file named MyApp.res in the same directory as MyApp.rc:</span></span>

<span data-ttu-id="0fa8f-107">**RC MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="0fa8f-107">**rc myapp.rc**</span></span>

<span data-ttu-id="0fa8f-108">Die **/FO** -Option gibt der resultierenden res-Datei einen Namen, der sich vom Namen der entsprechenden RC-Datei unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="0fa8f-108">The **/fo** option gives the resulting .res file a name that differs from the name of the corresponding .rc file.</span></span> <span data-ttu-id="0fa8f-109">Verwenden Sie z. b. den folgenden Befehl, um die resultierende res-Datei "newFile. res" zu benennen:</span><span class="sxs-lookup"><span data-stu-id="0fa8f-109">For example, to name the resulting .res file NewFile.res, use the following command:</span></span>

<span data-ttu-id="0fa8f-110">**RC-FO newFile. res MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="0fa8f-110">**rc -fo newfile.res myapp.rc**</span></span>

<span data-ttu-id="0fa8f-111">Die **/FO** -Option kann die res-Datei auch in einem anderen Verzeichnis platzieren.</span><span class="sxs-lookup"><span data-stu-id="0fa8f-111">The **/fo** option can also place the .res file in a different directory.</span></span> <span data-ttu-id="0fa8f-112">Beispielsweise wird mit dem folgenden Befehl die kompilierte Ressourcen Datei "MyApp. res" in das Verzeichnis "C: Source" eingefügt \\ \\ :</span><span class="sxs-lookup"><span data-stu-id="0fa8f-112">For example, the following command places the compiled resource file MyApp.res in the directory C:\\Source\\Resource:</span></span>

<span data-ttu-id="0fa8f-113">**RC-FO c: \\ Quell \\ Ressource \\ myapp. res MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="0fa8f-113">**rc -fo c:\\source\\resource\\myapp.res myapp.rc**</span></span>

 

 




