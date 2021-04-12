---
description: In diesem Thema wird beschrieben, wie ein generischer Experte erstellt wird, der mit dem Netzwerkmonitor SDK ausgeliefert wird.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Entwickeln eines Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215892"
---
# <a name="building-an-expert"></a><span data-ttu-id="7bf16-103">Entwickeln eines Experten</span><span class="sxs-lookup"><span data-stu-id="7bf16-103">Building an Expert</span></span>

<span data-ttu-id="7bf16-104">In diesem Thema wird beschrieben, wie ein generischer Experte erstellt wird, der mit dem Netzwerkmonitor SDK ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="7bf16-104">This topic describes how to build a generic expert that ships with the Network Monitor SDK.</span></span>

> [!Note]  
> <span data-ttu-id="7bf16-105">Installieren Sie vor dem Erstellen der folgenden Codebeispiele das Netzwerkmonitor SDK, und initialisieren Sie die Datei MySetEnv.bat.</span><span class="sxs-lookup"><span data-stu-id="7bf16-105">Before creating the following code examples, install the Network Monitor SDK and initialize the MySetEnv.bat file.</span></span>

 

<span data-ttu-id="7bf16-106">**So erstellen Sie einen generischen Experten**</span><span class="sxs-lookup"><span data-stu-id="7bf16-106">**To build a generic expert**</span></span>

1.  <span data-ttu-id="7bf16-107">Öffnen Sie eine Netzwerkmonitor Eingabeaufforderung, und navigieren Sie zum \\ Unterverzeichnis Experts, z. b \\ . C: Program Files \\ NetMonSDK2 \\ Experten.</span><span class="sxs-lookup"><span data-stu-id="7bf16-107">Open a Network Monitor command prompt and navigate to the \\Experts subdirectory; for example, C:\\Program Files\\NetMonSDK2\\Experts.</span></span>
2.  <span data-ttu-id="7bf16-108">Type **xcopy/e/s/v blrplate myexpert**; Wenn Sie dazu aufgefordert werden, geben Sie **D** ein.</span><span class="sxs-lookup"><span data-stu-id="7bf16-108">Type **xcopy /e /s /v Blrplate MyExpert**; then, when prompted, type **D**.</span></span>
3.  <span data-ttu-id="7bf16-109">Wechseln Sie zum \\ Unterverzeichnis myexpert.</span><span class="sxs-lookup"><span data-stu-id="7bf16-109">Move to the \\MyExpert subdirectory.</span></span>
4.  <span data-ttu-id="7bf16-110">Geben Sie **ren blrplate ein \* . \* Myexpert \* . \***.</span><span class="sxs-lookup"><span data-stu-id="7bf16-110">Type **ren Blrplate\*.\* MyExpert\*.\***.</span></span> <span data-ttu-id="7bf16-111">Stellen Sie sicher, dass alle Dateien ordnungsgemäß umbenannt wurden.</span><span class="sxs-lookup"><span data-stu-id="7bf16-111">Ensure that all files are properly renamed.</span></span> <span data-ttu-id="7bf16-112">Überprüfen Sie die Dateinamen, indem Sie die Dateien im \\ \\ Unterverzeichnis "Experten blrplate" vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7bf16-112">Verify the file names by comparing the files in the \\Experts\\Blrplate subdirectory.</span></span>
5.  <span data-ttu-id="7bf16-113">Bearbeiten Sie das Makefile, indem Sie alle Vorkommen von **blrplate** durch **myexpert** ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7bf16-113">Edit the Makefile by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
6.  <span data-ttu-id="7bf16-114">Bearbeiten Sie beide cpp-Dateien, indem Sie alle Vorkommen von **blrplate** durch **myexpert** ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7bf16-114">Edit both .cpp files by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span> <span data-ttu-id="7bf16-115">Beachten Sie, dass der Dialogfeld Bezeichner in der Datei "config. cpp" groß geschrieben werden muss (z. b. **myexpert**).</span><span class="sxs-lookup"><span data-stu-id="7bf16-115">Be aware that the dialog box identifier in Config.cpp must be capitalized (for example, **MYEXPERT**).</span></span>
7.  <span data-ttu-id="7bf16-116">Bearbeiten Sie myexpert. h, indem Sie alle Vorkommen von **blrplate** durch **myexpert** ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7bf16-116">Edit MyExpert.h by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
8.  <span data-ttu-id="7bf16-117">Bearbeiten Sie Resrc1. h durch Umbenennen von **blrplate** in **myexpert**</span><span class="sxs-lookup"><span data-stu-id="7bf16-117">Edit Resrc1.h by renaming **BLRPLATE** to **MYEXPERT**.</span></span> <span data-ttu-id="7bf16-118">(Beachten Sie, dass **myexpert** groß geschrieben werden muss.)</span><span class="sxs-lookup"><span data-stu-id="7bf16-118">(Remember, **MYEXPERT** must be capitalized).</span></span>
9.  <span data-ttu-id="7bf16-119">Bearbeiten Sie die Datei myexpert. RC, indem Sie **IDD \_ blrplate \_ config \_ Dialog** in **IDD \_ myexpert \_ config \_ Dialog** umbenennen.</span><span class="sxs-lookup"><span data-stu-id="7bf16-119">Edit the MyExpert.rc file by renaming **IDD\_BLRPLATE\_CONFIG\_DIALOG** to **IDD\_MYEXPERT\_CONFIG\_DIALOG**.</span></span>
10. <span data-ttu-id="7bf16-120">Geben Sie **NMAKE** ein, um die DLL-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bf16-120">Type **nmake** to build the DLL file.</span></span> <span data-ttu-id="7bf16-121">Wechseln Sie zum Überprüfen des Builds in das \\ obj-Unterverzeichnis, und überprüfen Sie, ob die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7bf16-121">To verify the build, change directory to the \\Obj subdirectory and verify that the file exists.</span></span> <span data-ttu-id="7bf16-122">Weitere Informationen finden Sie unter [Anzeigen von Eigenschaften der expertendll](viewing-expert-dll-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7bf16-122">For more information, see [Viewing Expert DLL Properties](viewing-expert-dll-properties.md).</span></span>

<span data-ttu-id="7bf16-123">Nachdem der Build fertiggestellt wurde, verfügen Sie über eine Experten-dll, die Sie mit Netzwerkmonitor testen und bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="7bf16-123">When the build is complete, you will have an expert DLL that you can test and deploy with Network Monitor.</span></span> <span data-ttu-id="7bf16-124">Weitere Informationen zum Installieren eines Experten finden Sie unter [Installieren eines Experten in Netzwerkmonitor 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="7bf16-124">For more information about installing an expert, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span> <span data-ttu-id="7bf16-125">Weitere Informationen zum Debuggen eines Experten finden Sie unter [Debuggen eines Experten](debugging-an-expert.md).</span><span class="sxs-lookup"><span data-stu-id="7bf16-125">For more information about debugging an expert, see [Debugging an Expert](debugging-an-expert.md).</span></span>

 

 



