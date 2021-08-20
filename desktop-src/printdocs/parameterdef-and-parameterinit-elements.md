---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: ParameterDef- und ParameterInit-Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa945ad7fec484828bd81b2052f9b330d0e1679
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475126"
---
# <a name="parameterdef-and-parameterinit-elements"></a>ParameterDef- und ParameterInit-Elemente

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein ParameterDef-Element unterscheidet sich von einem ParameterInit-Element, da es den Wert beschreibt, den ein ParameterInit-Element enthalten kann, während ein ParameterInit-Element dem Parameter einen Wert zuteilt. Ein ParameterDef-Element besteht aus einem bestimmten Satz von Property-Elementen, die dem ParameterDef-Element untergestellt sind und den Datentyp, den Höchst-, Minimal- und Standardwert für die Daten sowie weitere Informationen angeben. Diese Property-Elemente werden weiter oben in diesem Thema erläutert.

ParameterDef-Elemente können nur in ihrem zulässigen Kontext angezeigt werden. Für die erste Version des Druckschemas befinden sie sich möglicherweise auf der Stammebene des PrintCapabilities-Dokuments. Das Name-Attribut des ParameterDef-Elements definiert den Parameternamen. Jedem ParameterDef-Element im PrintCapabilities-Dokument muss ein eindeutiges Namensattribut zugewiesen werden.

> [!Note]
> zum Drucken von Funktionen – Dokumentanbieter:
> 
> Die Bedeutung eines Parameternamens ist universell. Das heißt, wenn ein ParameterDef-Element in einem PrintCapabilities-Dokument das gleiche Namensattribut (die aus dem Namespace und dem beschreibenden Namen des ParametersDef-Elements gebildete Zeichenfolge) als ParameterDef-Element in einem anderen PrintCapabilities-Dokument hat, wird angenommen, dass beide Elemente das gleiche Konzept darstellen und auf die gleiche Weise interpretiert werden sollten. Daher kann ein ParameterDef-Element, das in einem PrintTicket für ein PrintCapabilities-Dokument definiert ist, verwendet werden, um das ParameterInit-Element mit demselben Namen zu initialisieren, das in einem anderen PrintCapabilities-Dokument definiert ist.

 

## <a name="relationship-to-xml-attributes"></a>Beziehung zu XML-Attributen

Wie bei allen Namensattributen hat der Parametername die Form eines XML-QName. Ein schemadefiniertes Parameterkonstrukt verfügt über einen Namen, der durch den öffentlichen Namespace qualifiziert wird und das Namensattribut bildet, während das Name-Attribut eines privat definierten Parameterkonstrukts durch einen privaten Namespace qualifiziert wird, der für den Ersteller eindeutig ist.

## <a name="relationship-between-parameterdef-and-property-element-types"></a>Beziehung zwischen ParameterDef- und Property-Elementtypen

ParameterDef-Elemente, die in den Print Schema Keywords definiert sind, müssen vollständig in einem PrintCapabilities-Dokument definiert werden. Das Dokument Print Schema Keywords (Druckschemaschlüsselwörter) enthält nominale Werte für einige Property-Elemente eines ParameterDef-Elements (z. B. DefaultValue und andere), aber der Autor eines PrintCapabilities-Dokuments ist für das Definieren der verbleibenden Property-Elemente verantwortlich. In jedem Fall müssen alle Property-Elemente explizit in einem ParameterDef-Element definiert werden, einschließlich der elemente, die in den Schlüsselwörtern für Druckschemas definiert sind.

Bestimmte Property-Elemente der einzelnen ParameterDef-Elemente, die in den Druckschemaschlüsselwörtern angezeigt werden, werden *als unveränderlich festgelegt.* Dies bedeutet, dass alle PrintCapabilities-Dokumentdefinitionen von ParameterDef-Elementen, die mit "Print Schema Keywords" definiert sind, diese Property-Elemente ohne Änderungen beibehalten müssen. Diese unveränderlichen Property-Elemente ermöglichen es, dass die Parameterkonstrukte in allen PrintCapabilities-Dokumenten portierbar und eindeutig sind. Ein Primbeispiel sind die Einheiten, die in einem ParameterDef-Element verwendet werden. Diese Einheiten sollten unveränderlich sein, um ein konsistentes Verständnis ihrer Bedeutung zu fördern. Eigenschaftselemente einer ParameterDef, die als nicht unveränderlich festgelegt sind, können innerhalb eines PrintCapabilities-Dokuments neu definiert werden.

Ein ParameterDef-Element besteht aus den folgenden Property-Elementen. Alle müssen vorhanden sein, sofern nicht anders angegeben.




