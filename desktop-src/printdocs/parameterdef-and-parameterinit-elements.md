---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter "Print Schema Specification".
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: ParameterDef-und parameterinit-Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e71ed86d627072ee4b5b0ca0acb4e068ae62b6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354924"
---
# <a name="parameterdef-and-parameterinit-elements"></a>ParameterDef-und parameterinit-Elemente

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein ParameterDef-Element unterscheidet sich von einem parameterinit-Element darin, dass es den Wert beschreibt, den ein parameterinit-Element enthalten kann, während ein parameterinit-Element dem-Parameter einen Wert zuweist. Ein ParameterDef-Element besteht aus einem bestimmten Satz von Eigenschafts Elementen, bei denen es sich um untergeordnete Elemente des ParameterDef-Elements handelt, die den Typ der Daten, die maximalen, minimalen und Standardwerte für die Daten und andere Informationen angeben. Diese Eigenschaften Elemente werden weiter unten in diesem Thema erläutert.

ParameterDef-Elemente können nur in Ihrem zulässigen Kontext angezeigt werden. Für die anfängliche Version des Druck Schemas befinden sich diese möglicherweise auf der Stamm Ebene des Dokuments printfunktionen. Das Name-Attribut des ParameterDef-Elements definiert den Parameternamen. Jedem ParameterDef-Element im printfunktionalitäten-Dokument muss ein eindeutiges Namensattribut zugewiesen werden.

> [!Note]
> So drucken Sie Funktionen von Dokument Anbietern:
> 
> Die Bedeutung eines Parameter namens ist universell. Das heißt, wenn ein ParameterDef-Element in einem printfunktionalitäten-Dokument das gleiche Namensattribut hat (die aus dem Namespace und dem beschreibenden Namen des ParameterDef-Elements gebildete Zeichenfolge), wird davon ausgegangen, dass beide Elemente dasselbe Konzept darstellen und auf die gleiche Weise interpretiert werden sollten. Daher kann ein ParameterDef-Element, das in einem PrintTicket für ein Printworks-Dokument definiert ist, verwendet werden, um das parameterinit-Element mit demselben Namen zu initialisieren, der in einem anderen Printworks-Dokument definiert ist.

 

## <a name="relationship-to-xml-attributes"></a>Beziehung zu XML-Attributen

Wie bei allen namens Attributen hat der Parameter Name die Form eines XML-QName. Ein Schema definiertes Parameter Konstrukt weist einen Namen auf, der durch den öffentlichen Namespace qualifiziert wird und das Name-Attribut bildet, während das Name-Attribut eines privat definierten Parameter Konstrukts durch einen privaten Namespace qualifiziert wird, der für den Ersteller eindeutig ist.

## <a name="relationship-between-parameterdef-and-property-element-types"></a>Beziehung zwischen ParameterDef-und Property-Element Typen

ParameterDef-Elemente, die in den Schlüsselwörtern des Druck Schemas definiert sind, müssen in einem Printworks-Dokument vollständig definiert sein. Das Dokument mit den Schlüsselwörtern für den Druck Schema stellt nominale Werte für einige Eigenschafts Elemente eines ParameterDef-Elements (z. b. DefaultValue und andere) bereit, aber der Autor eines PrintValues-Dokuments ist für das Definieren der restlichen Eigenschafts Elemente verantwortlich. In jedem Fall müssen alle Eigenschafts Elemente explizit in einem ParameterDef-Element definiert werden, einschließlich derjenigen, die in den Schlüsselwörtern des Druck Schemas definiert sind.

Bestimmte Eigenschaften Elemente der einzelnen ParameterDef-Elemente, die in den Schlüsselwörtern des Druck Schemas angezeigt werden, werden als *unveränderlich* festgelegt. Dies bedeutet, dass alle Dokument Definitionen von Print-Schema Schlüsselwörtern definierte ParameterDef-Elemente diese Eigenschafts Elemente unverändert beibehalten müssen. Diese unveränderlichen Eigenschafts Elemente ermöglichen es, dass die Parameterkonstrukte über alle Printworks-Dokumente portabel und eindeutig sind. Ein gutes Beispiel hierfür sind die in einem ParameterDef-Element verwendeten Einheiten. Diese Einheiten sollten unveränderlich sein, um ein konsistentes Verständnis ihrer Bedeutung zu fördern. Eigenschaften Elemente eines ParameterDef, die als nicht unveränderlich festgelegt sind, können in einem printfunktionalitäten-Dokument neu definiert werden.

