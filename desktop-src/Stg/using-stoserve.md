---
title: Verwenden von stoservice
description: Stoservice ist eine DLL, die in erster Linie als com-Server vorgesehen ist.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342144"
---
# <a name="using-stoserve"></a><span data-ttu-id="b328e-103">Verwenden von stoservice</span><span class="sxs-lookup"><span data-stu-id="b328e-103">Using StoServe</span></span>

<span data-ttu-id="b328e-104">**Stoservice** ist eine DLL, die in erster Linie als com-Server vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="b328e-104">**StoServe** is a DLL that is intended primarily as a COM server.</span></span> <span data-ttu-id="b328e-105">Obwohl Sie durch Verknüpfen mit dem zugeordneten implizit geladen werden kann. LIB-Datei wird normalerweise nach einem expliziten LoadLibrary-Befehl verwendet, normalerweise aus der com-Funktion [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span><span class="sxs-lookup"><span data-stu-id="b328e-105">Although it can be implicitly loaded by linking to its associated .LIB file, it is normally used after an explicit LoadLibrary call, usually from within the COM function [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span></span> <span data-ttu-id="b328e-106">Bei **stoservice** handelt es sich um einen selbst registrierenden Prozess internen Server.</span><span class="sxs-lookup"><span data-stu-id="b328e-106">**StoServe** is a self-registering in-process server.</span></span>

<span data-ttu-id="b328e-107">Zur Verwendung von **stoservice** muss ein Client Programm stoservice nicht einschließen. H oder Link zum stoservice. LIB.</span><span class="sxs-lookup"><span data-stu-id="b328e-107">To use **StoServe**, a client program does not need to include STOSERVE.H or link to STOSERVE.LIB.</span></span> <span data-ttu-id="b328e-108">Ein com-Client von **stoservice** erhält ausschließlich den Zugriff über die CLSID und die com-Dienste seines Objekts.</span><span class="sxs-lookup"><span data-stu-id="b328e-108">A COM client of **StoServe** obtains access solely through its object's CLSID and COM services.</span></span> <span data-ttu-id="b328e-109">Für **stoservice** ist diese CLSID CLSID \_ dllpaper (in der Datei "papguids" definiert. H im \\ Verzeichnis "Inc.".</span><span class="sxs-lookup"><span data-stu-id="b328e-109">For **StoServe**, that CLSID is CLSID\_DllPaper (defined in file PAPGUIDS.H in the \\INC sibling directory).</span></span> <span data-ttu-id="b328e-110">Das [stoclien](structured-storage-client-sample--stoclien-.md) -Codebeispiel zeigt, wie der Client diesen Zugriff erhält.</span><span class="sxs-lookup"><span data-stu-id="b328e-110">The [StoClien](structured-storage-client-sample--stoclien-.md) code sample shows how the client obtains this access.</span></span>

<span data-ttu-id="b328e-111">Das Makefile, das dieses Beispiel erstellt, registriert den Server automatisch in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="b328e-111">The makefile that builds this sample automatically registers the server in the registry.</span></span> <span data-ttu-id="b328e-112">Sie können die Selbstregistrierung manuell initiieren, indem Sie den folgenden Befehl an der Eingabeaufforderung im **stoservice** -Verzeichnis ausgeben:</span><span class="sxs-lookup"><span data-stu-id="b328e-112">You can manually initiate its self-registration by issuing the following command at the command prompt in the **StoServe** directory:</span></span>

<span data-ttu-id="b328e-113">**NMAKE** - **Register**</span><span class="sxs-lookup"><span data-stu-id="b328e-113">**nmake** **register**</span></span>

<span data-ttu-id="b328e-114">Dabei wird davon ausgegangen, dass Sie eine Kompilierungs Umgebung eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="b328e-114">This assumes that you have a compilation environment set up.</span></span> <span data-ttu-id="b328e-115">Andernfalls können Sie den REGISTER.EXE-Befehl auch direkt an der Eingabeaufforderung aufrufen, während Sie sich im **stoservice** -Verzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="b328e-115">If not, you can also directly invoke the REGISTER.EXE command at the command prompt while in the **StoServe** directory.</span></span>

<span data-ttu-id="b328e-116">**..\\ \\register.exeregistrieren** **stoserve.dll**</span><span class="sxs-lookup"><span data-stu-id="b328e-116">**..\\register\\register.exe** **stoserve.dll**</span></span>

<span data-ttu-id="b328e-117">Diese Registrierungs Befehle erfordern einen vorherigen Build des Register Beispiels in dieser Reihe sowie einen früheren Build STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="b328e-117">These registration commands require a prior build of the REGISTER sample in this series, as well as a prior build of STOSERVE.DLL.</span></span>

<span data-ttu-id="b328e-118">In dieser Reihe verwenden Makefiles das REGISTER.EXE-Hilfsprogramm aus dem Register Sample.</span><span class="sxs-lookup"><span data-stu-id="b328e-118">In this series, the makefiles use the REGISTER.EXE utility from the REGISTER sample.</span></span> <span data-ttu-id="b328e-119">Aktuelle Versionen des Platform Software Development Kit (SDK) und Visual C++ enthalten ein Dienstprogramm, REGSVR32.EXE, das auf ähnliche Weise zum Registrieren von in-Process-Servern und Marshalling von DLLs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b328e-119">Recent releases of the Platform Software Development Kit (SDK) and Visual C++ include a utility, REGSVR32.EXE, which can be used in a similar fashion to register in-process servers and marshaling DLLs.</span></span>

<span data-ttu-id="b328e-120">**Stoservice** verwendet viele der Hilfsprogrammklassen und Dienste, die von apputil bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b328e-120">**StoServe** uses many of the utility classes and services provided by APPUTIL.</span></span> <span data-ttu-id="b328e-121">Weitere Informationen zu apputil erhalten Sie, wenn Sie den Quellcode der apputil-Bibliothek im gleich geordneten apputil-Verzeichnis untersuchen und im Hauptverzeichnis des Tutorials APPUTIL.HTM.</span><span class="sxs-lookup"><span data-stu-id="b328e-121">For more details on APPUTIL, study the APPUTIL library's source code in the sibling APPUTIL directory and APPUTIL.HTM in the main tutorial directory.</span></span>

 

 