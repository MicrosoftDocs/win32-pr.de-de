---
title: Definieren von Aufgaben und OpCodes
description: Anbieter verwenden Aufgaben und Opcodes, um Ereignisse logisch zu gruppieren. Beim Gruppieren von Ereignissen können Consumer nur Ereignisse Abfragen, die bestimmte Kombinationen aus Aufgabe und OpCode enthalten.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257166a34c167d076fec39ac6997d12dc785450
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104516689"
---
# <a name="defining-tasks-and-opcodes"></a>Definieren von Aufgaben und OpCodes

Anbieter verwenden Aufgaben und Opcodes, um Ereignisse logisch zu gruppieren. Beim Gruppieren von Ereignissen können Consumer nur Ereignisse Abfragen, die bestimmte Kombinationen aus Aufgabe und OpCode enthalten. In der Regel verwenden Sie Aufgaben, um eine Hauptkomponente des Anbieters zu identifizieren, z. b. die Netzwerk-oder Datenbankkomponente. Sie können dann Opcodes verwenden, um die Vorgänge zu identifizieren, die von der Komponente durchführt werden, z. b. die Sende-und Empfangs Vorgänge für eine Netzwerkkomponente. Wenn Sie nur über eine Komponente verfügen, können Sie mithilfe der Aufgabe einen größeren Vorgang in der Komponente, z. b. verbinden oder trennen, widerspiegeln und Opcode verwenden, um eine Aktivität innerhalb des Vorgangs, z. b. das Lesen der Registrierung, widerzuspiegeln. Sie können Opcode auch ohne Angabe einer Aufgabe verwenden. Wie Sie Aufgaben und Opcodes verwenden, um Ereignisse für den Consumer zu gruppieren, ist vollständig auf dem neuesten Stand.

Verwenden Sie das **Task** -Element, um eine Aufgabe zu definieren. Um einen Opcode zu definieren, verwenden Sie das **Opcode** -Element. Sie können bis zu 228 Opcodes angeben. Der Aufgaben **Wert** muss größer als 0 sein. Die OpCodes müssen zwischen 11 und 239 liegen. Die Winmeta.xml Datei definiert allgemeine Vorgänge, die Sie verwenden können, anstatt ihre eigenen zu definieren.

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
