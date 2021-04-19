---
description: Verwenden Sie das folgende Verfahren, um in Microsoft Visual C++ geschriebene Experten zu debuggen.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Debuggen eines Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349498"
---
# <a name="debugging-an-expert"></a><span data-ttu-id="3148d-103">Debuggen eines Experten</span><span class="sxs-lookup"><span data-stu-id="3148d-103">Debugging an Expert</span></span>

<span data-ttu-id="3148d-104">Verwenden Sie das folgende Verfahren, um in Microsoft Visual C++ geschriebene Experten zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="3148d-104">Use the following procedure to debug experts written in Microsoft Visual C++.</span></span>

<span data-ttu-id="3148d-105">**Debuggen eines Experten**</span><span class="sxs-lookup"><span data-stu-id="3148d-105">**Debugging an Expert**</span></span>

1.  <span data-ttu-id="3148d-106">Installieren Sie den Experten (DLL-Datei) und die Programm Datenbankdatei (. pdb), die bei der Kompilierung des Experten am richtigen Speicherort generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3148d-106">Install the expert (DLL file) and the program database file (.pdb) generated when you compiled the expert in the correct location.</span></span> <span data-ttu-id="3148d-107">Weitere Informationen finden Sie unter [Installieren eines Experten in Netzwerkmonitor 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="3148d-107">For further details, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="3148d-108">Starten Sie Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="3148d-108">Start Microsoft Visual C++.</span></span>
3.  <span data-ttu-id="3148d-109">Klicken Sie im Menü **Datei** auf **Öffnen** , und wählen Sie den Namen ihrer Experten-dll aus.</span><span class="sxs-lookup"><span data-stu-id="3148d-109">From the **File** menu, click **Open** and select the name of your expert DLL.</span></span>
4.  <span data-ttu-id="3148d-110">Nachdem Microsoft Visual C++ geladen ist, klicken Sie auf das Menü **Projekt** , und klicken Sie dann auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="3148d-110">After Microsoft Visual C++ loads, click the **Project** menu and then click **Settings**.</span></span>
5.  <span data-ttu-id="3148d-111">Klicken Sie auf **Debug**.</span><span class="sxs-lookup"><span data-stu-id="3148d-111">Click **Debug**.</span></span> <span data-ttu-id="3148d-112">Geben Sie unter **ausführbare Datei für Debugsitzung** den vollständigen Pfad Netmon.exe ein, z. b.:</span><span class="sxs-lookup"><span data-stu-id="3148d-112">Under **Executable for debug session**, type the full path of Netmon.exe, for example:</span></span>

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  <span data-ttu-id="3148d-113">Legen Sie die Breakpoints im Code fest.</span><span class="sxs-lookup"><span data-stu-id="3148d-113">Set the breakpoints in your code.</span></span>

 

 



