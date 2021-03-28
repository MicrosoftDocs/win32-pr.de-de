---
description: Klassische Anbieter sollten Managed Object Format (MOF) verwenden, um das Layout Ihrer Ereignisdaten zu veröffentlichen. Consumer können das veröffentlichte Layout dann zur Laufzeit aus WMI lesen und zum Lesen der Ereignisdaten verwenden.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Veröffentlichen Ihres Ereignis Schemas für einen klassischen Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f51cfd30d0c9d73841ca906fb81e9d544dec88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343879"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a><span data-ttu-id="42e78-104">Veröffentlichen Ihres Ereignis Schemas für einen klassischen Anbieter</span><span class="sxs-lookup"><span data-stu-id="42e78-104">Publishing Your Event Schema for a Classic Provider</span></span>

<span data-ttu-id="42e78-105">[Klassische](about-event-tracing.md) Anbieter sollten [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) verwenden, um das Layout Ihrer Ereignisdaten zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="42e78-105">[Classic](about-event-tracing.md) providers should use [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) to publish the layout of their event data.</span></span> <span data-ttu-id="42e78-106">Consumer können das veröffentlichte Layout dann zur Laufzeit aus WMI lesen und zum Lesen der Ereignisdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e78-106">Consumers can then read the published layout from WMI at runtime and use it to read the event data.</span></span>

<span data-ttu-id="42e78-107">Wenn Sie MOF verwenden, um das Layout der Ereignisdaten in WMI zu veröffentlichen, erstellen Sie in der Regel die folgenden drei Typen von MOF-Klassen im Stamm- \\ WMI-Namespace:</span><span class="sxs-lookup"><span data-stu-id="42e78-107">If you use MOF to publish the layout of your event data in WMI, you typically create the following three types of MOF classes in the root\\wmi namespace:</span></span>

