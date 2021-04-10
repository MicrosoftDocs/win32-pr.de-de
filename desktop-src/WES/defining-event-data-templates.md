---
title: Definieren von Ereignisdaten Vorlagen
description: Anbieter verwenden Datenvorlagen, um die ereignisspezifischen Daten zu definieren, die Sie mit einem Ereignis einschließen, und um die Filterdaten zu definieren, die eine ETW-Ablauf Verfolgungs Sitzung an den Anbieter übergeben kann, wenn Sie den Anbieter aktiviert.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067230472c8de5ce29145e221c109b3f390f0a6c
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "103858095"
---
# <a name="defining-event-data-templates"></a>Definieren von Ereignisdaten Vorlagen

Anbieter verwenden Datenvorlagen, um die ereignisspezifischen Daten zu definieren, die Sie mit einem Ereignis einschließen, und um die Filterdaten zu definieren, die eine ETW-Ablauf Verfolgungs Sitzung an den Anbieter übergeben kann, wenn Sie den Anbieter aktiviert. Wenn das Ereignis keine ereignisspezifischen Daten enthält, wird keine Vorlage definiert. Verwenden Sie das **Template** -Element, um eine Vorlage zu definieren. Eine Vorlage enthält ein Datenelement für jedes Datenelement, das der Anbieter mit dem Ereignis einschließt. Sie können ganzzahlige Typen, Zeichen folgen, Arrays und Strukturen angeben. Sie müssen die Ereignisdaten in der Reihenfolge schreiben, in der die Datenelemente in der Vorlage definiert wurden.

Sie können auch in die Vorlage einschließen, ein XML-Fragment, das Consumer verwenden sollten, um zu bestimmen, wie die Ereignisdaten gerenden werden. Wenn Sie das Fragment nicht einschließen, sollten Consumer die Ereignisdaten in der Reihenfolge Rendering, in der die Datenelemente in der Vorlage definiert wurden.

Wenn Sie eine Vorlage definieren, müssen Sie Ihr einen Vorlagen Bezeichner zuordnen, mit dem Sie in einer Ereignis Definition auf die Vorlage verweisen. Jedes Datenelement in der Vorlage muss einen Namen und einen Eingabe Datentyp angeben (eine Liste der Eingabetypen finden Sie im Abschnitt "Hinweise" des komplexen [**InputType**](eventmanifestschema-inputtype-complextype.md) -Typs). Wenn der Eingabe Datentyp in mehreren Formaten gerendert werden kann, sollten Sie den Ausgabedatentyp angeben, der Consumer anweist, wie das Datenelement gerendert werden soll. Beispielsweise kann ein UInt32 Input-Datentyp als ganze Zahl ohne Vorzeichen, als Thread Bezeichner, als IPv4-Adresse und als Win32-Fehlercode gerendert werden. Wenn Sie den Ausgabedatentyp nicht angeben, sollten Consumer den Standard Ausgabetyp des Eingabe Typs verwenden, um das Datenelement zu Rendering.

Um ein Array anzugeben, schließen Sie das **count** -Attribut für das Datenelement ein, und legen Sie es auf die Anzahl der Elemente im Array fest. Das Array kann ein Array variabler Größe oder ein Array mit fester Größe sein. Wenn das Array ein Array fester Größe ist, legen Sie **count** auf die Größe des Arrays fest. Wenn beispielsweise ein Array aus ganzen Zahlen eine festgelegte Größe von 10 hat, legen Sie **count** auf 10 fest. Wenn Sie das Array schreiben, müssen Sie 40 Bytes an Daten schreiben.

Wenn das Array ein Array variabler Größe ist, legen Sie **count** auf den Namen des Datenelements fest, das die Größe des Arrays enthält. Wenn das Array Zeiger enthält, wird die Adresse der Zeiger als Ereignisdaten geschrieben, nicht die Daten, auf die die Zeiger zeigen.

Sie müssen das **length** -Attribut angeben, wenn das Datenelement ein binäres Blob ist. Sie können auch das **length** -Attribut für Zeichen folgen mit fester Länge angeben.

Geben Sie das **map** -Attribut an, wenn das Datenelement einen Enumerationswert darstellt und Sie möchten, dass der Consumer anstelle des Werts selbst eine Zeichenfolge für den Wert druckt.

Wenn Sie Strukturen in die Vorlage einschließen, sollten Sie die Elemente der Struktur einzeln schreiben, anstatt die Struktur zu schreiben, es sei denn, Sie können eine 8-Byte-Begrenzungs Ausrichtung gewährleisten.

Berücksichtigen Sie die Informationen, die Sie in die Ereignisse einschließen, insbesondere dann, wenn die Ereignisse in die globalen Kanäle geschrieben werden. Als allgemeine Regel sollten Sie keine privaten Informationen in die Ereignisse einschließen. Dies schließt nur-Text-Kenn Wörter und persönliche Benutzerinformationen ein. Zusätzlich sollten Programme, die vom Benutzer ausgeführt wurden, vom Benutzer besuchte URLs und andere Informationen im Zusammenhang mit den Benutzeraktivitäten auf dem Computer als privat angesehen werden.

Wenn Sie URLs und Benutzernamen in den Ereignissen aufzeichnen müssen, schreiben Sie Sie nicht in die Windows-Kanäle (System und Anwendung), da diese Kanäle für alle authentifizierten Benutzer lesbar sind. Schreiben Sie Sie stattdessen in Ihre eigenen betrieblichen oder analytischen Kanäle. Legen Sie die Zugriffsberechtigungen für diese Kanäle fest, damit nur Administratoren die Ereignisse lesen können. Möglicherweise müssen Sie eine entsprechende Offenlegung angeben, um Benutzer darüber zu benachrichtigen, dass den Administratoren private Informationen zur Verfügung gestellt werden.

Im folgenden Beispiel wird gezeigt, wie Sie eine Vorlage definieren. Sie müssen das **TID** -Attribut der Vorlage angeben, auf das Sie in der Ereignis Definition oder Filter Definition verweisen.


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
