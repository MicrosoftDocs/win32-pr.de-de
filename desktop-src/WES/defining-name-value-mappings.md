---
title: Definieren von Name/Wert-Zuordnungen
description: Ein Anbieter kann eine Liste von Name-Wert-Paaren definieren, mit denen Verbraucher ganzzahlige Werte Zeichenfolgen zuordnen.
ms.assetid: d16b2410-a0de-42da-8f2a-98341c90ed87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ddf3ebb45ba509356a38797682be2be5d5bf1867b81767ce4fe262d678517a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937212"
---
# <a name="defining-namevalue-mappings"></a>Definieren von Name/Wert-Zuordnungen

Ein Anbieter kann eine Liste von Name-Wert-Paaren definieren, mit denen Verbraucher ganzzahlige Werte Zeichenfolgen zuordnen. Die Name-Wert-Paare können Zeichenfolgen ganzzahlige Werte oder Bitwerte Bitwerte zu Zeichenfolgen zuordnen. jeder Wert entspricht einem Zeichenfolgenwert. Verwenden Sie Zuordnungen für ganzzahlige Datenelemente, die Enumerationswerte enthalten.

Benutzer können die Wertzuordnung verwenden, um die einem Wert zugeordnete Zeichenfolge abzurufen und anzuzeigen, anstatt den Ganzzahl- oder Bitwert anzuzeigen. Verwenden Sie zum Definieren einer Ganzzahlwertzuordnung die **Elemente valueMap** und **map.** Um eine Bitwertzuordnung zu definieren, verwenden Sie die **Bitmap-** und **Kartenelemente.**

Das folgende Beispiel zeigt, wie Sie eine Wertzuordnung und eine Bitmap definieren. Sie müssen das Namensattribut der **Karte** angeben. Für jedes Name-Wert-Paar müssen Sie den Wert **und** das **Nachrichtenattribut** angeben.


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

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
