---
title: Definieren von Ereignisdatenvorlagen
description: Anbieter verwenden Datenvorlagen, um die ereignisspezifischen Daten zu definieren, die sie mit einem Ereignis enthalten, und um die Filterdaten zu definieren, die eine ETW-Ablaufverfolgungssitzung an den Anbieter übergeben kann, wenn sie den Anbieter aktiviert.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5480ca158916801665943bd33b886bfcd5d73015e8730c1dd108123dadc1995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652610"
---
# <a name="defining-event-data-templates"></a>Definieren von Ereignisdatenvorlagen

Anbieter verwenden Datenvorlagen, um die ereignisspezifischen Daten zu definieren, die sie mit einem Ereignis enthalten, und um die Filterdaten zu definieren, die eine ETW-Ablaufverfolgungssitzung an den Anbieter übergeben kann, wenn sie den Anbieter aktiviert. Wenn das Ereignis keine ereignisspezifischen Daten enthält, definieren Sie keine Vorlage. Verwenden Sie zum Definieren einer Vorlage das **Vorlagenelement.** Eine Vorlage enthält ein Datenelement für jedes Datenelement, das der Anbieter in das Ereignis einfing. Sie können integrale Typen, Zeichenfolgen, Arrays und Strukturen angeben. Sie müssen die Ereignisdaten in der Reihenfolge schreiben, in der die Datenelemente in der Vorlage definiert wurden.

Sie können auch ein XML-Fragment in die Vorlage hinzufügen, das Von Consumers verwendet werden soll, um zu bestimmen, wie die Ereignisdaten gerendert werden sollen. Wenn Sie das Fragment nicht hinzufügen, sollten Benutzer die Ereignisdaten in der Reihenfolge rendern, in der die Datenelemente in der Vorlage definiert wurden.

Wenn Sie eine Vorlage definieren, müssen Sie ihr einen Vorlagenbezeichner geben, mit dem Sie auf die Vorlage in einer Ereignisdefinition verweisen. Jedes Datenelement in der Vorlage muss einen Namen und einen Eingabedatentyp angeben (eine Liste der Eingabetypen finden Sie im Abschnitt "Hinweise" des komplexen [**InputType-Typs).**](eventmanifestschema-inputtype-complextype.md) Wenn der Eingabedatentyp in mehreren Formaten gerendert werden kann, sollten Sie den Ausgabedatentyp angeben, der den Verbraucher darüber informiert, wie das Datenelement gerendert werden soll. Ein UInt32-Eingabedatentyp kann z. B. als ganze Zahl ohne Vorzeichen, Threadbezeichner, IPv4-Adresse und Win32-Fehlercode gerendert werden. Wenn Sie den Ausgabedatentyp nicht angeben, sollten Benutzer den Standardausgabetyp des Eingabetyps verwenden, um das Datenelement zu rendern.

Um ein Array anzugeben, schließen Sie das **count-Attribut** für das Datenelement ein, und legen Sie es auf die Anzahl der Elemente im Array fest. Das Array kann ein Array variabler Größe oder ein Array fester Größe sein. Wenn das Array ein Array mit fester Größe ist, legen Sie **count** auf die Größe des Arrays fest. Wenn ein Array von ganzen Zahlen beispielsweise eine feste Größe von 10 hat, legen Sie **count** auf 10 fest. Wenn Sie das Array schreiben, müssen Sie 40 Byte an Daten schreiben.

Wenn das Array ein Array variabler Größe ist, legen Sie **count** auf den Namen des Datenelements fest, das die Größe des Arrays enthält. Wenn das Array Zeiger enthält, wird die Adresse der Zeiger als Ereignisdaten geschrieben, nicht die Daten, auf die die Zeiger zeigen.

Sie müssen das **Längenattribut** angeben, wenn das Datenelement ein binäres Blob ist. Sie können auch das **Length-Attribut für Zeichenfolgen** fester Länge angeben.

Geben Sie **das Map-Attribut** an, wenn das Datenelement einen Enumerationswert darstellt und der Consumer anstelle des Werts selbst eine Zeichenfolge für den Wert drucken soll.

Wenn Sie Strukturen in die Vorlage integrieren, sollten Sie die Member der Struktur einzeln schreiben, anstatt die Struktur zu schreiben, es sei denn, Sie können eine 8-Byte-Begrenzungsausrichtung garantieren.

Sie sollten die Informationen, die Sie in die Ereignisse einreihen, sorgfältig berücksichtigen, insbesondere, wenn die Ereignisse in die globalen Kanäle geschrieben werden. In der Regel sollten Sie keine privaten Informationen in die Ereignisse einreihen. Dies schließt Klartextkennwörter und persönliche Benutzerinformationen ein. Darüber hinaus sollten vom Benutzer ausgeführte Programme, urLs, die der Benutzer besucht hat, und andere Informationen im Zusammenhang mit den Benutzeraktivitäten auf dem Computer als privat betrachtet werden.

Wenn Sie URLs und Benutzernamen in den Ereignissen aufzeichnen müssen, schreiben Sie sie nicht in die Windows-Kanäle (System und Anwendung), da diese Kanäle für alle authentifizierten Benutzer lesbar sind. Schreiben Sie sie stattdessen in Ihre eigenen Betriebs- oder Analysekanäle. Legen Sie die Zugriffsberechtigungen für diese Kanäle fest, damit nur Administratoren die Ereignisse lesen können. Möglicherweise müssen Sie eine geeignete Offenlegung bereitstellen, um benutzer darüber zu informieren, dass den Administratoren private Informationen zur Verfügung gestellt werden.

Das folgende Beispiel zeigt, wie Eine Vorlage definiert wird. Sie müssen das **tid-Attribut** der Vorlage angeben, auf das Sie in der Ereignisdefinition oder Filterdefinition verweisen.


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

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

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
