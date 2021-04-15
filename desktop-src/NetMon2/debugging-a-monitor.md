---
description: Im folgenden Verfahren wird veranschaulicht, wie ein Monitor debuggt wird.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Debuggen eines Monitors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529018"
---
# <a name="debugging-a-monitor"></a><span data-ttu-id="176f1-103">Debuggen eines Monitors</span><span class="sxs-lookup"><span data-stu-id="176f1-103">Debugging a Monitor</span></span>

<span data-ttu-id="176f1-104">Im folgenden Verfahren wird veranschaulicht, wie ein Monitor debuggt wird.</span><span class="sxs-lookup"><span data-stu-id="176f1-104">The following procedure demonstrates how to debug a monitor.</span></span>

<span data-ttu-id="176f1-105">**So debuggen Sie einen Monitor**</span><span class="sxs-lookup"><span data-stu-id="176f1-105">**To debug a monitor**</span></span>

1.  <span data-ttu-id="176f1-106">Installieren Sie die Monitor-DLL und die Programm Datenbankdatei (. pdb), die bei der Kompilierung des Monitors am richtigen Speicherort generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="176f1-106">Install the monitor DLL and the program database (.pdb) file generated when you compiled the monitor in the correct location.</span></span> <span data-ttu-id="176f1-107">Weitere Informationen finden [Sie unter Installieren eines Monitors zum Netzwerkmonitor](installing-a-monitor-to-network-monitor.md) .</span><span class="sxs-lookup"><span data-stu-id="176f1-107">See [Installing a Monitor to Network Monitor](installing-a-monitor-to-network-monitor.md) for further details.</span></span>
2.  <span data-ttu-id="176f1-108">Überprüfen Sie, ob der Überwachungs Steuerungs Dienst als Server anstelle eines Diensts konfiguriert ist, indem Sie die Option Systemsteuerung, Dienste auswählen.</span><span class="sxs-lookup"><span data-stu-id="176f1-108">Verify that the Monitor Control Service is configured as a server instead of a service by selecting Control Panel, Services.</span></span>
3.  <span data-ttu-id="176f1-109">Öffnen Sie eine Eingabeaufforderung, und wechseln Sie zum Netzwerkmonitor Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="176f1-109">Open a command prompt and go to the Network Monitor directory.</span></span> <span data-ttu-id="176f1-110">Typ:</span><span class="sxs-lookup"><span data-stu-id="176f1-110">Type:</span></span>

    <span data-ttu-id="176f1-111">**Mcsvc.exe/RegServer**</span><span class="sxs-lookup"><span data-stu-id="176f1-111">**Mcsvc.exe /RegServer**</span></span>

    <span data-ttu-id="176f1-112">Nachdem die Debugsitzung des Monitors ausgeführt wurde, können Sie die mcsvc-Datei an die Standard Bedingung zurückgeben, indem Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="176f1-112">After the monitor debugging session is complete, you can return the MCSVC to its default condition by typing:</span></span>

    <span data-ttu-id="176f1-113">**Mcsvc.exe/Service**</span><span class="sxs-lookup"><span data-stu-id="176f1-113">**Mcsvc.exe /Service**</span></span>

4.  <span data-ttu-id="176f1-114">Starten Sie Microsoft Visual C++ in Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="176f1-114">In Microsoft Visual Studio, launch Microsoft Visual C++.</span></span>
5.  <span data-ttu-id="176f1-115">Wählen Sie in der Menüoption **Datei** **Öffnen** den Namen Ihrer Monitor-DLL aus.</span><span class="sxs-lookup"><span data-stu-id="176f1-115">From the **File**, **Open** menu option, select the name of your monitor DLL.</span></span>
6.  <span data-ttu-id="176f1-116">Nachdem Microsoft Visual C++ geladen ist, klicken Sie auf **Projekt** und dann auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="176f1-116">After Microsoft Visual C++ loads, click **Project**, **Settings**.</span></span>
7.  <span data-ttu-id="176f1-117">Klicken Sie unter **ausführbare Datei** für Debugsitzung auf die Registerkarte **Debuggen** , und geben Sie den voll Mcsvc.exe ständigen</span><span class="sxs-lookup"><span data-stu-id="176f1-117">Click the **Debug** tab under **Executable** for debug session and type the full path of Mcsvc.exe.</span></span> <span data-ttu-id="176f1-118">Beispiel: C: \\ Program Files \\ Netmon2 \\Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="176f1-118">For example, C:\\Program files\\Netmon2\\Mcsvc.exe.</span></span>
8.  <span data-ttu-id="176f1-119">Legen Sie die Breakpoints im Code fest.</span><span class="sxs-lookup"><span data-stu-id="176f1-119">Set the breakpoints in the code.</span></span>

> [!Note]  
> <span data-ttu-id="176f1-120">Verwenden Sie kein Meldungs Feld zum Debuggen von Monitoren.</span><span class="sxs-lookup"><span data-stu-id="176f1-120">Do not use a message box for monitor debugging.</span></span> <span data-ttu-id="176f1-121">Wenn der mcsvc als Dienst ausgeführt wird, wird das Popup nicht angezeigt, und mcsvc scheint zu hängen.</span><span class="sxs-lookup"><span data-stu-id="176f1-121">If the MCSVC is running as a service, you will not see the popup, and MCSVC will appear to hang.</span></span>

 

 

 



