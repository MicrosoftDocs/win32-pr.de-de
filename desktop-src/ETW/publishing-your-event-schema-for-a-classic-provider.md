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
# <a name="publishing-your-event-schema-for-a-classic-provider"></a>Veröffentlichen Ihres Ereignis Schemas für einen klassischen Anbieter

[Klassische](about-event-tracing.md) Anbieter sollten [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) verwenden, um das Layout Ihrer Ereignisdaten zu veröffentlichen. Consumer können das veröffentlichte Layout dann zur Laufzeit aus WMI lesen und zum Lesen der Ereignisdaten verwenden.

Wenn Sie MOF verwenden, um das Layout der Ereignisdaten in WMI zu veröffentlichen, erstellen Sie in der Regel die folgenden drei Typen von MOF-Klassen im Stamm- \\ WMI-Namespace:

-   [Eine MOF-Anbieter Klasse](#provider-mof-classes)
-   [Mindestens eine MOF-Ereignisklasse](#event-mof-classes)
-   [Mindestens eine MOF-Klasse für den Ereignistyp.](#event-type-mof-classes)

## <a name="provider-mof-classes"></a>MOF-Anbieter Klassen

Wenn Sie das Layout der Ereignisdaten veröffentlichen, müssen Sie eine MOF-Klasse erstellen, die Ihren Anbieter identifiziert. Diese Klasse muss von der **EventTrace** MOF-Klasse abgeleitet werden und muss leer sein (keine Eigenschaften oder Methoden). Die Klasse muss auch den **GUID** -Qualifizierer enthalten, der den Anbieter eindeutig identifiziert. Dies ist dieselbe GUID, die Sie verwenden, wenn Sie die [**registertraceguids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) -Funktion aufrufen, um den Anbieter zu registrieren.

## <a name="event-mof-classes"></a>MOF-Ereignis Klassen

Eine MOF-Ereignisklasse definiert eine Klasse von Ereignissen, die der Anbieter bereitstellt. Diese Klasse wird von der MOF-Klasse des Anbieters abgeleitet und muss leer sein (keine Eigenschaften oder Methoden). Die Klasse muss auch den **GUID** -Qualifizierer enthalten, der die Klasse der Ereignisse eindeutig identifiziert, die von den untergeordneten Klassen definiert werden. Der Anbieter verwendet dieselbe GUID, wenn der **GUID** -Member der Ereignis-Ablauf [**\_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur festgelegt wird.

## <a name="event-type-mof-classes"></a>MOF-Ereignistyp Klassen

Eine MOF-Klasse für den Ereignistyp definiert die tatsächlichen Ereignisdaten. Diese Klasse wird von der übergeordneten Ereignis-MOF-Klasse abgeleitet. Wenn Sie die MOF-Klasse für den Ereignistyp benennen, besteht die Konvention darin, den MOF-Ereignis Klassennamen am Anfang des MOF-Klassen namens des Ereignis Typs zu verwenden. Wenn z. b. der MOF-Klassenname des Ereignisses hwconfig ist und die MOF-Klasse des Ereignis Typs CPU-Informationen darstellt, sollten Sie den Ereignistyp MOF Class, hwconfig CPU, benennen \_ .

Verwenden Sie den **eventType** -Qualifizierer für die MOF-Ereignisklasse, um den Ereignistyp zu identifizieren. Wenn mehrere Ereignis Typen dieselben Ereignisdaten verwenden, können Sie dieselbe MOF-Klasse verwenden. Der Anbieter verwendet den gleichen Ereignistyp Wert, um das Ereignis zu identifizieren, wenn der **Class. Type** -Member der Ereignis-Ablauf [**\_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur festgelegt wird.

Die MOF-Ereignistyp Klasse enthält Eigenschaften. Die Reihenfolge dieser Eigenschaften definiert das Layout der Ereignisdaten. In der folgenden Tabelle sind die Datentypen und Qualifizierer aufgeführt, die Sie zum Definieren der Eigenschaften verwenden können. Weitere Informationen zu den Eigenschaften und Klassen Qualifizierern, die Sie verwenden können, finden Sie unter [Ereignis Ablauf Verfolgung MOF-Qualifizierer](event-tracing-mof-qualifiers.md).



| Datentyp              | Qualifizierer                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**, **Uint8**   | **Format**                        | Deklariert eine 1-Byte-Ganzzahl mit Dezimalzahlen. Verwenden Sie zum Deklarieren eines ANSI-Zeichens den **Format** Qualifizierer, und legen Sie dessen Wert auf "c" fest.                                                                                                                                                                                                  |
| **sint16**, **UInt16** | **Format**                        | Deklariert eine ganzzahlige 2-Byte-Ganzzahl. Um anzugeben, dass die Zahl eine hexadezimale Zahl ist, verwenden Sie den **Format** Qualifizierer. Beispiel: Format ("x").                                                                                                                                                                               |
| **sint32**, **UInt32** | **Format**                        | Deklariert eine ganze 4-Byte-Ganzzahl. Um anzugeben, dass die Zahl eine hexadezimale Zahl ist, verwenden Sie den **Format** Qualifizierer, und legen Sie dessen Wert auf "x" fest.                                                                                                                                                                                |
| **sint64**, **UInt64** | **Format**                        | Deklariert eine 8-Byte-Ganzzahl mit Dezimalzahlen. Um anzugeben, dass die Zahl eine hexadezimale Zahl ist, verwenden Sie den **Format** Qualifizierer, und legen Sie dessen Wert auf "x" fest.                                                                                                                                                                                |
| **boolean**            |                                   | Deklariert einen booleschen Wert. Der Ereignisconsumer sollte den Wert als bool (4-Byte-Ganzzahl) interpretieren.                                                                                                                                                                                                                        |
| **char16**             |                                   | Deklariert ein breit Zeichen. Der Ereignisconsumer sollte char16 Arrays in Kernel Ereignissen als breit Zeichen-Zeichen folgen interpretieren. (Verwenden Sie die Array Größe, um die Zeichenfolge zu kopieren. Einige Zeichen folgen können führende Null-Zeichen enthalten.)                                                                                                      |
| **object**             | **Erweiterung**                     | Deklariert ein binäres Blob. Der **Erweiterungs** Qualifizierer gibt den Typ der Daten im BLOB an.                                                                                                                                                                                                                              |
| **string**             | **Format**, **stringbeendigung** | Deklariert einen Zeichen folgen Wert. Um anzugeben, dass die Zeichenfolge eine Zeichenfolge mit breit Zeichen ist, verwenden Sie den **Format** Qualifizierer und legen den Wert auf "w" fest. Die Zeichenfolge wird als ANSI-Zeichenfolge betrachtet, wenn Sie nicht den **Format** Qualifizierer angeben. Um anzugeben, wie die Zeichenfolge beendet wird, verwenden Sie den **stringbeendigung** -Qualifizierer. <br/> |



 

Zum Angeben eines Arrays können Sie eckige Klammern () verwenden \[ \] . Die eckigen Klammern können die Größe des Arrays einschließen. Beispiel:

`[WmiDataId(1), read] uint8 MyGuid[16];`

Sie können auch den **Max** -Qualifizierer verwenden, um die Größe eines Arrays anzugeben. Beispiel:

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

Wenn Sie die Größe des Arrays in die eckigen Klammern einschließen, generiert der MOF-Compiler den maximalen Qualifizierer für Sie.

Es ist wichtig, dass Sie für jede Eigenschaft den **Beschreibungs** Qualifizierer verwenden. Die Beschreibung sollte einen anzeigen Amen enthalten, der vom Consumer beim Anzeigen der Eigenschaftswerte verwendet werden kann.

Das folgende Beispiel zeigt den Inhalt einer MOF-Datei, die einen Anbieter, ein Ereignis und eine MOF-Klasse für den Ereignistyp beschreibt.

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

Beachten Sie, dass die MOF-Klassennamen des Anbieters, des Ereignisses und des Ereignis Typs innerhalb des gesamten Namespace eindeutig sein müssen. Um Benennungs Konflikte zu vermeiden, sollten Sie einen eindeutigen und beschreibenden Namen für alle Klassennamen verwenden. Klasseneigenschaften sollten außerdem beschreibend und innerhalb der Klassenhierarchie eindeutig sein – eine untergeordnete Klasse, die denselben Eigenschaftsnamen wie eine übergeordnete Klasse enthält, überschreibt die-Eigenschaft der übergeordneten Klasse.

Nachdem Sie Ihre MOF-Klassen definiert haben, verwenden Sie den MOF-Compiler, um das Ereignis Schema zu generieren und es dem CIM-Repository hinzuzufügen. Consumer können dann das Schema aus dem Repository lesen und die Ereignisdaten Programm gesteuert lesen. Eine umfassende Beschreibung der MOF-Syntax und die Verwendung des MOF-Compilers (Mofcomp.exe) zum Hinzufügen der MOF-Klassen zum CIM-Repository finden Sie unter [Managed Object Format](../wmisdk/managed-object-format--mof-.md). Informationen zum Verwenden von Wbemtest.exe für den Zugriff auf das CIM-Repository finden Sie unter [Windows-Verwaltungsinstrumentation](../wmisdk/wmi-start-page.md) (WMI).

## <a name="versioning-mof-class"></a>Versionierung der MOF-Klasse

Wenn Sie eine MOF-Klasse für den Ereignistyp hinzufügen oder ändern, besteht die Konvention darin, sowohl die MOF-Ereignisklasse als auch die MOF-Klassen des untergeordneten Ereignis Typs zu Version Um die MOF-Klasse des aktuellen Ereignisses zu versionenden, fügen \_ Sie VN an den Klassennamen an, wobei n eine inkrementelle Zahl ist, beginnend bei 0 Wenn dies die erste Revision der-Klasse ist, fügen \_ Sie v0 an den Klassennamen an. Außerdem müssen Sie der-Klasse den **eventversion** -Qualifizierer hinzufügen. Verwenden Sie die gleiche Versionsnummer, die Sie im Klassennamen verwendet haben, für den Wert des **eventversion** -Qualifizierers.

Die neue Version der MOF-Ereignisklasse muss denselben Namen und **GUID** -Qualifizierer wie die ursprüngliche Klasse verwenden. Die neue Klasse kann optional den **eventversion** -Qualifizierer hinzufügen. Die MOF-Ereignisklasse, die nicht den **eventversion** -Qualifizierer enthält, wird als neueste Version betrachtet, oder wenn alle Versionen der Klasse einen **eventversion** -Qualifizierer enthalten, wird die Klasse mit der höchsten Versionsnummer als die neueste Version betrachtet. Der Anbieter verwendet den **Class. Version** -Member der [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur, um die Version des Ereignisses zu identifizieren, das in der Ablauf Verfolgung enthalten ist.

Im folgenden Beispiel wird gezeigt, wie eine MOF-Ereignisklasse in einer Version Versions

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

 

 
