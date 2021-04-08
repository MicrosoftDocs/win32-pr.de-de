---
title: Definieren von Kanälen
description: Ereignisse können in Ereignisprotokoll Kanäle, Ereignis Ablauf Verfolgungs Protokolldateien oder beides geschrieben werden. Ein Kanal ist im Grunde genommen eine Senke, die Ereignisse sammelt.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3c73697aa11e7b63ace0ece33be23ca7a1b883
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104101362"
---
# <a name="defining-channels"></a>Definieren von Kanälen

Ereignisse können in Ereignisprotokoll Kanäle, Ereignis Ablauf Verfolgungs Protokolldateien oder beides geschrieben werden. Ein Kanal ist im Grunde genommen eine Senke, die Ereignisse sammelt. Wenn die Zielgruppe für Ihre Ereignisse Ereignisconsumer verwendet, z. b. die Windows-Ereignisanzeige, müssen Sie neue Kanäle definieren, um die Ereignisse zu erfassen oder einen von einem anderen Anbieter definierten vorhandenen Kanal zu importieren.

Verwenden Sie das **Channel** -Element, um eigene Kanäle zu definieren. Verwenden Sie das **importchannel** -Element, um einen importierten Kanal zu definieren. Sie können bis zu acht Kanäle in einer beliebigen Kombination aus importierten Kanälen oder Kanälen angeben, die Sie definieren.

Der Kanal muss einen von vier Typen aufweisen: "admin", "Operational", "Analytic" und "Debug". Jeder Kanaltyp verfügt über eine beabsichtigte Zielgruppe, die den Typ der Ereignisse bestimmt, die Sie in den Kanal schreiben. Eine Beschreibung der einzelnen Typen finden Sie unter der komplexe [**channelType**](eventmanifestschema-channeltype-complextype.md) -Typ.

Legen Sie zum Angeben des Kanals, auf den ein Ereignis geschrieben wird, das **Channel** -Attribut der Ereignis Definition auf denselben Wert wie das **Chid** -Attribut der Channeldefinition fest. Ereignisse können jeweils nur in einen Kanal geschrieben werden, können jedoch auch von bis zu 7 anderen ETW-Sitzungen gleichzeitig gesammelt werden.

Im folgenden Beispiel wird gezeigt, wie ein Kanal importiert wird. Sie müssen die Attribute " **Chid** " und " **Name** " festlegen. Das **Chid** -Attribut identifiziert den Channel eindeutig – jeder Kanal Bezeichner in der Liste der Channels muss eindeutig sein. Legen Sie das **Name** -Attribut auf den Namen fest, der vom Anbieter beim Definieren des Kanals verwendet wurde.


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

Obwohl Winmeta.xml Legacy Kanäle definiert, die importiert werden können, sollten Sie Sie nicht verwenden, es sei denn, Sie unterstützen Legacy-Consumer, die Ereignisse aus den Legacy Kanälen (z. b. Anwendung oder System) nutzen. Die Winmeta.xml-Datei ist im Windows SDK enthalten.

Im folgenden Beispiel wird gezeigt, wie ein Kanal definiert wird. Sie müssen die Attribute " **Chid**", " **Name**" und " **Type** " festlegen. Das **Chid** -Attribut identifiziert den Channel eindeutig – jeder Kanal Bezeichner in der Liste der Channels muss eindeutig sein. Legen Sie das **Chid** -Attribut auf einen Wert fest, der für die Kanäle eindeutig ist, die Ihr Anbieter auflistet. auf den Kanal Bezeichner wird in einer oder mehreren Ereignis Definitionen verwiesen. Die Konvention für die Benennung des Kanals besteht darin, den Anbieter Namen und den Kanaltyp in der Form *Provider Name* / *channelType* zu verwenden.

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
