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
# <a name="defining-event-data-templates"></a><span data-ttu-id="1b15d-103">Definieren von Ereignisdaten Vorlagen</span><span class="sxs-lookup"><span data-stu-id="1b15d-103">Defining Event Data Templates</span></span>

<span data-ttu-id="1b15d-104">Anbieter verwenden Datenvorlagen, um die ereignisspezifischen Daten zu definieren, die Sie mit einem Ereignis einschließen, und um die Filterdaten zu definieren, die eine ETW-Ablauf Verfolgungs Sitzung an den Anbieter übergeben kann, wenn Sie den Anbieter aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1b15d-104">Providers use data templates to define the event-specific data that they include with an event and to define the filter data that an ETW tracing session can pass to the provider when it enables the provider.</span></span> <span data-ttu-id="1b15d-105">Wenn das Ereignis keine ereignisspezifischen Daten enthält, wird keine Vorlage definiert.</span><span class="sxs-lookup"><span data-stu-id="1b15d-105">If the event does not include event-specific data, you will not define a template.</span></span> <span data-ttu-id="1b15d-106">Verwenden Sie das **Template** -Element, um eine Vorlage zu definieren.</span><span class="sxs-lookup"><span data-stu-id="1b15d-106">To define a template, use the **template** element.</span></span> <span data-ttu-id="1b15d-107">Eine Vorlage enthält ein Datenelement für jedes Datenelement, das der Anbieter mit dem Ereignis einschließt.</span><span class="sxs-lookup"><span data-stu-id="1b15d-107">A template includes a data item for each piece of data that the provider includes with the event.</span></span> <span data-ttu-id="1b15d-108">Sie können ganzzahlige Typen, Zeichen folgen, Arrays und Strukturen angeben.</span><span class="sxs-lookup"><span data-stu-id="1b15d-108">You can specify integral types, strings, arrays, and structures.</span></span> <span data-ttu-id="1b15d-109">Sie müssen die Ereignisdaten in der Reihenfolge schreiben, in der die Datenelemente in der Vorlage definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1b15d-109">You must write the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="1b15d-110">Sie können auch in die Vorlage einschließen, ein XML-Fragment, das Consumer verwenden sollten, um zu bestimmen, wie die Ereignisdaten gerenden werden.</span><span class="sxs-lookup"><span data-stu-id="1b15d-110">You can also include in the template, an XML fragment that consumers should use to determine how to render the event data.</span></span> <span data-ttu-id="1b15d-111">Wenn Sie das Fragment nicht einschließen, sollten Consumer die Ereignisdaten in der Reihenfolge Rendering, in der die Datenelemente in der Vorlage definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1b15d-111">If you do not include the fragment, consumers should render the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="1b15d-112">Wenn Sie eine Vorlage definieren, müssen Sie Ihr einen Vorlagen Bezeichner zuordnen, mit dem Sie in einer Ereignis Definition auf die Vorlage verweisen.</span><span class="sxs-lookup"><span data-stu-id="1b15d-112">When you define a template, you must give it a template identifier that you use to reference the template in an event definition.</span></span> <span data-ttu-id="1b15d-113">Jedes Datenelement in der Vorlage muss einen Namen und einen Eingabe Datentyp angeben (eine Liste der Eingabetypen finden Sie im Abschnitt "Hinweise" des komplexen [**InputType**](eventmanifestschema-inputtype-complextype.md) -Typs).</span><span class="sxs-lookup"><span data-stu-id="1b15d-113">Each data item in the template must specify a name and input data type (for a list of input types, see the Remarks section of the [**InputType**](eventmanifestschema-inputtype-complextype.md) complex type).</span></span> <span data-ttu-id="1b15d-114">Wenn der Eingabe Datentyp in mehreren Formaten gerendert werden kann, sollten Sie den Ausgabedatentyp angeben, der Consumer anweist, wie das Datenelement gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b15d-114">If the input data type can be rendered in multiple formats, you should specify the output data type that tells consumers how to render the data item.</span></span> <span data-ttu-id="1b15d-115">Beispielsweise kann ein UInt32 Input-Datentyp als ganze Zahl ohne Vorzeichen, als Thread Bezeichner, als IPv4-Adresse und als Win32-Fehlercode gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="1b15d-115">For example, an UInt32 input data type can be rendered as an unsigned integer, thread identifier, IPv4 address, and Win32 error code among others.</span></span> <span data-ttu-id="1b15d-116">Wenn Sie den Ausgabedatentyp nicht angeben, sollten Consumer den Standard Ausgabetyp des Eingabe Typs verwenden, um das Datenelement zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="1b15d-116">If you do not specify the output data type, consumers should use the input type's default output type to render the data item.</span></span>

<span data-ttu-id="1b15d-117">Um ein Array anzugeben, schließen Sie das **count** -Attribut für das Datenelement ein, und legen Sie es auf die Anzahl der Elemente im Array fest.</span><span class="sxs-lookup"><span data-stu-id="1b15d-117">To specify an array, include the **count** attribute on the data item and set it to the number of elements in the array.</span></span> <span data-ttu-id="1b15d-118">Das Array kann ein Array variabler Größe oder ein Array mit fester Größe sein.</span><span class="sxs-lookup"><span data-stu-id="1b15d-118">The array can be a variable size array or fixed size array.</span></span> <span data-ttu-id="1b15d-119">Wenn das Array ein Array fester Größe ist, legen Sie **count** auf die Größe des Arrays fest.</span><span class="sxs-lookup"><span data-stu-id="1b15d-119">If the array is a fixed size array, set **count** to the size of the array.</span></span> <span data-ttu-id="1b15d-120">Wenn beispielsweise ein Array aus ganzen Zahlen eine festgelegte Größe von 10 hat, legen Sie **count** auf 10 fest.</span><span class="sxs-lookup"><span data-stu-id="1b15d-120">For example, if an array of integers has a fixed size of 10, set **count** to 10.</span></span> <span data-ttu-id="1b15d-121">Wenn Sie das Array schreiben, müssen Sie 40 Bytes an Daten schreiben.</span><span class="sxs-lookup"><span data-stu-id="1b15d-121">When you write the array, you must write 40 bytes of data.</span></span>

