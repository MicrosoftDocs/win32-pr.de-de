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
# <a name="using-system-monitor"></a>Verwenden des System Monitors

Der System Monitor (Sysmon) kann in jeder Anwendung enthalten sein, die ActiveX-® Steuerelemente unterstützt. Beispielsweise können Sie sysmon in eine Microsoft Visual Basic-Anwendung oder in ein HTML-Dokument einschließen.

Im folgenden Beispiel wird gezeigt, wie Sie sysmon in ein HTML-Dokument einschließen. Im Beispiel wird VBScript zum Hinzufügen von Indikatoren verwendet, deren Werte vom lokalen Computer abgerufen werden. einige der sysmon-Eigenschaften, die die Anzeige des Monitors steuern, werden geändert, und das oncounteradd-Ereignis wird verarbeitet. Im Beispiel wird das Platzhalter Zeichen ( \* ) verwendet, um alle Instanzen des Prozess Zählers hinzuzufügen.

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

 

 




