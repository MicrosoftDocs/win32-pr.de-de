---
description: Msitool. MAK ist ein Makefile, das Sie zum Erstellen von Tools und benutzerdefinierten Aktionen verwenden können.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Msitool. MAK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131308"
---
# <a name="msitoolmak"></a><span data-ttu-id="26fa2-103">Msitool. MAK</span><span class="sxs-lookup"><span data-stu-id="26fa2-103">Msitool.mak</span></span>

<span data-ttu-id="26fa2-104">Msitool. MAK ist ein Makefile, das Sie zum Erstellen von Tools und benutzerdefinierten Aktionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="26fa2-104">Msitool.mak is a makefile that you can use to build tools and custom actions.</span></span> <span data-ttu-id="26fa2-105">Sie kann mit Visual C++ Version 4,0 oder höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26fa2-105">It may be used with Visual C++ version 4.0 or later.</span></span> <span data-ttu-id="26fa2-106">Weitere Informationen finden Sie in der Header Datei.</span><span class="sxs-lookup"><span data-stu-id="26fa2-106">For more information, see the header file.</span></span> <span data-ttu-id="26fa2-107">Vor dem einschließen dieser Datei muss ein Satz von Werten definiert werden.</span><span class="sxs-lookup"><span data-stu-id="26fa2-107">It requires a set of values to be defined before including this file.</span></span> <span data-ttu-id="26fa2-108">In der Regel platzieren Entwickler diese am Anfang der CPP-Datei, die durch den C-Compiler übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="26fa2-108">Typically developers put those at the start of the .cpp, ifdef'd to be skipped by the C compiler.</span></span> <span data-ttu-id="26fa2-109">Ebenso werden Ressourcen am Ende der CPP-Datei hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="26fa2-109">Likewise resources are added to the end of the .cpp file.</span></span> <span data-ttu-id="26fa2-110">Weitere Informationen finden Sie in den Beispielen.</span><span class="sxs-lookup"><span data-stu-id="26fa2-110">See samples for details.</span></span>

<span data-ttu-id="26fa2-111">Vcbin kann für das Verzeichnis definiert werden, in dem die Visual C++ Tools gefunden werden, oder das Makefile verwendet msvcdir und msdevdir.</span><span class="sxs-lookup"><span data-stu-id="26fa2-111">VCBIN can be defined to the directory where the Visual C++ tools are found or the makefile uses MSVCDIR and MSDEVDIR.</span></span> <span data-ttu-id="26fa2-112">Wenn diese nicht definiert sind, wird kein Speicherort angegeben, es wird davon ausgegangen, dass sich die Tools auf dem Pfad befinden.</span><span class="sxs-lookup"><span data-stu-id="26fa2-112">If those are not defined, it does not specify a location, assuming the tools to be on the PATH.</span></span> <span data-ttu-id="26fa2-113">Ein Problem mit den Umgebungsvariablen in Visual C++ Version 5,0 besteht darin, dass der Linker keine Msdis100.dll finden kann, wenn sich beide nicht auf Ihrem Pfad befinden.</span><span class="sxs-lookup"><span data-stu-id="26fa2-113">An issue with the environment variables in Visual C++ version 5.0 is that if both are not on you path, the linker cannot find Msdis100.dll.</span></span> <span data-ttu-id="26fa2-114">Wenn Sie diese aus msdevdir in msvcdir kopieren, funktioniert Sie.</span><span class="sxs-lookup"><span data-stu-id="26fa2-114">If you copy that from MSDEVDIR to MSVCDIR, it works.</span></span> <span data-ttu-id="26fa2-115">Die andere Möglichkeit besteht darin, Msdis100.dll und Rc.exe und Rcdll.dll in msvcdir zu kopieren und vcbin auf diese festzulegen.</span><span class="sxs-lookup"><span data-stu-id="26fa2-115">The other option is to copy Msdis100.dll and Rc.exe and Rcdll.dll to MSVCDIR, and set VCBIN to that.</span></span>

<span data-ttu-id="26fa2-116">Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26fa2-116">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26fa2-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26fa2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26fa2-118">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="26fa2-118">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="26fa2-119">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="26fa2-119">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