-   [<span data-ttu-id="42e78-108">Eine MOF-Anbieter Klasse</span><span class="sxs-lookup"><span data-stu-id="42e78-108">A provider MOF class</span></span>](#provider-mof-classes)
-   [<span data-ttu-id="42e78-109">Mindestens eine MOF-Ereignisklasse</span><span class="sxs-lookup"><span data-stu-id="42e78-109">One or more event MOF classes</span></span>](#event-mof-classes)
-   [<span data-ttu-id="42e78-110">Mindestens eine MOF-Klasse für den Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="42e78-110">One or more event type MOF classes</span></span>](#event-type-mof-classes)

## <a name="provider-mof-classes"></a><span data-ttu-id="42e78-111">MOF-Anbieter Klassen</span><span class="sxs-lookup"><span data-stu-id="42e78-111">Provider MOF classes</span></span>

<span data-ttu-id="42e78-112">Wenn Sie das Layout der Ereignisdaten veröffentlichen, müssen Sie eine MOF-Klasse erstellen, die Ihren Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="42e78-112">If you publish the layout of your event data, you must create a MOF class that identifies your provider.</span></span> <span data-ttu-id="42e78-113">Diese Klasse muss von der **EventTrace** MOF-Klasse abgeleitet werden und muss leer sein (keine Eigenschaften oder Methoden).</span><span class="sxs-lookup"><span data-stu-id="42e78-113">This class must derive from the **EventTrace** MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="42e78-114">Die Klasse muss auch den **GUID** -Qualifizierer enthalten, der den Anbieter eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="42e78-114">The class must also include the **Guid** qualifier which uniquely identifies the provider.</span></span> <span data-ttu-id="42e78-115">Dies ist dieselbe GUID, die Sie verwenden, wenn Sie die [**registertraceguids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) -Funktion aufrufen, um den Anbieter zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="42e78-115">This is the same GUID you use when you calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register your provider.</span></span>

## <a name="event-mof-classes"></a><span data-ttu-id="42e78-116">MOF-Ereignis Klassen</span><span class="sxs-lookup"><span data-stu-id="42e78-116">Event MOF classes</span></span>

<span data-ttu-id="42e78-117">Eine MOF-Ereignisklasse definiert eine Klasse von Ereignissen, die der Anbieter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="42e78-117">An event MOF class defines a class of events that the provider provides.</span></span> <span data-ttu-id="42e78-118">Diese Klasse wird von der MOF-Klasse des Anbieters abgeleitet und muss leer sein (keine Eigenschaften oder Methoden).</span><span class="sxs-lookup"><span data-stu-id="42e78-118">This class derives from the provider MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="42e78-119">Die Klasse muss auch den **GUID** -Qualifizierer enthalten, der die Klasse der Ereignisse eindeutig identifiziert, die von den untergeordneten Klassen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="42e78-119">The class must also include the **Guid** qualifier which uniquely identifies the class of events that its child classes define.</span></span> <span data-ttu-id="42e78-120">Der Anbieter verwendet dieselbe GUID, wenn der **GUID** -Member der Ereignis-Ablauf [**\_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="42e78-120">The provider uses this same GUID when setting the **Guid** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="event-type-mof-classes"></a><span data-ttu-id="42e78-121">MOF-Ereignistyp Klassen</span><span class="sxs-lookup"><span data-stu-id="42e78-121">Event type MOF classes</span></span>

<span data-ttu-id="42e78-122">Eine MOF-Klasse für den Ereignistyp definiert die tatsächlichen Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="42e78-122">An event type MOF class defines the actual event data.</span></span> <span data-ttu-id="42e78-123">Diese Klasse wird von der übergeordneten Ereignis-MOF-Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="42e78-123">This class derives from its parent event MOF class.</span></span> <span data-ttu-id="42e78-124">Wenn Sie die MOF-Klasse für den Ereignistyp benennen, besteht die Konvention darin, den MOF-Ereignis Klassennamen am Anfang des MOF-Klassen namens des Ereignis Typs zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e78-124">When naming the event type MOF class, the convention is to use the event MOF class name at the beginning of the event type MOF class name.</span></span> <span data-ttu-id="42e78-125">Wenn z. b. der MOF-Klassenname des Ereignisses hwconfig ist und die MOF-Klasse des Ereignis Typs CPU-Informationen darstellt, sollten Sie den Ereignistyp MOF Class, hwconfig CPU, benennen \_ .</span><span class="sxs-lookup"><span data-stu-id="42e78-125">For example, if the event MOF class name is HWConfig and the event type MOF class represents CPU information, you should name the event type MOF class, HWConfig\_CPU.</span></span>

<span data-ttu-id="42e78-126">Verwenden Sie den **eventType** -Qualifizierer für die MOF-Ereignisklasse, um den Ereignistyp zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="42e78-126">Use the **EventType** qualifier on the event type MOF class to identify the event type.</span></span> <span data-ttu-id="42e78-127">Wenn mehrere Ereignis Typen dieselben Ereignisdaten verwenden, können Sie dieselbe MOF-Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e78-127">If multiple event types use the same event data, they can use the same MOF class.</span></span> <span data-ttu-id="42e78-128">Der Anbieter verwendet den gleichen Ereignistyp Wert, um das Ereignis zu identifizieren, wenn der **Class. Type** -Member der Ereignis-Ablauf [**\_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="42e78-128">The provider uses the same event type value to identify the event when setting the **Class.Type** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

<span data-ttu-id="42e78-129">Die MOF-Ereignistyp Klasse enthält Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42e78-129">The event type MOF class contains properties.</span></span> <span data-ttu-id="42e78-130">Die Reihenfolge dieser Eigenschaften definiert das Layout der Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="42e78-130">The order of these properties define the layout of the event data.</span></span> <span data-ttu-id="42e78-131">In der folgenden Tabelle sind die Datentypen und Qualifizierer aufgeführt, die Sie zum Definieren der Eigenschaften verwenden können.</span><span class="sxs-lookup"><span data-stu-id="42e78-131">The following table identifies the data types and qualifiers you can use to define the properties.</span></span> <span data-ttu-id="42e78-132">Weitere Informationen zu den Eigenschaften und Klassen Qualifizierern, die Sie verwenden können, finden Sie unter [Ereignis Ablauf Verfolgung MOF-Qualifizierer](event-tracing-mof-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="42e78-132">For more information on the property and class qualifiers that you can use, see [Event Tracing MOF Qualifiers](event-tracing-mof-qualifiers.md).</span></span>



| <span data-ttu-id="42e78-133">Datentyp</span><span class="sxs-lookup"><span data-stu-id="42e78-133">Data type</span></span>              | <span data-ttu-id="42e78-134">Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="42e78-134">Qualifiers</span></span>                        | <span data-ttu-id="42e78-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42e78-135">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e78-136">**sint8**, **Uint8**</span><span class="sxs-lookup"><span data-stu-id="42e78-136">**sint8**, **uint8**</span></span>   | <span data-ttu-id="42e78-137">**Format**</span><span class="sxs-lookup"><span data-stu-id="42e78-137">**Format**</span></span>                        | <span data-ttu-id="42e78-138">Deklariert eine 1-Byte-Ganzzahl mit Dezimalzahlen.</span><span class="sxs-lookup"><span data-stu-id="42e78-138">Declares a 1-byte decimal integer.</span></span> <span data-ttu-id="42e78-139">Verwenden Sie zum Deklarieren eines ANSI-Zeichens den **Format** Qualifizierer, und legen Sie dessen Wert auf "c" fest.</span><span class="sxs-lookup"><span data-stu-id="42e78-139">To declare an ANSI character, use the **Format** qualifier and set its value to "c".</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="42e78-140">**sint16**, **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42e78-140">**sint16**, **uint16**</span></span> | <span data-ttu-id="42e78-141">**Format**</span><span class="sxs-lookup"><span data-stu-id="42e78-141">**Format**</span></span>                        | <span data-ttu-id="42e78-142">Deklariert eine ganzzahlige 2-Byte-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="42e78-142">Declares a 2-byte decimal integer.</span></span> <span data-ttu-id="42e78-143">Um anzugeben, dass die Zahl eine hexadezimale Zahl ist, verwenden Sie den **Format** Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="42e78-143">To indicate the number is a hexadecimal number, use the **Format** qualifier.</span></span> <span data-ttu-id="42e78-144">Beispiel: Format ("x").</span><span class="sxs-lookup"><span data-stu-id="42e78-144">For example, format("x").</span></span>                                                                                                                                                                               |
| <span data-ttu-id="42e78-145">**sint32**, **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42e78-145">**sint32**, **uint32**</span></span> | <span data-ttu-id="42e78-146">**Format**</span><span class="sxs-lookup"><span data-stu-id="42e78-146">**Format**</span></span>                        | <span data-ttu-id="42e78-147">Deklariert eine ganze 4-Byte-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="42e78-147">Declares a 4-byte decimal integer.</span></span> <span data-ttu-id="42e78-148">Um anzugeben, dass die Zahl eine hexadezimale Zahl ist, verwenden Sie den **Format** Qualifizierer, und legen Sie dessen Wert auf "x" fest.</span><span class="sxs-lookup"><span data-stu-id="42e78-148">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="42e78-149">**sint64**, **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42e78-149">**sint64**, **uint64**</span></span> | <span data-ttu-id="42e78-150">**Format**</span><span class="sxs-lookup"><span data-stu-id="42e78-150">**Format**</span></span>                        | <span data-ttu-id="42e78-151">Deklariert eine 8-Byte-Ganzzahl mit Dezimalzahlen.</span><span class="sxs-lookup"><span data-stu-id="42e78-151">Declares a 8-byte decimal integer.</span></span> <span data-ttu-id="42e78-152">Um anzugeben, dass die Zahl eine hexadezimale Zahl ist, verwenden Sie den **Format** Qualifizierer, und legen Sie dessen Wert auf "x" fest.</span><span class="sxs-lookup"><span data-stu-id="42e78-152">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="42e78-153">**boolean**</span><span class="sxs-lookup"><span data-stu-id="42e78-153">**boolean**</span></span>            |                                   | <span data-ttu-id="42e78-154">Deklariert einen booleschen Wert.</span><span class="sxs-lookup"><span data-stu-id="42e78-154">Declares a Boolean value.</span></span> <span data-ttu-id="42e78-155">Der Ereignisconsumer sollte den Wert als bool (4-Byte-Ganzzahl) interpretieren.</span><span class="sxs-lookup"><span data-stu-id="42e78-155">The event consumer should interpret the value as BOOL (4-byte integer).</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="42e78-156">**char16**</span><span class="sxs-lookup"><span data-stu-id="42e78-156">**char16**</span></span>             |                                   | <span data-ttu-id="42e78-157">Deklariert ein breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="42e78-157">Declares a wide character.</span></span> <span data-ttu-id="42e78-158">Der Ereignisconsumer sollte char16 Arrays in Kernel Ereignissen als breit Zeichen-Zeichen folgen interpretieren.</span><span class="sxs-lookup"><span data-stu-id="42e78-158">The event consumer should interpret char16 arrays in kernel events as wide character strings.</span></span> <span data-ttu-id="42e78-159">(Verwenden Sie die Array Größe, um die Zeichenfolge zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="42e78-159">(Use the array size to copy the string.</span></span> <span data-ttu-id="42e78-160">Einige Zeichen folgen können führende Null-Zeichen enthalten.)</span><span class="sxs-lookup"><span data-stu-id="42e78-160">Some strings may contain leading NULL characters.)</span></span>                                                                                                      |
| <span data-ttu-id="42e78-161">**object**</span><span class="sxs-lookup"><span data-stu-id="42e78-161">**object**</span></span>             | <span data-ttu-id="42e78-162">**Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="42e78-162">**Extension**</span></span>                     | <span data-ttu-id="42e78-163">Deklariert ein binäres Blob.</span><span class="sxs-lookup"><span data-stu-id="42e78-163">Declares a binary blob.</span></span> <span data-ttu-id="42e78-164">Der **Erweiterungs** Qualifizierer gibt den Typ der Daten im BLOB an.</span><span class="sxs-lookup"><span data-stu-id="42e78-164">The **Extension** qualifier indicates the type of data in the blob.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="42e78-165">**string**</span><span class="sxs-lookup"><span data-stu-id="42e78-165">**string**</span></span>             | <span data-ttu-id="42e78-166">**Format**, **stringbeendigung**</span><span class="sxs-lookup"><span data-stu-id="42e78-166">**Format**, **StringTermination**</span></span> | <span data-ttu-id="42e78-167">Deklariert einen Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="42e78-167">Declares a string value.</span></span> <span data-ttu-id="42e78-168">Um anzugeben, dass die Zeichenfolge eine Zeichenfolge mit breit Zeichen ist, verwenden Sie den **Format** Qualifizierer und legen den Wert auf "w" fest.</span><span class="sxs-lookup"><span data-stu-id="42e78-168">To indicate the string is a wide-character string use the **Format** qualifier and set its value to "w".</span></span> <span data-ttu-id="42e78-169">Die Zeichenfolge wird als ANSI-Zeichenfolge betrachtet, wenn Sie nicht den **Format** Qualifizierer angeben.</span><span class="sxs-lookup"><span data-stu-id="42e78-169">The string is considered an ANSI string if you do not specify the **Format** qualifier.</span></span> <span data-ttu-id="42e78-170">Um anzugeben, wie die Zeichenfolge beendet wird, verwenden Sie den **stringbeendigung** -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="42e78-170">To indicate how the string is terminated, use the **StringTermination** qualifier.</span></span> <br/> |



 

<span data-ttu-id="42e78-171">Zum Angeben eines Arrays können Sie eckige Klammern () verwenden \[ \] .</span><span class="sxs-lookup"><span data-stu-id="42e78-171">To specify an array, you can use square brackets, \[\].</span></span> <span data-ttu-id="42e78-172">Die eckigen Klammern können die Größe des Arrays einschließen.</span><span class="sxs-lookup"><span data-stu-id="42e78-172">The square brackets can include the size of the array.</span></span> <span data-ttu-id="42e78-173">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42e78-173">For example:</span></span>

`[WmiDataId(1), read] uint8 MyGuid[16];`

<span data-ttu-id="42e78-174">Sie können auch den **Max** -Qualifizierer verwenden, um die Größe eines Arrays anzugeben.</span><span class="sxs-lookup"><span data-stu-id="42e78-174">You can also use the **Max** qualifier to specify the size of an array.</span></span> <span data-ttu-id="42e78-175">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42e78-175">For example:</span></span>

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

<span data-ttu-id="42e78-176">Wenn Sie die Größe des Arrays in die eckigen Klammern einschließen, generiert der MOF-Compiler den maximalen Qualifizierer für Sie.</span><span class="sxs-lookup"><span data-stu-id="42e78-176">If you include the size of the array in the square brackets, the MOF compiler generates the Max qualifier for you.</span></span>

<span data-ttu-id="42e78-177">Es ist wichtig, dass Sie für jede Eigenschaft den **Beschreibungs** Qualifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e78-177">It is important that you use the **Description** qualifier for each property.</span></span> <span data-ttu-id="42e78-178">Die Beschreibung sollte einen anzeigen Amen enthalten, der vom Consumer beim Anzeigen der Eigenschaftswerte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="42e78-178">The description should contain a display name that the consumer can use when displaying the property values.</span></span>

<span data-ttu-id="42e78-179">Das folgende Beispiel zeigt den Inhalt einer MOF-Datei, die einen Anbieter, ein Ereignis und eine MOF-Klasse für den Ereignistyp beschreibt.</span><span class="sxs-lookup"><span data-stu-id="42e78-179">The following example shows the contents of a MOF file that describes a provider, event, and event type MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

<span data-ttu-id="42e78-180">Beachten Sie, dass die MOF-Klassennamen des Anbieters, des Ereignisses und des Ereignis Typs innerhalb des gesamten Namespace eindeutig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="42e78-180">Note that the provider, event, and event type MOF class names must be unique within the entire namespace.</span></span> <span data-ttu-id="42e78-181">Um Benennungs Konflikte zu vermeiden, sollten Sie einen eindeutigen und beschreibenden Namen für alle Klassennamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e78-181">To avoid naming conflicts, you should use unique and descriptive name for all class names.</span></span> <span data-ttu-id="42e78-182">Klasseneigenschaften sollten außerdem beschreibend und innerhalb der Klassenhierarchie eindeutig sein – eine untergeordnete Klasse, die denselben Eigenschaftsnamen wie eine übergeordnete Klasse enthält, überschreibt die-Eigenschaft der übergeordneten Klasse.</span><span class="sxs-lookup"><span data-stu-id="42e78-182">Class properties should also be descriptive and unique within its class hierarchy—a child class that contains the same property name as a parent class overwrites the property of the parent class.</span></span>

<span data-ttu-id="42e78-183">Nachdem Sie Ihre MOF-Klassen definiert haben, verwenden Sie den MOF-Compiler, um das Ereignis Schema zu generieren und es dem CIM-Repository hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="42e78-183">After defining your MOF classes, use the MOF compiler to generate your event schema and add it to the CIM repository.</span></span> <span data-ttu-id="42e78-184">Consumer können dann das Schema aus dem Repository lesen und die Ereignisdaten Programm gesteuert lesen.</span><span class="sxs-lookup"><span data-stu-id="42e78-184">Consumers can then read the schema from the repository and programmatically read the event data.</span></span> <span data-ttu-id="42e78-185">Eine umfassende Beschreibung der MOF-Syntax und die Verwendung des MOF-Compilers (Mofcomp.exe) zum Hinzufügen der MOF-Klassen zum CIM-Repository finden Sie unter [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="42e78-185">For a complete description of the MOF syntax and using the MOF compiler (Mofcomp.exe) to add your MOF classes to the CIM repository, see [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span></span> <span data-ttu-id="42e78-186">Informationen zum Verwenden von Wbemtest.exe für den Zugriff auf das CIM-Repository finden Sie unter [Windows-Verwaltungsinstrumentation](../wmisdk/wmi-start-page.md) (WMI).</span><span class="sxs-lookup"><span data-stu-id="42e78-186">For information on using Wbemtest.exe to access the CIM repository, see [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).</span></span>

## <a name="versioning-mof-class"></a><span data-ttu-id="42e78-187">Versionierung der MOF-Klasse</span><span class="sxs-lookup"><span data-stu-id="42e78-187">Versioning MOF class</span></span>

<span data-ttu-id="42e78-188">Wenn Sie eine MOF-Klasse für den Ereignistyp hinzufügen oder ändern, besteht die Konvention darin, sowohl die MOF-Ereignisklasse als auch die MOF-Klassen des untergeordneten Ereignis Typs zu Version</span><span class="sxs-lookup"><span data-stu-id="42e78-188">If you add or change an event type MOF class, the convention is to version both the event MOF class and its child event type MOF classes.</span></span> <span data-ttu-id="42e78-189">Um die MOF-Klasse des aktuellen Ereignisses zu versionenden, fügen \_ Sie VN an den Klassennamen an, wobei n eine inkrementelle Zahl ist, beginnend bei 0</span><span class="sxs-lookup"><span data-stu-id="42e78-189">To version the current event MOF class, append \_Vn to the class name, where n is an incremental number starting at 0.</span></span> <span data-ttu-id="42e78-190">Wenn dies die erste Revision der-Klasse ist, fügen \_ Sie v0 an den Klassennamen an.</span><span class="sxs-lookup"><span data-stu-id="42e78-190">If this is the first revision to the class, append \_V0 to the class name.</span></span> <span data-ttu-id="42e78-191">Außerdem müssen Sie der-Klasse den **eventversion** -Qualifizierer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="42e78-191">You must also add the **EventVersion** qualifier to the class.</span></span> <span data-ttu-id="42e78-192">Verwenden Sie die gleiche Versionsnummer, die Sie im Klassennamen verwendet haben, für den Wert des **eventversion** -Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="42e78-192">Use the same version number you used in the class name for the value of the **EventVersion** qualifier.</span></span>

<span data-ttu-id="42e78-193">Die neue Version der MOF-Ereignisklasse muss denselben Namen und **GUID** -Qualifizierer wie die ursprüngliche Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e78-193">The new version of the event MOF class must use the same name and **Guid** qualifier as the original class.</span></span> <span data-ttu-id="42e78-194">Die neue Klasse kann optional den **eventversion** -Qualifizierer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="42e78-194">The new class may optionally add the **EventVersion** qualifier.</span></span> <span data-ttu-id="42e78-195">Die MOF-Ereignisklasse, die nicht den **eventversion** -Qualifizierer enthält, wird als neueste Version betrachtet, oder wenn alle Versionen der Klasse einen **eventversion** -Qualifizierer enthalten, wird die Klasse mit der höchsten Versionsnummer als die neueste Version betrachtet.</span><span class="sxs-lookup"><span data-stu-id="42e78-195">The event MOF class that does not contain the **EventVersion** qualifier is considered the latest version, or if all the versions of the class contain an **EventVersion** qualifier, then the class with the highest version number is considered the latest version.</span></span> <span data-ttu-id="42e78-196">Der Anbieter verwendet den **Class. Version** -Member der [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur, um die Version des Ereignisses zu identifizieren, das in der Ablauf Verfolgung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="42e78-196">The provider uses the **Class.Version** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to identify the version of the event included in the trace.</span></span>

<span data-ttu-id="42e78-197">Im folgenden Beispiel wird gezeigt, wie eine MOF-Ereignisklasse in einer Version Versions</span><span class="sxs-lookup"><span data-stu-id="42e78-197">The following example shows how to version an event MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 
