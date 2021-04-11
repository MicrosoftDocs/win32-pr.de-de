---
title: Referenz zum Windows-Ereignisprotokoll
description: Im folgenden finden Sie die Programmier Elemente, die Sie zum Erstellen eines Instrumentierungs Manifests, zum Erstellen von Ressourcen aus dem vom Anbieter verwendeten Manifest, zum erhalten von Instrumentations Metadaten zur Laufzeit und zum Abfragen von Ereignissen aus Kanälen und Protokolldateien verwenden.
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041365"
---
# <a name="windows-event-log-reference"></a><span data-ttu-id="8f921-103">Referenz zum Windows-Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="8f921-103">Windows Event Log Reference</span></span>

<span data-ttu-id="8f921-104">Im folgenden sind die Programmier Elemente aufgeführt, die Sie zum Erstellen eines Instrumentierungs Manifests, zum Erstellen von Ressourcen aus dem vom Anbieter verwendeten Manifest, zum erhalten von Instrumentations Metadaten zur Laufzeit und zum Abfragen von Ereignissen aus Kanälen und Protokolldateien verwenden:</span><span class="sxs-lookup"><span data-stu-id="8f921-104">The following are the programming elements that you use to create an instrumentation manifest, create resources from the manifest that your provider uses, get instrumentation metadata at run time, and query events from channels and log files:</span></span>

-   [<span data-ttu-id="8f921-105">Event Manifest-Schema</span><span class="sxs-lookup"><span data-stu-id="8f921-105">EventManifest Schema</span></span>](eventmanifestschema-schema.md)
-   [<span data-ttu-id="8f921-106">Ereignis Schema</span><span class="sxs-lookup"><span data-stu-id="8f921-106">Event Schema</span></span>](eventschema-schema.md)
-   [<span data-ttu-id="8f921-107">Abfrage Schema</span><span class="sxs-lookup"><span data-stu-id="8f921-107">Query Schema</span></span>](queryschema-schema.md)
-   [<span data-ttu-id="8f921-108">Windows-Ereignisprotokoll Konstanten</span><span class="sxs-lookup"><span data-stu-id="8f921-108">Windows Event Log Constants</span></span>](windows-event-log-constants.md)
-   [<span data-ttu-id="8f921-109">Windows-Ereignisprotokoll Datentypen</span><span class="sxs-lookup"><span data-stu-id="8f921-109">Windows Event Log Data Types</span></span>](windows-event-log-data-types.md)
-   [<span data-ttu-id="8f921-110">Windows-Ereignisprotokoll-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8f921-110">Windows Event Log Enumerations</span></span>](windows-event-log-enumerations.md)
-   [<span data-ttu-id="8f921-111">Windows-Ereignisprotokoll Funktionen</span><span class="sxs-lookup"><span data-stu-id="8f921-111">Windows Event Log Functions</span></span>](windows-event-log-functions.md)
-   [<span data-ttu-id="8f921-112">Windows-Ereignisprotokoll Strukturen</span><span class="sxs-lookup"><span data-stu-id="8f921-112">Windows Event Log Structures</span></span>](windows-event-log-structures.md)
-   [<span data-ttu-id="8f921-113">Windows-Ereignisprotokoll Tools</span><span class="sxs-lookup"><span data-stu-id="8f921-113">Windows Event Log Tools</span></span>](windows-event-log-tools.md)

<span data-ttu-id="8f921-114">Informationen zu Anwendungen, die mit einer .NET-Sprache geschrieben werden, z. b. c# oder Visual Basic, finden Sie in den folgenden Namespaces</span><span class="sxs-lookup"><span data-stu-id="8f921-114">For applications written using a .NET language, such as C# or Visual Basic, see the following namespaces:</span></span>

-   <span data-ttu-id="8f921-115">Um Ereignisse zu schreiben, verwenden Sie die Klassen und Methoden, die im [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) -Namespace definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8f921-115">To write events, use the classes and methods defined in the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace.</span></span>
-   <span data-ttu-id="8f921-116">Verwenden Sie die Klassen und Methoden, die im [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace definiert sind, um Ereignisse aus einem Windows-Ereignisprotokoll Kanal oder-Protokoll zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8f921-116">To consume events from a Windows Event Log channel or log, use the classes and methods defined in the [System.Diagnostics.Eventing.Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.</span></span>

<span data-ttu-id="8f921-117">Als Alternative zur Verwendung des [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) -Namespace zum Schreiben von Ereignissen können Sie das **-CS-** oder **-CSS** -Argument verwenden, damit der Nachrichten Compiler den Code zum Schreiben der Ereignisse generiert.</span><span class="sxs-lookup"><span data-stu-id="8f921-117">As an alternative to using the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace to write events, you can use the **-cs** or **-css** argument to have the message compiler generate the code to write the events.</span></span> <span data-ttu-id="8f921-118">Weitere Informationen finden Sie unter [**Message Compiler**](message-compiler--mc-exe-.md).</span><span class="sxs-lookup"><span data-stu-id="8f921-118">For details, see [**Message Compiler**](message-compiler--mc-exe-.md).</span></span>