<span data-ttu-id="1b15d-122">Wenn das Array ein Array variabler Größe ist, legen Sie **count** auf den Namen des Datenelements fest, das die Größe des Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="1b15d-122">If the array is a variable size array, set **count** to the name of the data item that contains the size of the array.</span></span> <span data-ttu-id="1b15d-123">Wenn das Array Zeiger enthält, wird die Adresse der Zeiger als Ereignisdaten geschrieben, nicht die Daten, auf die die Zeiger zeigen.</span><span class="sxs-lookup"><span data-stu-id="1b15d-123">If the array contains pointers, the address of the pointers are written as the event data, not the data to which the pointers point.</span></span>

<span data-ttu-id="1b15d-124">Sie müssen das **length** -Attribut angeben, wenn das Datenelement ein binäres Blob ist.</span><span class="sxs-lookup"><span data-stu-id="1b15d-124">You must specify the **length** attribute if the data item is a binary blob.</span></span> <span data-ttu-id="1b15d-125">Sie können auch das **length** -Attribut für Zeichen folgen mit fester Länge angeben.</span><span class="sxs-lookup"><span data-stu-id="1b15d-125">You can also specify the **length** attribute for fixed length strings.</span></span>

<span data-ttu-id="1b15d-126">Geben Sie das **map** -Attribut an, wenn das Datenelement einen Enumerationswert darstellt und Sie möchten, dass der Consumer anstelle des Werts selbst eine Zeichenfolge für den Wert druckt.</span><span class="sxs-lookup"><span data-stu-id="1b15d-126">Specify the **map** attribute if the data item represents an enumeration value and you want the consumer to print a string for the value instead of the value itself.</span></span>

<span data-ttu-id="1b15d-127">Wenn Sie Strukturen in die Vorlage einschließen, sollten Sie die Elemente der Struktur einzeln schreiben, anstatt die Struktur zu schreiben, es sei denn, Sie können eine 8-Byte-Begrenzungs Ausrichtung gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="1b15d-127">If you include structures in the template, you should write the members of the structure individually instead of writing the structure unless you can guarantee 8-byte boundary alignment.</span></span>

<span data-ttu-id="1b15d-128">Berücksichtigen Sie die Informationen, die Sie in die Ereignisse einschließen, insbesondere dann, wenn die Ereignisse in die globalen Kanäle geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1b15d-128">You should carefully consider the information that you include in the events, especially when the events are written into the global channels.</span></span> <span data-ttu-id="1b15d-129">Als allgemeine Regel sollten Sie keine privaten Informationen in die Ereignisse einschließen.</span><span class="sxs-lookup"><span data-stu-id="1b15d-129">As a general rule, you should not include private information in the events.</span></span> <span data-ttu-id="1b15d-130">Dies schließt nur-Text-Kenn Wörter und persönliche Benutzerinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="1b15d-130">This includes plaintext passwords and personal user information.</span></span> <span data-ttu-id="1b15d-131">Zusätzlich sollten Programme, die vom Benutzer ausgeführt wurden, vom Benutzer besuchte URLs und andere Informationen im Zusammenhang mit den Benutzeraktivitäten auf dem Computer als privat angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="1b15d-131">Additionally, programs run by the user, URLs that the user visited, and other information related to the user activities on the computer should be considered private.</span></span>

<span data-ttu-id="1b15d-132">Wenn Sie URLs und Benutzernamen in den Ereignissen aufzeichnen müssen, schreiben Sie Sie nicht in die Windows-Kanäle (System und Anwendung), da diese Kanäle für alle authentifizierten Benutzer lesbar sind.</span><span class="sxs-lookup"><span data-stu-id="1b15d-132">If you must record URLs and user names in the events, do not write them to the Windows channels (System and Application) because these channels are readable by all authenticated users.</span></span> <span data-ttu-id="1b15d-133">Schreiben Sie Sie stattdessen in Ihre eigenen betrieblichen oder analytischen Kanäle.</span><span class="sxs-lookup"><span data-stu-id="1b15d-133">Instead, write them to your own Operational or Analytic channels.</span></span> <span data-ttu-id="1b15d-134">Legen Sie die Zugriffsberechtigungen für diese Kanäle fest, damit nur Administratoren die Ereignisse lesen können.</span><span class="sxs-lookup"><span data-stu-id="1b15d-134">Set the access permissions on these channels to allow only administrators to read the events.</span></span> <span data-ttu-id="1b15d-135">Möglicherweise müssen Sie eine entsprechende Offenlegung angeben, um Benutzer darüber zu benachrichtigen, dass den Administratoren private Informationen zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b15d-135">You may need to provide an appropriate disclosure to notify users of the fact that private information is made available to the administrators.</span></span>

<span data-ttu-id="1b15d-136">Im folgenden Beispiel wird gezeigt, wie Sie eine Vorlage definieren.</span><span class="sxs-lookup"><span data-stu-id="1b15d-136">The following example shows how to define a template.</span></span> <span data-ttu-id="1b15d-137">Sie müssen das **TID** -Attribut der Vorlage angeben, auf das Sie in der Ereignis Definition oder Filter Definition verweisen.</span><span class="sxs-lookup"><span data-stu-id="1b15d-137">You must specify the template's **tid** attribute that you reference in the event definition or filter definition.</span></span>


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
