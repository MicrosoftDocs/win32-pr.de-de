---
title: Definieren von Kanälen
description: Ereignisse können in Ereignisprotokollkanäle, Protokolldateien für die Ereignisablaufverfolgung oder beides geschrieben werden. Ein Kanal ist im Grunde eine Senke, die Ereignisse sammelt.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c2f932616a131e478c100996fd0b76034b3cccdebf4e3714fd5b9b38ba9678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032480"
---
# <a name="defining-channels"></a>Definieren von Kanälen

Ereignisse können in Ereignisprotokollkanäle, Protokolldateien für die Ereignisablaufverfolgung oder beides geschrieben werden. Ein Kanal ist im Grunde eine Senke, die Ereignisse sammelt. Wenn die Zielgruppe für Ihre Ereignisse Ereignisverbraucher wie die Windows Ereignisanzeige verwendet, müssen Sie neue Kanäle definieren, um Ihre Ereignisse zu erfassen oder einen vorhandenen Kanal zu importieren, den ein anderer Anbieter definiert hat.

Verwenden Sie das **Channelelement,** um ihre eigenen Kanäle zu definieren. Um einen importierten Kanal zu definieren, verwenden Sie das **importChannel-Element.** Sie können bis zu acht Kanäle in einer beliebigen Kombination aus importierten Kanälen oder Kanälen angeben, die Sie definieren.

Der Kanal muss einen von vier Typen aufweisen: Admin, Operational, Analytics und Debug. Jeder Kanaltyp verfügt über eine zielgruppe, die den Typ der Ereignisse bestimmt, die Sie in den Kanal schreiben. Eine Beschreibung der einzelnen Typen finden Sie unter [**Komplexer ChannelType-Typ.**](eventmanifestschema-channeltype-complextype.md)

Um den Kanal anzugeben, in den ein Ereignis  geschrieben wird, legen Sie das Kanalattribut der Ereignisdefinition auf den gleichen Wert wie das **Chid-Attribut** der Kanaldefinition fest. Ereignisse können jeweils nur in einen Kanal geschrieben, aber auch von bis zu sieben anderen ETW-Sitzungen gleichzeitig gesammelt werden.

Das folgende Beispiel zeigt, wie ein Kanal importiert wird. Sie müssen die **Chid-** und **Namensattribute** festlegen. Das **Chid-Attribut** identifiziert den Kanal eindeutig. Jeder Kanalbezeichner in der Liste der Kanäle muss eindeutig sein. Legen Sie das **Name-Attribut** auf den gleichen Namen fest, den der Anbieter beim Definieren des Kanals verwendet hat.


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

                <channels>
                    <channel chid="c1"
                             name="Microsoft-Windows-BaseProvider/Admin"
                             symbol="CHANNEL_BASEPROVIDER_ADMIN"
                             type="Admin"/>
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

Obwohl Winmeta.xml Legacykanäle definiert, die Sie importieren können, sollten Sie sie nur verwenden, wenn Sie Legacy-Consumer unterstützen, die Ereignisse aus den Legacykanälen nutzen (z. B. Anwendung oder System). Die Winmeta.xml-Datei ist im Windows SDK enthalten.

Das folgende Beispiel zeigt, wie ein Kanal definiert wird. Sie müssen die **Chid-,** **Namens-** und **Typattribute** festlegen. Das **Chid-Attribut** identifiziert den Kanal eindeutig. Jeder Kanalbezeichner in der Liste der Kanäle muss eindeutig sein. Legen Sie das **Chid-Attribut** auf einen Wert fest, der für die Kanäle eindeutig ist, die Ihr Anbieter auflistet. Auf den Kanalbezeichner wird in einer oder mehreren Ihrer Ereignisdefinitionen verwiesen. Die Konvention für die Benennung des Kanals ist die Verwendung des Anbieternamens und Kanaltyps im Format *providername* / *channeltype.*

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

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
