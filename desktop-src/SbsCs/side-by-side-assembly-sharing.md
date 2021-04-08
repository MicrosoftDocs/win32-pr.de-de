---
description: In der folgenden Abbildung wird veranschaulicht, wie zwei Anwendungen eine Assembly mit der herkömmlichen Methode der assemblyfreigabe gemeinsam verwenden können.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Parallele assemblyfreigabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960551"
---
# <a name="side-by-side-assembly-sharing"></a><span data-ttu-id="22840-103">Parallele assemblyfreigabe</span><span class="sxs-lookup"><span data-stu-id="22840-103">Side-by-side Assembly Sharing</span></span>

<span data-ttu-id="22840-104">In der folgenden Abbildung wird veranschaulicht, wie zwei Anwendungen eine Assembly mit der herkömmlichen Methode der assemblyfreigabe gemeinsam verwenden können.</span><span class="sxs-lookup"><span data-stu-id="22840-104">The following figure illustrates how two applications might share an assembly using the traditional method of assembly sharing.</span></span> <span data-ttu-id="22840-105">Ein Problem mit der herkömmlichen assemblyfreigabe tritt auf, wenn eine Anwendung eine Version einer Assembly installiert – üblicherweise eine DLL –, die nicht abwärts kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="22840-105">A problem with traditional assembly sharing occurs when an application installs a version of an assembly—commonly a DLL—that is not backward compatible.</span></span> <span data-ttu-id="22840-106">Die soeben installierte Anwendung funktioniert, aber Anwendungen, die von der vorherigen dll-Version abhängen, funktionieren möglicherweise nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="22840-106">The application just installed works, but applications that depended on the previous DLL version may no longer work.</span></span>

![Darstellung von zwei Anwendungen, die eine Assembly gemeinsam nutzen](images/sxs1.png)

<span data-ttu-id="22840-108">Mit der isolierten Anwendung und der parallelen Assemblylösung können unterschiedliche Versionen der gleichen Win32-Assembly gleichzeitig auf demselben System ausgeführt werden, ohne dass es zu einem Konflikt kommt.</span><span class="sxs-lookup"><span data-stu-id="22840-108">The isolated application and side-by-side assembly solution enables different versions of the same Win32 assembly to run at the same time on the same system without conflict.</span></span> <span data-ttu-id="22840-109">Durch Angeben der parallelen Assemblyversion, die von der Anwendung verwendet werden soll, können Entwickler sicherstellen, dass die von Ihnen getestete Konfiguration immer auf dem Computer des Benutzers dupliziert wird.</span><span class="sxs-lookup"><span data-stu-id="22840-109">By specifying which side-by-side assembly version the application should use, developers can guarantee that the configuration they test will always be duplicated on the user's computer.</span></span> <span data-ttu-id="22840-110">Die parallele Freigabe wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="22840-110">Side-by-side sharing is illustrated in the following figure.</span></span>

![Implementierung der parallelen assemblyfreigabe](images/sxs2.png)

<span data-ttu-id="22840-112">Weitere Informationen finden Sie unter Informationen [zu isolierten Anwendungen und](about-isolated-applications-and-side-by-side-assemblies.md)parallelen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="22840-112">For more information, see [About Isolated Applications and Side-by-side Assemblies](about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

 

 



