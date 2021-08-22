---
description: Klassische Anbieter sollten Managed Object Format (MOF) verwenden, um das Layout ihrer Ereignisdaten zu veröffentlichen. Consumer können dann das veröffentlichte Layout zur Laufzeit aus WMI lesen und zum Lesen der Ereignisdaten verwenden.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Veröffentlichen des Ereignisschemas für einen klassischen Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e2e9b940df5afd6e8070e9235fe40566ef2b6d2b31b3c14656756835bab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069820"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a>Veröffentlichen des Ereignisschemas für einen klassischen Anbieter

[Klassische](about-event-tracing.md) Anbieter sollten [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) verwenden, um das Layout ihrer Ereignisdaten zu veröffentlichen. Consumer können dann das veröffentlichte Layout zur Laufzeit aus WMI lesen und zum Lesen der Ereignisdaten verwenden.

Wenn Sie MOF verwenden, um das Layout Ihrer Ereignisdaten in WMI zu veröffentlichen, erstellen Sie in der Regel die folgenden drei Typen von MOF-Klassen im \\ wmi-Stammnamespace:

-   [Eine MOF-Anbieterklasse](#provider-mof-classes)
-   [Eine oder mehrere MOF-Ereignisklassen](#event-mof-classes)
-   [Eine oder mehrere MOF-Ereignistypklassen](#event-type-mof-classes)

## <a name="provider-mof-classes"></a>MOF-Anbieterklassen

Wenn Sie das Layout Ihrer Ereignisdaten veröffentlichen, müssen Sie eine MOF-Klasse erstellen, die Ihren Anbieter identifiziert. Diese Klasse muss von der **EventTrace** MOF-Klasse abgeleitet sein und leer sein (keine Eigenschaften oder Methoden). Die -Klasse muss  auch den GUID-Qualifizierer enthalten, der den Anbieter eindeutig identifiziert. Dies ist die gleiche GUID, die Sie beim Aufrufen der [**RegisterTraceGuids-Funktion**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) zum Registrieren Ihres Anbieters verwenden.

## <a name="event-mof-classes"></a>MOF-Ereignisklassen

Eine MOF-Ereignisklasse definiert eine Klasse von Ereignissen, die der Anbieter bereitstellt. Diese Klasse wird von der MOF-Anbieterklasse abgeleitet und muss leer sein (keine Eigenschaften oder Methoden). Die -Klasse muss  auch den GUID-Qualifizierer enthalten, der die Klasse der Ereignisse eindeutig identifiziert, die von den untergeordneten Klassen definiert werden. Der Anbieter verwendet dieselbe GUID, wenn er den **Guid-Member** der [**EVENT TRACE \_ \_ HEADER-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) festlegt.

## <a name="event-type-mof-classes"></a>MOF-Klassen des Ereignistyps

Eine MOF-Ereignisklasse definiert die tatsächlichen Ereignisdaten. Diese Klasse wird von der MOF-Klasse des übergeordneten Ereignisses abgeleitet. Beim Benennen der MOF-Ereignisklasse wird der MOF-Ereignisklassenname am Anfang des MOF-Ereignistypklassennamens verwendet. Wenn der Mof-Ereignisklassenname beispielsweise HWConfig lautet und der Ereignistyp MOF-Klasse CPU-Informationen darstellt, sollten Sie den Ereignistyp MOF-Klasse, HWConfig \_ CPU, benennen.

Verwenden Sie den **EventType-Qualifizierer** für die MOF-Ereignisklasse, um den Ereignistyp zu identifizieren. Wenn mehrere Ereignistypen dieselben Ereignisdaten verwenden, können sie dieselbe MOF-Klasse verwenden. Der Anbieter verwendet den gleichen Ereignistypwert, um das Ereignis beim Festlegen des **Class.Type-Members** der [**EVENT TRACE \_ \_ HEADER-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) zu identifizieren.

Die MOF-Ereignisklasse enthält Eigenschaften. Die Reihenfolge dieser Eigenschaften definiert das Layout der Ereignisdaten. In der folgenden Tabelle sind die Datentypen und Qualifizierer aufgeführt, die Sie zum Definieren der Eigenschaften verwenden können. Weitere Informationen zu den Eigenschaften- und Klassenqualifizierern, die Sie verwenden können, finden Sie unter [MOF-Qualifizierer](event-tracing-mof-qualifiers.md)für die Ereignisablaufverfolgung.



| Datentyp              | Qualifizierer                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**, **uint8**   | **Format**                        | Deklariert eine ganze Dezimalzahl von 1 Byte. Um ein ANSI-Zeichen  zu deklarieren, verwenden Sie den Formatqualifizierer, und legen Sie seinen Wert auf "c" fest.                                                                                                                                                                                                  |
| **sint16**, **uint16** | **Format**                        | Deklariert eine dezimale 2-Byte-Ganzzahl. Um anzugeben, dass die Zahl eine Hexadezimalzahl ist, verwenden Sie den **Formatqualifizierer.** Beispiel: format("x").                                                                                                                                                                               |
| **sint32**, **uint32** | **Format**                        | Deklariert eine ganze 4-Byte-Dezimalzahl. Um anzugeben, dass die Zahl eine Hexadezimalzahl ist, verwenden Sie den **Formatqualifizierer,** und legen Sie seinen Wert auf "x" fest.                                                                                                                                                                                |
| **sint64**, **uint64** | **Format**                        | Deklariert eine dezimale 8-Byte-Ganzzahl. Um anzugeben, dass die Zahl eine Hexadezimalzahl ist, verwenden Sie den **Formatqualifizierer,** und legen Sie seinen Wert auf "x" fest.                                                                                                                                                                                |
| **boolean**            |                                   | Deklariert einen booleschen Wert. Der Ereignisverbraucher sollte den Wert als BOOL (4-Byte-Ganzzahl) interpretieren.                                                                                                                                                                                                                        |
| **char16**             |                                   | Deklariert ein Breitzeichen. Der Ereignisverbraucher sollte char16-Arrays in Kernelereignissen als Breitzeichenfolgen interpretieren. (Verwenden Sie die Arraygröße, um die Zeichenfolge zu kopieren. Einige Zeichenfolgen können führende NULL-Zeichen enthalten.)                                                                                                      |
| **object**             | **Erweiterung**                     | Deklariert ein binäres Blob. Der  Erweiterungsqualifizierer gibt den Typ der Daten im Blob an.                                                                                                                                                                                                                              |
| **string**             | **Format**, **StringTermination** | Deklariert einen Zeichenfolgenwert. Um anzugeben, dass es sich bei  der Zeichenfolge um eine Breitzeichenzeichenfolge handelt, verwenden Sie den Formatqualifizierer, und legen Sie dessen Wert auf "w" fest. Die Zeichenfolge gilt als ANSI-Zeichenfolge, wenn Sie den **Formatqualifizierer** nicht angeben. Verwenden Sie den **StringTermination-Qualifizierer,** um anzugeben, wie die Zeichenfolge beendet wird. <br/> |



 

Um ein Array anzugeben, können Sie eckige Klammern verwenden, \[ \] . Die eckigen Klammern können die Größe des Arrays enthalten. Beispiel:

`[WmiDataId(1), read] uint8 MyGuid[16];`

Sie können auch  den Max-Qualifizierer verwenden, um die Größe eines Arrays anzugeben. Beispiel:

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

Wenn Sie die Größe des Arrays in eckige Klammern einschließen, generiert der MOF-Compiler den Max-Qualifizierer für Sie.

Es ist wichtig, dass Sie den **Description-Qualifizierer** für jede Eigenschaft verwenden. Die Beschreibung sollte einen Anzeigenamen enthalten, den der Consumer beim Anzeigen der Eigenschaftswerte verwenden kann.

Das folgende Beispiel zeigt den Inhalt einer MOF-Datei, die einen Anbieter, ein Ereignis und eine MOF-Ereignisklasse beschreibt.

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

Beachten Sie, dass anbieter-, ereignis- und ereignistyp-MOF-Klassennamen innerhalb des gesamten Namespace eindeutig sein müssen. Um Namenskonflikte zu vermeiden, sollten Sie einen eindeutigen und beschreibenden Namen für alle Klassennamen verwenden. Klasseneigenschaften sollten auch beschreibend und innerhalb ihrer Klassenhierarchie eindeutig sein. Eine untergeordnete Klasse, die den gleichen Eigenschaftennamen wie eine übergeordnete Klasse enthält, überschreibt die -Eigenschaft der übergeordneten Klasse.

Verwenden Sie nach dem Definieren der MOF-Klassen den MOF-Compiler, um das Ereignisschema zu generieren und dem CIM-Repository hinzuzufügen. Consumer können dann das Schema aus dem Repository lesen und die Ereignisdaten programmgesteuert lesen. Eine vollständige Beschreibung der MOF-Syntax und die Verwendung des MOF-Compilers (Mofcomp.exe) zum Hinzufügen Ihrer MOF-Klassen zum CIM-Repository finden Sie unter [Managed Object Format](../wmisdk/managed-object-format--mof-.md). Informationen zur Verwendung von Wbemtest.exe für den Zugriff auf das CIM-Repository finden Sie unter [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).

## <a name="versioning-mof-class"></a>MOF-Versionierungsklasse

Wenn Sie eine MOF-Ereignisklasse hinzufügen oder ändern, besteht die Konvention darin, sowohl die MOF-Ereignisklasse als auch deren untergeordnete MOF-Ereignistypklassen zu versionieren. Fügen Sie Vn an den \_ Klassennamen an, wobei n eine inkrementelle Zahl ist, die bei 0 beginnt, um eine Version der aktuellen MOF-Ereignisklasse zu verwenden. Wenn dies die erste Revision der -Klasse ist, fügen Sie \_ V0 an den Klassennamen an. Sie müssen der Klasse auch den **EventVersion-Qualifizierer** hinzufügen. Verwenden Sie dieselbe Versionsnummer, die Sie im Klassennamen für den Wert des **EventVersion-Qualifizierers** verwendet haben.

Die neue Version der MOF-Ereignisklasse muss  den gleichen Namen und guid-Qualifizierer wie die ursprüngliche Klasse verwenden. Die neue Klasse kann optional den **EventVersion-Qualifizierer** hinzufügen. Die MOF-Ereignisklasse, die den **EventVersion-Qualifizierer** nicht enthält, wird als neueste Version betrachtet, oder wenn alle Versionen der Klasse einen **EventVersion-Qualifizierer** enthalten, wird die Klasse mit der höchsten Versionsnummer als neueste Version betrachtet. Der Anbieter verwendet den **Class.Version-Member** der [**EVENT TRACE \_ \_ HEADER-Struktur,**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) um die Version des Ereignisses zu identifizieren, das in der Ablaufverfolgung enthalten ist.

Das folgende Beispiel zeigt, wie sie eine MOF-Ereignisklasse versionen.

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

 

 
