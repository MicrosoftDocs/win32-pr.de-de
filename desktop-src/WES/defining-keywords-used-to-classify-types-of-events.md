---
title: Definieren von Schlüsselwörtern zum Klassifizieren von Ereignis Typen
description: Anbieter verwenden Schlüsselwörter, um unterschiedliche Arten von Ereignissen zu klassifizieren.
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "103858092"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a>Definieren von Schlüsselwörtern zum Klassifizieren von Ereignis Typen

Anbieter verwenden Schlüsselwörter, um unterschiedliche Arten von Ereignissen zu klassifizieren. Sie können z. b. ein Schlüsselwort für alle Lese Ereignisse erstellen und dann das Read-Schlüsselwort auf jedes Ereignis anwenden, das einen Lesevorgang ausführt, z. b. das Lesen aus einer Datei oder einer Registrierung. Consumer können dann die Bitwerte des-Schlüssel Worts verwenden, um nach einer anderen Klassifizierung von Ereignissen zu filtern. Der Consumer könnte z. b. alle Lese Ereignisse oder alle gelesenen Ereignisse von Aufgabe X anfordern (wenn Sie auch Ereignisse nach Aufgabe gruppieren). Um ein Schlüsselwort zu definieren, verwenden Sie das- **Schlüsselwort** Element.

Eine ETW-Ablauf Verfolgungs Sitzung kann die Schlüsselwörter (auf die gleiche Weise wie die Ebene) verwenden, um die Ereignisse einzuschränken, die der etw-Dienst in seine Ereignis Ablauf Verfolgungs Protokolldatei schreibt. Eine Ablauf Verfolgungs Sitzung kann den Anbieter mithilfe von zwei Sätzen von Schlüsselwort-Bitmasks aktivieren: eine "beliebige" Bitmaske, bei der das Ereignis geschrieben wird, wenn eines der Schlüsselwort Bits eines Ereignisses mit einer der in dieser Maske festgelegten Bits übereinstimmt, und einer "All"-Bitmaske, bei der für die Ereignisse, die mit "Any" übereinstimmen, das Ereignis nur dann geschrieben wird, wenn alle Bits in der "All"-Maske in der

Wenn der Anbieter z. b. ein Ereignis definiert, das ein Lese Schlüsselwort (Bit 0) und ein lokales Zugriffs Schlüsselwort (Bit 1) angibt, und ein zweites Ereignis, das ein Read-Schlüsselwort (Bit 0) und ein RAS-Schlüsselwort (Bit 2) angibt, können Sie die Bitmaske "Any" auf 1 festlegen, um alle Lese Ereignisse zu empfangen, oder Sie können die Bitmaske "beliebig" auf 1 und die Bitmaske "All" auf "3" festlegen, um nur lokale Lese

Sie müssen die Attribute **Name** und **Mask** des Schlüssel Worts angeben. Die Maske muss nur ein Bit zwischen Bit 0 und Bit 47 festlegen. Bits 48 bis 64 sind reserviert.

Das **Symbol** und die **Nachrichten** Attribute sind optional.

Im folgenden Beispiel wird gezeigt, wie Sie ein Schlüsselwort definieren.

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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