| Eigenschaftsname | Werte | BESCHREIBUNG | Unveränderlich? | 
|---------------|--------|-------------|------------|
| DataType <br /> | integer <br /> Decimal<br /> Zeichenfolge<br /> Für dieses Feld gibt es keinen Standardwert.<br /> | Gibt an, ob der Parameterwert eine ganze Zahl, eine Gleitkommazahl oder eine Textzeichenfolge ist. Der Wert eines Parameters wird im gleichen Format wie der entsprechende XSD-Basisdatentyp ausgedrückt. das heißt, als ganze Zahl, Dezimalzahl oder Zeichenfolge. <br /> | Ja<br /> | 
| DefaultValue <br /> | Der von der DataType-Eigenschaft angegebene Typ.<br /> Für dieses Feld gibt es keinen Standardwert.<br /> | Gibt den Wert an, mit dem ein Ui-Steuerelement initialisiert werden soll.<br /><ul><li>oder <br /></li></ul>Gibt den Wert an, der verwendet werden soll, wenn das relevante Parameterelement im PrintTicket fehlt.<br /> | Nein<br /> | 
| Obligatorisch. <br /> | Bedingungslos: Das ParameterInit-Element muss immer angegeben werden. <br /> Bedingt: Das ParameterInit-Element ist nur erforderlich, wenn in einem Option-Element in einem PrintTicket auf den Parameter verwiesen wird.<br /> DefaultValue: Bedingt.<br /> | Gibt an, wenn ein ParameterInit-Element explizit angezeigt werden muss. Bei Bedingt muss ParameterInit initialisiert werden, wenn PrintTicket eine Option enthält, die auf den Parameter verweist.<br /> Wird von Benutzeroberflächenclients und PrintCapabilities- oder PrintTicket-Anbietern verwendet. Beachten Sie, dass in jeder Einschränkung die Mandatory-Eigenschaft des ParameterDef-Elements auf Bedingungslos festgelegt werden muss. Die ParameterDef muss einen definierten Wert haben, andernfalls konnte der abhängige Wert oder die Einschränkung nicht ausgewertet werden.<br /> | Nein<br /> | 
| MaxLength <br /> | integer, wenn die DataType-Eigenschaft eine Zeichenfolge angibt.<br /> DefaultValue: Es wird kein Maximalwert erzwungen.<br /> | Für Zeichenfolgenwertparameter gibt die am längsten zulässige Zeichenfolge an. Ui- und PrintCapabilities- oder PrintTicket-Anbieter verwenden diese Eigenschaft, um das ParameterDef-Element zu überprüfen.<br /> | Nein<br /> | 
| MaxValue <br /> | integer, wenn die DataType-Eigenschaft eine ganze Zahl angibt.<br /> decimal, wenn die DataType-Eigenschaft decimal angibt.<br /> DefaultValue: Es wird kein Maximalwert erzwungen.<br /> | Definiert für ParameterDef-Elemente mit ganzzahligen oder dezimalen Werten den größten zulässigen Wert.<br /> | Nein<br /> | 
| Minlength <br /> | integer, wenn die DataType-Eigenschaft eine Zeichenfolge angibt. <br /> DefaultValue: Es wird kein Mindestwert erzwungen.<br /> | Definiert für Zeichenfolgenwerte die kürzeste zulässige Zeichenfolge. Ui- und PrintCapabilities- oder PrintTicket-Anbieter verwenden diese Eigenschaft, um das ParameterDef-Element zu überprüfen.<br /> | Nein<br /> | 
| Minvalue <br /> | integer, wenn die DataType-Eigenschaft eine ganze Zahl angibt.<br /> decimal, wenn die DataType-Eigenschaft decimal angibt.<br /> DefaultValue: Es wird kein Mindestwert erzwungen.<br /> | Definiert für Ganzzahl- oder Dezimalwertparameter den kleinsten zulässigen Wert. <br /> | Nein<br /> | 
| Mehrere <br /> | integer, wenn die DataType-Eigenschaft eine ganze Zahl angibt.<br /> decimal, wenn die DataType-Eigenschaft decimal angibt.<br /> DefaultValue: 1<br /> | Bei Ganzzahl- oder Dezimalwertparametern sollte der Wert des Parameters ein Vielfaches dieser Zahl sein. Weitere Informationen finden Sie unter <a href="#notes-on-multiple">Hinweise zu mehreren in</a> dieser Tabelle.<br /> | Nein<br /> | 
| Unittype <br /> | Zeichenfolgenwert, der die für den Parameter verwendeten Einheiten angibt.<br /> Für dieses Feld gibt es keinen Standardwert.<br /> | Gibt die Einheiten an, in denen der Parameter ausgedrückt wird. Beispielsweise Winkel in Zehntel grad, Längen in Mikrons und so weiter.<br /> | Ja<br /> | 




 

## <a name="notes-on-multiple"></a>Hinweise zu mehreren

Für ParameterInit-Elemente mit ganzzahligen oder dezimalen Werten sollte der Wert von ParameterInit ein Vielfaches dieser Zahl sein. Beispielsweise können ParameterInit-Elemente mit Dezimalwert auf Zehntel beschränkt werden, indem sie diese Eigenschaft auf 0,1 festlegen. Benutzeroberflächenelemente verwenden diese Eigenschaft, wenn sie Dialoge und UI-Steuerelemente erstellen. Darüber hinaus kann der PrintTicket-Validierungscode diese Eigenschaft verwenden, um den Wert eines ParameterInit auf den nächsten Wert zu runden, der durch Multiple angegeben wird. Hinweis: Gerätetreiber und PrintCapabilities-Anbieter sollten nicht davon ausgehen, dass ParameterInit-Werte Vielfache dieses Eigenschaftswerts sind. Jeder Anbieter muss in der Lage sein, beliebige Werte auf den nächstgelegenen nutzbaren Wert zu runden. Dies liegt daran, dass verschiedene Anbieter unterschiedliche und in Konflikt stehende Werte für diese Eigenschaft angeben können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




