---
title: Definieren von Ereignissen
description: Anbieter müssen alle Ereignisse definieren, die Sie schreiben. Verwenden Sie zum Definieren eines Ereignisses das-Ereignis Element.
ms.assetid: f282612c-cfa5-42fe-af8a-5b35c033abe2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4c1da0e54d1e9fc328978ebe447c8e843b540c
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104390093"
---
# <a name="defining-events"></a>Definieren von Ereignissen

Anbieter müssen alle Ereignisse definieren, die Sie schreiben. Verwenden Sie zum Definieren eines Ereignisses das- **Ereignis** Element.

Das **value** -Attribut ist der Ereignis Bezeichner, der für die von Ihnen definierten Ereignisse eindeutig sein muss. Ob Sie die anderen Attribute festlegen, hängt davon ab, wer die Ereignisse verarbeiten soll und von wo. Wenn Administratoren ihre Ereignisse mithilfe eines Tools wie Windows Ereignisanzeige nutzen, müssen Sie das **Channel** -Attribut festlegen. Wenn der Kanaltyp admin ist, müssen Sie auch das **Level** -Attribut angeben und es auf eine der Ebenen festlegen, die in Winmeta.xml (Win: Critical durch Win: verbose) definiert sind.

Wenn das Ereignis ereignisspezifische Daten enthält, müssen Sie das **Vorlagen** Attribut auf den Bezeichner der Vorlage festlegen, die die ereignisspezifischen Daten definiert. Die Attribute **Level**, **Keywords**, **Task** und **Opcode** werden verwendet, um Ereignisse zu gruppieren oder zu Bucket. Obwohl diese Attribute optional sind, sollten Sie die Angabe von Ebene, Aufgabe, Opcode und Schlüsselwörtern in Erwägung gezogen, damit Consumer auf einfache Weise nur auf relevante Ereignisse zugreifen können. Die Attribute **Level** und **Keywords** können auch von einer etw-Ablauf Verfolgungs Sitzung verwendet werden, um die Ereignisse einzuschränken, die in die Protokolldatei der Ereignis Ablauf Verfolgung geschrieben werden. Das **Keywords** -Attribut enthält eine durch Leerzeichen getrennte Liste von Schlüsselwort Namen, die im Manifest definiert sind. Wenn mehrere Schlüsselwörter angegeben werden, werden Ihre Masken Werte zusammengefasst, um den Schlüsselwort Wert zu erstellen, der vom Ereignis verwendet wird.

Sie sollten das **Symbol** Attribut festlegen, um die symbolische Konstante anzugeben, die vom Compiler generiert wird, um den Ereignis Deskriptor des Ereignisses zu identifizieren – Sie verwenden beim Schreiben des Ereignisses den Ereignis Deskriptor. Wenn Sie das Symbol nicht angeben, generiert der Compiler einen Namen für Sie.

Das **Message** -Attribut enthält die lokalisierte Nachrichten Zeichenfolge, die mit dem-Ereignis angezeigt wird. Um ereignisspezifische Daten in die Zeichenfolge einzuschließen, fügen Sie dem Meldungs Text Einfügezeichenfolgen hinzu. Wenn Sie z. b. das dritte Datenelement in die Vorlage einschließen möchten, schließen Sie %3 ein.

Das folgende Beispiel zeigt ein umfassendes Manifest, das Ereignisse definiert.

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

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>

                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                <tasks>
                    <task name="Disconnect"
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>

                    <task name="Connect"
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)"/>

                    <task name="Validate"
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)"/>
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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

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

                    <template tid="t4">
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="Path" inType="win:UnicodeString" />
                    </template>
                </templates>

                <events>
                    <event value="1"
                        level="win:Informational"
                        keywords="Remote Read"
                        task="Connect"
                        template="t2"
                        channel="c1"
                        symbol="TRANSFER_SCHEDULE_EVENT"
                        message ="$(string.Event.XferSchedule)"/>

                    <event value="2"
                        level="win:Error"
                        keywords="Remote Write"
                        task="Disconnect"
                        opcode="Initialize"
                        template="t3"
                        channel="c1"
                        symbol="DOWNLOAD_XFER_FAILED_EVENT"
                        message ="$(string.Event.DownloadFailed)"/>

                    <event value="3"
                        level="NotValid"
                        keywords="Local Write"
                        task="Validate"
                        opcode="Cleanup"
                        template="t4"
                        channel="c2"
                        symbol="TEMPFILE_CLEANUP_EVENT"
                        message ="$(string.Event.TempFilesNotDeleted)"/>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
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
                <string id="Event.XferSchedule" value="The %1 %2 transfer will occur on %3."/>
                <string id="Event.DownloadFailed" value="The %1 download job failed with %2. The job contains the following files:%n%n%4"/>
                <string id="Event.TempFilesNotDeleted" value="The following temp files were not removed from %3:%n%n%2"/>
            </stringTable>
        </resources>
    </localization>
</instrumentationManifest>
```