Ein ParameterDef-Element besteht aus den folgenden Eigenschaften Elementen. Alle müssen vorhanden sein, sofern nicht anders angegeben.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaftsname</th>
<th>Werte</th>
<th>BESCHREIBUNG</th>
<th>Unveränderliche?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DataType <br/></td>
<td>integer <br/> Decimal<br/> Zeichenfolge<br/> Für dieses Feld gibt es keinen Standardwert.<br/></td>
<td>Gibt an, ob der Parameterwert eine ganze Zahl, eine Gleit Komma Zahl oder eine Text Zeichenfolge ist. Der Wert eines Parameters wird im gleichen Format wie der entsprechende XSD-Grund Datentyp ausgedrückt. Das heißt, als ganze Zahl, Dezimalzahl oder Zeichenfolge. <br/></td>
<td>Ja<br/></td>
</tr>
<tr class="even">
<td>DefaultValue <br/></td>
<td>Der durch die DataType-Eigenschaft angegebene Typ.<br/> Für dieses Feld gibt es keinen Standardwert.<br/></td>
<td>Gibt den Wert an, mit dem ein Benutzeroberflächen Steuerelement (UI) initialisiert werden soll.<br/>
<ul>
<li>oder <br/></li>
</ul>
Gibt den Wert an, der verwendet werden soll, wenn das relevante Parameter Element in PrintTicket fehlt.<br/></td>
<td>Nein<br/></td>
</tr>
<tr class="odd">
<td>Obligatorisch. <br/></td>
<td>Bedingungs bedingt: das parameterinit-Element muss immer angegeben werden. <br/> Conditional: das parameterinit-Element ist nur erforderlich, wenn innerhalb eines Option-Elements in einem PrintTicket auf den Parameter verwiesen wird.<br/> DefaultValue: bedingt.<br/></td>
<td>Gibt an, dass ein parameterinit-Element explizit angezeigt werden muss. Wenn der Wert bedingt ist, muss der parameterinit initialisiert werden, wenn das PrintTicket eine Option enthält, die auf den Parameter verweist.<br/> Wird von UI-Clients und Print-Funktionen oder PrintTicket-Anbietern verwendet. Beachten Sie, dass die obligatorische-Eigenschaft des ParameterDef-Elements in jeder Einschränkung auf bedingungslos festgelegt werden muss. Der ParameterDef muss über einen definierten Wert verfügen. andernfalls konnte der abhängige Wert oder die Einschränkung nicht ausgewertet werden.<br/></td>
<td>Nein<br/></td>
</tr>
<tr class="even">
<td>MaxLength <br/></td>
<td>Integer, wenn die DataType-Eigenschaft eine Zeichenfolge angibt.<br/> DefaultValue: Es wird kein maximaler Wert erzwungen.<br/></td>
<td>Gibt für Zeichen folgen Wert Parameter die längste zulässige Zeichenfolge an. Benutzeroberflächen-und PrintService-Anbieter verwenden diese Eigenschaft, um das ParameterDef-Element zu validieren.<br/></td>
<td>Nein<br/></td>
</tr>
<tr class="odd">
<td>MaxValue <br/></td>
<td>Integer, wenn die DataType-Eigenschaft eine ganze Zahl angibt.<br/> Decimal, wenn die DataType-Eigenschaft Decimal angibt.<br/> DefaultValue: Es wird kein maximaler Wert erzwungen.<br/></td>
<td>Definiert bei ganzzahligen oder Dezimal wertigen ParameterDef-Elementen den größten zulässigen Wert.<br/></td>
<td>Nein<br/></td>
</tr>
<tr class="even">
<td>MinLength <br/></td>
<td>Integer, wenn die DataType-Eigenschaft eine Zeichenfolge angibt. <br/> DefaultValue: Es wird kein Minimalwert erzwungen.<br/></td>
<td>Definiert für Zeichen folgen Werte die kürzeste zulässige Zeichenfolge. Benutzeroberflächen-und PrintService-Anbieter verwenden diese Eigenschaft, um das ParameterDef-Element zu validieren.<br/></td>
<td>Nein<br/></td>
</tr>
<tr class="odd">
<td>MinValue <br/></td>
<td>Integer, wenn die DataType-Eigenschaft eine ganze Zahl angibt.<br/> Decimal, wenn die DataType-Eigenschaft Decimal angibt.<br/> DefaultValue: Es wird kein Minimalwert erzwungen.<br/></td>
<td>Definiert bei ganzzahligen oder Dezimalwert Parametern den kleinsten zulässigen Wert. <br/></td>
<td>Nein<br/></td>
</tr>
<tr class="even">
<td>Mehrere <br/></td>
<td>Integer, wenn die DataType-Eigenschaft eine ganze Zahl angibt.<br/> Decimal, wenn die DataType-Eigenschaft Decimal angibt.<br/> DefaultValue: 1<br/></td>
<td>Bei ganzzahligen oder Dezimalwert Parametern sollte der Wert des-Parameters ein Vielfaches dieser Zahl sein. Weitere Informationen finden Sie <a href="#notes-on-multiple">in den Hinweisen zu mehreren Informationen in der</a> folgenden Tabelle.<br/></td>
<td>Nein<br/></td>
</tr>
<tr class="odd">
<td>UnitType <br/></td>
<td>ein Zeichen folgen Wert, der die für den Parameter verwendeten Einheiten angibt.<br/> Für dieses Feld gibt es keinen Standardwert.<br/></td>
<td>Gibt die Einheiten an, in denen der-Parameter ausgedrückt wird. Beispielsweise Winkel in Zehntel Graden, Längen in Mikrometern usw.<br/></td>
<td>Ja<br/></td>
</tr>
</tbody>
</table>



 

## <a name="notes-on-multiple"></a>Hinweise zu mehreren

Für parameterinit-Elemente mit ganzzahligen oder Dezimalwerten sollte der Wert von parameterinit ein Vielfaches dieser Zahl sein. Beispielsweise können parameterinit-Elemente mit Dezimalwert auf Zehntel Werte beschränkt werden, indem diese Eigenschaft auf 0,1 festgelegt wird. Benutzeroberflächen Elemente verwenden diese Eigenschaft, wenn Sie Dialoge und UI-Steuerelemente erstellen. Außerdem kann der PrintTicket-Validierungscode diese Eigenschaft verwenden, um den Wert einer parameterinit auf den nächstgelegenen Wert zu runden, der durch multiple angegeben wird. Hinweis: Gerätetreiber und printfunktionalitäten-Anbieter sollten nicht davon ausgehen, dass parameterinit-Werte vielfache dieses Eigenschafts Werts sind. Jeder Anbieter muss in der Lage sein, beliebige Werte auf den nächstgelegenen nutzbaren Wert zu runden, da verschiedene Anbieter unterschiedliche und widersprüchliche Werte für diese Eigenschaft angeben können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




