---
title: Einrichten der Umgebung
description: Das installierte Platform Software Development Kit (SDK) stellt eine Setenv.bat-Datei im Stammverzeichnis des Platform SDK bereit, das Sie ausführen können, um Ihre Umgebung für die Entwicklung von Anwendungen einzurichten, die das Platform SDK verwenden.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341851"
---
# <a name="environment-setup"></a><span data-ttu-id="39c7f-103">Einrichten der Umgebung</span><span class="sxs-lookup"><span data-stu-id="39c7f-103">Environment Setup</span></span>

<span data-ttu-id="39c7f-104">Das installierte Platform Software Development Kit (SDK) stellt eine Setenv.bat-Datei im Stammverzeichnis des Platform SDK bereit, das Sie ausführen können, um Ihre Umgebung für die Entwicklung von Anwendungen einzurichten, die das Platform SDK verwenden.</span><span class="sxs-lookup"><span data-stu-id="39c7f-104">The installed Platform Software Development Kit (SDK) provides a Setenv.bat file located in the root directory of the Platform SDK that you can run to set up your environment for building applications that use the Platform SDK.</span></span>

## <a name="settings-and-variables"></a><span data-ttu-id="39c7f-105">Einstellungen und Variablen</span><span class="sxs-lookup"><span data-stu-id="39c7f-105">Settings and Variables</span></span>

<span data-ttu-id="39c7f-106">Sie können Ihre Umgebung auch manuell einrichten, indem Sie Ihrer Autoexec.bat-Datei etwas wie das folgende hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="39c7f-106">You can also manually set up your environment by adding something like the following to your Autoexec.bat file.</span></span> <span data-ttu-id="39c7f-107">Mithilfe von Windows können Sie die Autoexec.bat Datei bearbeiten, um diese Befehle einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="39c7f-107">Using Windows, you can edit the Autoexec.bat file to include these commands.</span></span> <span data-ttu-id="39c7f-108">Mithilfe von Windows Server 2003, Windows XP, Windows 2000 oder Windows NT können Sie diese Einstellungen mithilfe des System Dialogfelds, das Sie in der Systemsteuerung ausführen können, den Umgebungsvariablen bearbeiten oder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="39c7f-108">Using Windows Server 2003, Windows XP, Windows 2000, or Windows NT, you can edit or add these settings to your environment variables using the System dialog that you can run from the Control Panel.</span></span>


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



<span data-ttu-id="39c7f-109">Diese Einstellungen sind für eine Plattform von Intel 80386 oder höher geeignet, auf der Windows Me, Windows 98 oder Windows 95 ausgeführt wird und auf denen sowohl Microsoft Visual C++ als auch das Platform SDK installiert sind.</span><span class="sxs-lookup"><span data-stu-id="39c7f-109">These settings are appropriate for an Intel 80386 or later platform running Windows Me, Windows 98, or Windows 95 with both Microsoft Visual C++ and the Platform SDK installed.</span></span> <span data-ttu-id="39c7f-110">Beispielsweise wird auf diesem System Visual C++ Version 5,0 unter dem Verzeichnis C: \\ Msdev installiert.</span><span class="sxs-lookup"><span data-stu-id="39c7f-110">For example, on this system, Visual C++ version 5.0 is installed under the C:\\MSDEV directory.</span></span> <span data-ttu-id="39c7f-111">Das Platform SDK wird unter dem Verzeichnis "D: \\ Mssdk" installiert.</span><span class="sxs-lookup"><span data-stu-id="39c7f-111">The Platform SDK is installed under the D:\\MSSDK directory.</span></span> <span data-ttu-id="39c7f-112">Die Datenträger Konfiguration ist möglicherweise anders.</span><span class="sxs-lookup"><span data-stu-id="39c7f-112">Your disk configuration may be different.</span></span> <span data-ttu-id="39c7f-113">Die Platform SDK-Verzeichnisse (in diesem Beispiel mit "D: \\ Mssdk") sind alle zuvor in jeder Pfad Sequenz.</span><span class="sxs-lookup"><span data-stu-id="39c7f-113">The Platform SDK directories (for this example, those with D:\\MSSDK in them) are all earlier in each path sequence.</span></span> <span data-ttu-id="39c7f-114">Diese Sequenz geht davon aus, dass Befehlszeilen Kompilierungen im Eingabe Aufforderungs Fenster ausgeführt werden sollen und dass die. h-Bibliotheksdateien include und. lib im Platform SDK für diese Kompilierungen bevorzugt werden.</span><span class="sxs-lookup"><span data-stu-id="39c7f-114">This sequence assumes that command line compilations are intended to be run in the Command Prompt window and that the .h include and .lib library files in the Platform SDK are preferred for those compilations.</span></span>

<span data-ttu-id="39c7f-115">Die CPU-Umgebungsvariable wird definiert, um die Win32-Builds abhängig von der Plattform zu steuern.</span><span class="sxs-lookup"><span data-stu-id="39c7f-115">The CPU environment variable is defined to control the Win32 builds, depending on the platform.</span></span> <span data-ttu-id="39c7f-116">Zu den aktuell möglichen Werten zählen i386, mips, Alpha und PPC.</span><span class="sxs-lookup"><span data-stu-id="39c7f-116">Current possible values include i386, MIPS, ALPHA, and PPC.</span></span> <span data-ttu-id="39c7f-117">Weitere Informationen finden Sie in der Datei Win32. MAK, die im Platform SDK im \\ Verzeichnis "Mssdk include" bereitgestellt wird \\ .</span><span class="sxs-lookup"><span data-stu-id="39c7f-117">For more information, see the Win32.mak file provided in the Platform SDK in the \\MSSDK\\INCLUDE directory.</span></span> <span data-ttu-id="39c7f-118">Alle Codebeispiele für com-Tutorial enthalten Win32. MAK.</span><span class="sxs-lookup"><span data-stu-id="39c7f-118">All of the COM tutorial code sample makefiles include Win32.mak.</span></span>

 

 




