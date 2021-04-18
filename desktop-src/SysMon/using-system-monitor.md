---
title: Verwenden des System Monitors
description: Der System Monitor (Sysmon) kann in jeder Anwendung enthalten sein, die ActiveX \ 174 unterstützt. Steuerelemente. Beispielsweise können Sie sysmon in eine Microsoft Visual Basic-Anwendung oder in ein HTML-Dokument einschließen.
ms.assetid: 36931aae-b608-42d9-a3e3-09784e80f386
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd636c8b984f7c891c2222b4674dd8d0d7e747d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338595"
---
# <a name="using-system-monitor"></a><span data-ttu-id="2b5b3-104">Verwenden des System Monitors</span><span class="sxs-lookup"><span data-stu-id="2b5b3-104">Using System Monitor</span></span>

<span data-ttu-id="2b5b3-105">Der System Monitor (Sysmon) kann in jeder Anwendung enthalten sein, die ActiveX-® Steuerelemente unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b5b3-105">System Monitor (SYSMON) can be included in any application that supports ActiveX® controls.</span></span> <span data-ttu-id="2b5b3-106">Beispielsweise können Sie sysmon in eine Microsoft Visual Basic-Anwendung oder in ein HTML-Dokument einschließen.</span><span class="sxs-lookup"><span data-stu-id="2b5b3-106">For example, you can include SYSMON in a Microsoft Visual Basic application or in an HTML document.</span></span>

<span data-ttu-id="2b5b3-107">Im folgenden Beispiel wird gezeigt, wie Sie sysmon in ein HTML-Dokument einschließen.</span><span class="sxs-lookup"><span data-stu-id="2b5b3-107">The following example shows how to include SYSMON in an HTML document.</span></span> <span data-ttu-id="2b5b3-108">Im Beispiel wird VBScript zum Hinzufügen von Indikatoren verwendet, deren Werte vom lokalen Computer abgerufen werden. einige der sysmon-Eigenschaften, die die Anzeige des Monitors steuern, werden geändert, und das oncounteradd-Ereignis wird verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2b5b3-108">The example uses VBScript to add counters whose values are retrieved from the local computer, modifies some of the SYSMON properties that control how the monitor is displayed, and processes the OnCounterAdd event.</span></span> <span data-ttu-id="2b5b3-109">Im Beispiel wird das Platzhalter Zeichen ( \* ) verwendet, um alle Instanzen des Prozess Zählers hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2b5b3-109">The example uses the wildcard character (\*) to add all instances of the process counter.</span></span>

``` syntax
<HTML>
<BODY BGCOLOR=#C0C0C0>

<SCRIPT LANGUAGE="VBScript">
  Sub Monitor_OnCounterAdded(index)
    Monitor.Counters.Item(1).Width = 8
  End Sub
</Script>
<OBJECT
  CLASSID="clsid:C4D2D8E0-D1DD-11CE-940F-008029004347"
  ID="Monitor"
  HEIGHT=80%
  WIDTH=100%>
</OBJECT>

<SCRIPT LANGUAGE="VBScript">
  Sub Window_OnLoad
    On Error Resume Next
    Monitor.ShowValueBar = False
    Monitor.ShowHorizontalGrid = True
    Monitor.Counters.Add("\Process(*)\% Processor Time")
    Monitor.DisplayType=sysmonLineGraph
    Monitor.GraphTitle="System Performance Overview"
  End Sub
</SCRIPT>

</BODY>
</HTML>
```

 

 




