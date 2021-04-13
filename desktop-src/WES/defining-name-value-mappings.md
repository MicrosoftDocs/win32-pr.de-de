---
title: Definieren von Name-Wert-Zuordnungen
description: Ein Anbieter kann eine Liste von Name-Wert-Paaren definieren, die Consumer zum Zuordnen von ganzzahligen Werten zu Zeichen folgen verwenden.
ms.assetid: d16b2410-a0de-42da-8f2a-98341c90ed87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62020adeb46bac96cada70cf5830e17213d69868
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104390090"
---
# <a name="defining-namevalue-mappings"></a><span data-ttu-id="dc00f-103">Definieren von Name-Wert-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="dc00f-103">Defining Name/Value Mappings</span></span>

<span data-ttu-id="dc00f-104">Ein Anbieter kann eine Liste von Name-Wert-Paaren definieren, die Consumer zum Zuordnen von ganzzahligen Werten zu Zeichen folgen verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc00f-104">A provider can define a list of name/value pairs that consumers use to map integer values to strings.</span></span> <span data-ttu-id="dc00f-105">Die Name-Wert-Paare können ganzzahlige Werte zu Zeichen folgen oder Bitwerten von Bitwerten zu Zeichen folgen zuordnen. Jeder Wert entspricht einem Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="dc00f-105">The name/value pairs can map integer values to strings or bit values bit values to strings; each value corresponds to a string value.</span></span> <span data-ttu-id="dc00f-106">Verwenden Sie Zuordnungen für ganzzahlige Datenelemente, die Enumerationswerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc00f-106">Use mappings on integer data items that contain enumeration values.</span></span>

<span data-ttu-id="dc00f-107">Consumer können den Wert map verwenden, um die einem Wert zugeordnete Zeichenfolge abzurufen und anzuzeigen, anstatt die Ganzzahl oder den Bitwert anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dc00f-107">Consumers can use the value map to retrieve the string associated with a value and display it instead of displaying the integer or bit value.</span></span> <span data-ttu-id="dc00f-108">Um eine ganzzahlige Werte Zuordnung zu definieren, verwenden Sie das **ValueMap** -und das **map** -Element.</span><span class="sxs-lookup"><span data-stu-id="dc00f-108">To define an integer value map, use the **valueMap** and **map** elements.</span></span> <span data-ttu-id="dc00f-109">Verwenden Sie zum Definieren einer Bitwert Zuordnung das **Bitmap** -Element und das **map** -Element.</span><span class="sxs-lookup"><span data-stu-id="dc00f-109">To define a bit value map, use the **bitmap** and **map** elements.</span></span>

<span data-ttu-id="dc00f-110">Im folgenden Beispiel wird gezeigt, wie eine Werte Zuordnung und eine Bitmap definiert werden.</span><span class="sxs-lookup"><span data-stu-id="dc00f-110">The following example shows how to define a value map and a bitmap.</span></span> <span data-ttu-id="dc00f-111">Sie müssen das **Name** -Attribut der Zuordnung angeben.</span><span class="sxs-lookup"><span data-stu-id="dc00f-111">You must specify the map's **name** attribute.</span></span> <span data-ttu-id="dc00f-112">Sie müssen für jedes Name/Wert-Paar den **Wert** und das **Nachrichten** Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="dc00f-112">For each name/value pair, you must specify the **value** and **message** attribute.</span></span>


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
