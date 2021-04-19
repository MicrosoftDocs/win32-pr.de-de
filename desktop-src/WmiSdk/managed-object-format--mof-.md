---
description: Managed Object Format (MOF) ist die Sprache, mit der Common Information Model (CIM)-Klassen beschrieben werden.
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: MOF-Datei (Managed Object Format)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360757"
---
# <a name="managed-object-format-mof"></a><span data-ttu-id="df314-103">MOF-Datei (Managed Object Format)</span><span class="sxs-lookup"><span data-stu-id="df314-103">Managed Object Format (MOF)</span></span>

<span data-ttu-id="df314-104">Managed Object Format (MOF) ist die Sprache, mit der [*Common Information Model (CIM)*](gloss-c.md) -Klassen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="df314-104">Managed Object Format (MOF) is the language used to describe [*Common Information Model (CIM)*](gloss-c.md) classes.</span></span>

<span data-ttu-id="df314-105">Die empfohlene Vorgehensweise für WMI-Anbieter, neue WMI-Klassen zu implementieren, ist in MOF-Dateien, die mithilfe von [**Mofcomp.exe**](mofcomp.md) in das [*WMI-Repository*](gloss-w.md)kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="df314-105">The recommended way for WMI providers to implement new WMI classes is in MOF files which are compiled using [**Mofcomp.exe**](mofcomp.md) into the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="df314-106">Es ist auch möglich, CIM-Klassen und-Instanzen mithilfe der [com-API für WMI](com-api-for-wmi.md)zu erstellen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="df314-106">It is also possible to create and manipulate CIM classes and instances using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="df314-107">Ein WMI-Anbieter besteht normalerweise aus einer MOF-Datei, die die Daten-und Ereignis Klassen definiert, für die der Anbieter Daten zurückgibt, sowie eine DLL-Datei, die den Code enthält, der Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="df314-107">A WMI provider normally consists of a MOF file, which defines the data and event classes for which the provider returns data, and a DLL file which contains the code that supplies data.</span></span> <span data-ttu-id="df314-108">Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="df314-108">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="df314-109">WMI-Client Skripts und-Anwendungen können Instanzen von MOF-Anbieter Klassen Abfragen oder Empfangs Ereignis Benachrichtigungen abonnieren.</span><span class="sxs-lookup"><span data-stu-id="df314-109">WMI client scripts and applications can query for instances of provider MOF classes or subscribe to receive event notifications.</span></span>

<span data-ttu-id="df314-110">Mit MOF können Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="df314-110">You can perform the following tasks with MOF:</span></span>

-   [<span data-ttu-id="df314-111">Kompilieren von MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="df314-111">Compiling MOF Files</span></span>](compiling-mof-files.md)
-   [<span data-ttu-id="df314-112">Erstellen einer Klasse</span><span class="sxs-lookup"><span data-stu-id="df314-112">Creating a Class</span></span>](creating-a-class.md)
-   [<span data-ttu-id="df314-113">Erstellen einer Instanz</span><span class="sxs-lookup"><span data-stu-id="df314-113">Creating an Instance</span></span>](creating-an-instance.md)
-   [<span data-ttu-id="df314-114">Erstellen einer Methode</span><span class="sxs-lookup"><span data-stu-id="df314-114">Creating a Method</span></span>](creating-a-method.md)
-   [<span data-ttu-id="df314-115">Fügen eines Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="df314-115">Adding a Qualifier</span></span>](adding-a-qualifier.md)
-   [<span data-ttu-id="df314-116">Erstellen eines Kommentars</span><span class="sxs-lookup"><span data-stu-id="df314-116">Creating a Comment</span></span>](creating-a-comment.md)

## <a name="related-topics"></a><span data-ttu-id="df314-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df314-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df314-118">Informationen zu WMI</span><span class="sxs-lookup"><span data-stu-id="df314-118">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



