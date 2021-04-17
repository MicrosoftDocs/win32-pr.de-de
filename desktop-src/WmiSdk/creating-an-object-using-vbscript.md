---
description: Sie können ein Objekt für WMI in Visual Basic Scripting Edition (VBScript) erstellen, indem Sie eine Verbindung mit WMI herstellen und dann CreateObject aufrufen. In der folgenden Tabelle sind die Methoden in der Skript-API für WMI aufgelistet, die die Objekt Erstellung unterstützen.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Erstellen eines Objekts mithilfe von VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485355"
---
# <a name="creating-an-object-using-vbscript"></a><span data-ttu-id="c1745-104">Erstellen eines Objekts mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="c1745-104">Creating an Object Using VBScript</span></span>

<span data-ttu-id="c1745-105">Sie können ein Objekt für WMI in Visual Basic Scripting Edition (VBScript) erstellen, indem Sie eine Verbindung mit WMI herstellen und dann [CreateObject](/previous-versions//xzysf6hc(v=vs.85))aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c1745-105">You can create an object for WMI in Visual Basic Scripting Edition (VBScript) by connecting to WMI and then calling [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span> <span data-ttu-id="c1745-106">In der folgenden Tabelle sind die Methoden in der Skript-API für WMI aufgelistet, die die Objekt Erstellung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c1745-106">The following table lists the methods in the Scripting API for WMI that support object creation.</span></span>



| <span data-ttu-id="c1745-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c1745-107">Interface</span></span>                                        | <span data-ttu-id="c1745-108">ProgID</span><span class="sxs-lookup"><span data-stu-id="c1745-108">ProgID</span></span>                             |
|--------------------------------------------------|------------------------------------|
| [<span data-ttu-id="c1745-109">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1745-109">**SWbemDateTime**</span></span>](swbemdatetime.md)           | <span data-ttu-id="c1745-110">"WbemScripting. Swap Time"</span><span class="sxs-lookup"><span data-stu-id="c1745-110">"WbemScripting.SwbemDateTime"</span></span>      |
| [<span data-ttu-id="c1745-111">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="c1745-111">**SWbemLocator**</span></span>](swbemlocator.md)             | <span data-ttu-id="c1745-112">"WbemScripting. Swap-Locator"</span><span class="sxs-lookup"><span data-stu-id="c1745-112">"WbemScripting.SWbemLocator"</span></span>       |
| [<span data-ttu-id="c1745-113">**Austausch Fehler**</span><span class="sxs-lookup"><span data-stu-id="c1745-113">**SWbemLastError**</span></span>](swbemlasterror.md)         | <span data-ttu-id="c1745-114">"WbemScripting. taubem. LastError"</span><span class="sxs-lookup"><span data-stu-id="c1745-114">"WbemScripting.SWbem.LastError"</span></span>    |
| [<span data-ttu-id="c1745-115">**Errbemubjectpath**</span><span class="sxs-lookup"><span data-stu-id="c1745-115">**SWbemObjectPath**</span></span>](swbemobjectpath.md)       | <span data-ttu-id="c1745-116">"WbemScripting. errbewbjectpath"</span><span class="sxs-lookup"><span data-stu-id="c1745-116">"WbemScripting.SWbemObjectPath"</span></span>    |
| [<span data-ttu-id="c1745-117">**Austausch Elementname**</span><span class="sxs-lookup"><span data-stu-id="c1745-117">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md) | <span data-ttu-id="c1745-118">"WbemScripting. Swap Name Name"</span><span class="sxs-lookup"><span data-stu-id="c1745-118">"WbemScripting.SWbemNamedValueSet"</span></span> |
| [<span data-ttu-id="c1745-119">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="c1745-119">**SWbemRefresher**</span></span>](swbemrefresher.md)         | <span data-ttu-id="c1745-120">"WbemScripting. Swap-Aktualisierungs Programm"</span><span class="sxs-lookup"><span data-stu-id="c1745-120">"WbemScripting.SWbemRefresher"</span></span>     |
| [<span data-ttu-id="c1745-121">**Swap-Senke**</span><span class="sxs-lookup"><span data-stu-id="c1745-121">**SWbemSink**</span></span>](swbemsink.md)                   | <span data-ttu-id="c1745-122">"WbemScripting. taubemsink"</span><span class="sxs-lookup"><span data-stu-id="c1745-122">"WbemScripting.SWbemSink"</span></span>          |



 

<span data-ttu-id="c1745-123">Im folgenden Verfahren wird beschrieben, wie ein WMI-Objekt mit VBScript erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c1745-123">The following procedure describes how to create a WMI object using VBScript.</span></span>

<span data-ttu-id="c1745-124">**So erstellen Sie ein WMI-Objekt mithilfe von VBScript**</span><span class="sxs-lookup"><span data-stu-id="c1745-124">**To create a WMI object using VBScript**</span></span>

1.  <span data-ttu-id="c1745-125">Stellen Sie eine Verbindung mit WMI her, indem Sie entweder einen Moniker oder ein [**Swap**](swbemlocator.md) -Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1745-125">Connect to WMI using either a moniker or an [**SWbemLocator**](swbemlocator.md) object.</span></span>

    <span data-ttu-id="c1745-126">Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c1745-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

2.  <span data-ttu-id="c1745-127">Aufrufen der VBScript-Methode "| [ateobject](/previous-versions//xzysf6hc(v=vs.85)) ".</span><span class="sxs-lookup"><span data-stu-id="c1745-127">Make a call to the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method.</span></span>

    <span data-ttu-id="c1745-128">Im folgenden Codebeispiel wird gezeigt, wie ein-Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c1745-128">The following code example shows how to create an object.</span></span>

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    <span data-ttu-id="c1745-129">Wenn Sie in Schritt 1 einen Moniker verwenden, müssen Sie " [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) " nicht erneut aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c1745-129">If you use a moniker in Step 1, you do not need to call [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) again.</span></span>

 

 
