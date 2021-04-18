---
title: DLL-Surrogates
description: DLL-Surrogates
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337186"
---
# <a name="dll-surrogates"></a><span data-ttu-id="6567a-103">DLL-Surrogates</span><span class="sxs-lookup"><span data-stu-id="6567a-103">DLL Surrogates</span></span>

<span data-ttu-id="6567a-104">COM ermöglicht das Erstellen von DLL-Servern, die in einen Ersatz-exe-Prozess geladen werden können.</span><span class="sxs-lookup"><span data-stu-id="6567a-104">COM makes it possible to create DLL servers that can be loaded into a surrogate EXE process.</span></span> <span data-ttu-id="6567a-105">Dadurch wird die einfache Erstellung von DLL-Servern mit den Vorteilen der Implementierung der ausführbaren Datei kombiniert.</span><span class="sxs-lookup"><span data-stu-id="6567a-105">This combines the ease of writing DLL servers with the benefits of executable implementation.</span></span> <span data-ttu-id="6567a-106">Entwicklungs Tools wie Microsoft Visual Studio vereinfachen das Schreiben von DLL-Servern, aber ein dll-Server in sich weist Grenzen auf.</span><span class="sxs-lookup"><span data-stu-id="6567a-106">Development tools like Microsoft Visual Studio facilitate the writing of DLL servers, but a DLL server in itself has limits.</span></span> <span data-ttu-id="6567a-107">Das Ausführen des dll-Servers in einem Ersatzprozess bietet verschiedene Vorteile:</span><span class="sxs-lookup"><span data-stu-id="6567a-107">Running the DLL server in a surrogate process offers several possible benefits:</span></span>

-   <span data-ttu-id="6567a-108">Fehler Isolation und die Möglichkeit, mehrere Clients gleichzeitig zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="6567a-108">Fault isolation and the ability to service multiple clients simultaneously.</span></span>
-   <span data-ttu-id="6567a-109">In einer verteilten Umgebung könnte eine DLL-Server Implementierung zum Dienst von Remote Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6567a-109">In a distributed environment, a DLL server implementation could be used to service remote clients.</span></span>
-   <span data-ttu-id="6567a-110">Sie können es Clients ermöglichen, sich selbst vor nicht vertrauenswürdigem Servercode zu schützen, während Sie Ihnen den Zugriff auf die vom dll-Server bereitgestellten Dienste erlauben.</span><span class="sxs-lookup"><span data-stu-id="6567a-110">It could permit clients to help protect themselves from untrusted server code while allowing them access to the services the DLL server provides.</span></span>
-   <span data-ttu-id="6567a-111">Durch das Ausführen eines dll-Servers in einem Ersatz Zeichen erhält die dll die Sicherheit des Ersatz Diensts.</span><span class="sxs-lookup"><span data-stu-id="6567a-111">Running a DLL server in a surrogate provides the DLL with the surrogate's security.</span></span>

<span data-ttu-id="6567a-112">COM stellt einen standardmäßigen Ersatzprozess bereit, oder Sie können ein benutzerdefiniertes Ersatz Zeichen schreiben, wenn Sie besondere Anforderungen haben.</span><span class="sxs-lookup"><span data-stu-id="6567a-112">COM provides a default surrogate process, or you can write a custom surrogate if you have special needs.</span></span>

<span data-ttu-id="6567a-113">Die folgenden Themen enthalten weitere Informationen zu dll-Surrogates:</span><span class="sxs-lookup"><span data-stu-id="6567a-113">The following topics provide more information on DLL surrogates:</span></span>

-   [<span data-ttu-id="6567a-114">DLL-Server Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6567a-114">DLL Server Requirements</span></span>](dll-server-requirements.md)
-   [<span data-ttu-id="6567a-115">Verwenden des System-Supplied Ersatz Zeichens</span><span class="sxs-lookup"><span data-stu-id="6567a-115">Using the System-Supplied Surrogate</span></span>](using-the-system-supplied-surrogate.md)
-   [<span data-ttu-id="6567a-116">Schreiben eines benutzerdefinierten Ersatz Zeichens</span><span class="sxs-lookup"><span data-stu-id="6567a-116">Writing a Custom Surrogate</span></span>](writing-a-custom-surrogate.md)

 

 




