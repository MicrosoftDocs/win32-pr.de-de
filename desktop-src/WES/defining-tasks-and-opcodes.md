---
title: Definieren von Aufgaben und Opcodes
description: Anbieter verwenden Tasks und Opcodes, um Ereignisse logisch zu gruppieren. Das Gruppieren von Ereignissen hilft Consumern dabei, nur die Ereignisse abzufragen, die bestimmte Aufgaben- und Opcodekombinationen enthalten.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb576251edf4de14c564c6e468209ece93e5840da9e0d821c20b132794f48ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032470"
---
# <a name="defining-tasks-and-opcodes"></a>Definieren von Aufgaben und Opcodes

Anbieter verwenden Tasks und Opcodes, um Ereignisse logisch zu gruppieren. Das Gruppieren von Ereignissen hilft Consumern dabei, nur die Ereignisse abzufragen, die bestimmte Aufgaben- und Opcodekombinationen enthalten. In der Regel verwenden Sie Aufgaben, um eine Hauptkomponente des Anbieters zu identifizieren, z. B. die Netzwerk- oder Datenbankkomponente. Anschließend können Sie Opcodes verwenden, um die Vorgänge zu identifizieren, die von der Komponente ausgeführt werden, z. B. die Sende- und Empfangsvorgänge für eine Netzwerkkomponente. Wenn Sie nur über eine Komponente verfügen, können Sie task verwenden, um einen größeren Vorgang in der Komponente widerzuspiegeln, z. B. verbinden oder trennen, und opcode verwenden, um eine Aktivität innerhalb des Vorgangs widerzuspiegeln, z. B. das Lesen der Registrierung. Sie können opcode auch verwenden, ohne eine Aufgabe anzugeben. Wie Sie Aufgaben und Opcodes zum Gruppieren von Ereignissen für den Consumer verwenden, liegt vollständig bei Ihnen.

Verwenden Sie das **Taskelement,** um eine Aufgabe zu definieren. Um einen Opcode zu definieren, verwenden Sie das **Opcode-Element.** Sie können bis zu 228 Opcodes angeben. Der **Taskwert** muss größer als 0 sein. Die Opcodes müssen zwischen 11 und 239 liegen. Die Winmeta.xml-Datei definiert allgemeine Vorgänge, die Sie verwenden können, anstatt Eigene zu definieren.

Im folgenden Beispiel wird gezeigt, wie mehrere Aufgaben und Opcodes definiert werden.

```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <tasks>
                    <task name="Disconnect" 
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>
 
                    <task name="Connect" 
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)">
                    </task>

                    <task name="Validate" 
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)">
                    </task>
                </tasks>

                <opcodes>
                    <opcode name="Initialize" 
                            symbol="OPCODE_INITIALIZE" 
                            value="12"
                            message="$(string.Opcode.Initialize)"/>

                    <opcode name="Cleanup" 
                            symbol="OPCODE_CLEANUP" 
                            value="13"
                            message="$(string.Opcode.Cleanup)"/>
                 </opcodes>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
