---
title: Verwenden des System-Supplied Ersatz Zeichens
description: Verwenden des System-Supplied Ersatz Zeichens
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311388"
---
# <a name="using-the-system-supplied-surrogate"></a><span data-ttu-id="363e8-103">Verwenden des System-Supplied Ersatz Zeichens</span><span class="sxs-lookup"><span data-stu-id="363e8-103">Using the System-Supplied Surrogate</span></span>

<span data-ttu-id="363e8-104">Wenn Sie das vom System bereitgestellte Ersatz Zeichen für den DLL-Server verwenden möchten, registrieren Sie die dll, indem Sie eine leere Zeichenfolge oder **null** für den Wert [dllersatz](dllsurrogate.md) in der Registrierung angeben.</span><span class="sxs-lookup"><span data-stu-id="363e8-104">To use the system-supplied surrogate for your DLL server, register the DLL specifying an empty string or **NULL** for the [DllSurrogate](dllsurrogate.md) value in the registry.</span></span> <span data-ttu-id="363e8-105">Wenn eine Aktivierungs Anforderung für einen dll-Server, der so festgelegt ist, auf com festgelegt wird, startet com den standardmäßigen Ersatzprozess und die angeforderte DLL (indem er die CLSID intern in der Befehlszeile für den Start angibt), um einen separaten Aufruf zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="363e8-105">When an activation request for a DLL server so designated comes to COM, COM launches the default surrogate process and the requested DLL (by specifying the CLSID on the launch command line internally) at the same time to avoid a separate call.</span></span> <span data-ttu-id="363e8-106">(Informationen zum Ausführen von mehr als einem DLL-Server in einem Ersatzprozess finden Sie unter [Ersatz für Ersatz](surrogate-sharing.md)Zeichen.)</span><span class="sxs-lookup"><span data-stu-id="363e8-106">(For information on running more than one DLL server in a surrogate process, see [Surrogate Sharing](surrogate-sharing.md).)</span></span>

<span data-ttu-id="363e8-107">Die Standard Implementierung des Ersatz Prozesses ist ein Pseudo-com-Server mit gemischtem Threading Modell Stil.</span><span class="sxs-lookup"><span data-stu-id="363e8-107">The default implementation of the surrogate process is a mixed-threading model style pseudo-COM server.</span></span> <span data-ttu-id="363e8-108">Wenn mehrere dll-Server in einen einzelnen Ersatzprozess geladen werden, wird durch diesen Vorgang sichergestellt, dass jeder dll-Server mit dem Threading Modell instanziiert wird, das in der Registrierung für diesen Server angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="363e8-108">When multiple DLL servers are loaded into a single surrogate process, this process ensures that each DLL server is instantiated using the threading model specified in the registry for that server.</span></span> <span data-ttu-id="363e8-109">Alle geladenen frei Thread Server werden im Multithread-Apartment vereint, während sich jeder Apartment Thread Server in einem Single Thread-Apartment befindet.</span><span class="sxs-lookup"><span data-stu-id="363e8-109">All loaded free-threaded servers will live together in the multithreaded apartment, while each apartment-threaded server will reside in a single-threaded apartment.</span></span> <span data-ttu-id="363e8-110">Wenn ein dll-Server beide Threading Modelle unterstützt, wählt com das Multithreading.</span><span class="sxs-lookup"><span data-stu-id="363e8-110">If a DLL server supports both threading models, COM will choose multithreading.</span></span>

<span data-ttu-id="363e8-111">Dieser Ersatzprozess wird so geschrieben, dass com sowohl das Entladen der DLL-Server als auch das Beenden des Ersatz Vorgangs verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="363e8-111">This surrogate process is written so that COM handles both the unloading of DLL servers and the terminating of the surrogate process.</span></span>

<span data-ttu-id="363e8-112">Das vom System bereitgestellte Ersatz Zeichen funktioniert sehr gut für die meisten Entwickler und ist sehr einfach zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="363e8-112">The system-provided surrogate will work very well for most developers, as well as being very easy to use.</span></span> <span data-ttu-id="363e8-113">Allerdings können Entwickler mit besonderen Überlegungen festlegen, dass ein benutzerdefiniertes Ersatz Zeichen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="363e8-113">However, those developers with special considerations may decide that a custom surrogate is necessary.</span></span> <span data-ttu-id="363e8-114">Weitere Informationen finden Sie unter [Schreiben eines benutzerdefinierten Ersatz](writing-a-custom-surrogate.md)Zeichens.</span><span class="sxs-lookup"><span data-stu-id="363e8-114">For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="363e8-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="363e8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="363e8-116">DLL-Surrogates</span><span class="sxs-lookup"><span data-stu-id="363e8-116">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




