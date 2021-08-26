---
description: Erfahren Sie mehr über XML-Attribute im Druckschemaframework. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: XML-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf76889fdf38c6636b4beb5ba566b18af69e34c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622976"
---
# <a name="xml-attributes"></a>XML-Attribute

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Es gibt eine Reihe von XML-Attributen, die in mehreren Elementtypen angezeigt werden, die im Druckschemaframework definiert sind. XML-Attribute mit demselben Namen haben in der Regel dieselbe Bedeutung und befolgen die gleichen Regeln, unabhängig vom Elementtyp, in dem sie sich befinden. Daher werden die XML-Attribute hier nach Name und nicht nach ihrem Hostelementtyp aufgelistet. Privat definierte XML-Attribute sind nicht zulässig. Nur die hier definierten XML-Attribute können in einem PrintCapabilities-Dokument oder einem PrintTicket und dann nur im definierten Kontext verwendet werden.

Private Parteien dürfen zwar keine neuen Definitionen in den Namespace einer anderen Partei einführen, sie dürfen jedoch vorhandene Namen aus einem anderen privaten Namespace verwenden, solange ihre Verwendung mit der von der anderen Partei festgelegten Verwendung konsistent ist. Daher kann eine Option ScoredProperty-Elemente enthalten, die von mehreren verschiedenen Parteien definiert wurden, die sich jeweils in unterschiedlichen Namespaces befinden.



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributname</th>
<th>Datentypen und Werte</th>
<th>Zweck</th>
<th>Hinweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name <br/></td>
<td>XML QName<br/></td>
<td>Dieses XML-Attribut identifiziert die Elementinstanz. Es unterscheidet ein Element von einem anderen Element desselben Elementtyps. Dieses XML-Attribut wird so häufig verwendet, dass es als Namensattribut bezeichnet wird.<br/></td>
<td>Die folgenden Einschränkungen gelten für das Name-Attribut.<br/>
<ul>
<li>Das Name-Attribut muss in Form eines gültigen XML-definierten QName-Werts sein. Das heißt, sie muss durch einen gültigen XML-Namespace qualifiziert werden. Die QNames, die als Werte von Namensattributen angezeigt werden, müssen explizit namespacequalifiziert sein, auch wenn ein Standardnamespace definiert ist. <br/></li>
<li>Der Zeicheninhalt muss der eines gültigen XML-definierten QName sein. <br/></li>
<li>Privat definierte Namen müssen mit einem Namespace qualifiziert werden, der eindeutig der Partei zugeordnet ist, die das Namensattribut eingeführt hat.<br/></li>
<li>Anforderung an die gleichgeordnete Eindeutigkeit: Zwei gleichgeordnete Elemente, die zum gleichen Elementtyp gehören, dürfen nicht das gleiche Namensattribut haben. Die einzige Ausnahme sind Option-Elemente, bei denen das Name-Attribut verwendet werden kann, um eine Option zu definieren. Daher können mehrere gleichgeordnete Option-Elemente das gleiche Namensattribut haben.<br/></li>
<li>Die folgenden Elementtypen können Namensattribute enthalten: Property, ScoredProperty, ParameterDef, Option und Feature.<br/></li>
<li>Name-Attribute müssen in jedem element-Typ angezeigt werden, der sie enthält, mit Ausnahme einiger zuvor definierter öffentlicher Elemente der Druckschemaoption, z. B. DocumentNUp.<br/></li>
</ul>
Das folgende Beispiel zeigt, wie Sie eine Option-Instanz mithilfe eines "name"-Attributs identifizieren. Dies ist die richtige Methode zum Definieren von Option-Elementen. Ein Anbieter sollte keine unbenannten Optionen haben, es sei denn, sie sind öffentlich im Druckschema definiert, z. B. DocumentNUp.<br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td>Weitergegeben <br/></td>
<td>Enumeration<br/> Derzeit sind keine Werte definiert.<br/></td>
<td>Das Attribut "propagate" wird in der ursprünglichen Version des Druckschemaframeworks nicht verwendet. Dies ist hier dokumentiert, damit printCapabilities- oder PrintTicket-Validierungscode, der für die erste Version des Druckschemaframework implementiert wurde, alle nachfolgenden Schemaversionen ohne Fehler verarbeiten kann.<br/></td>

</tr>
<tr class="odd">
<td>Eingeschränkt <br/></td>
<td>Enumeration<br/> Zulässige Werte:<br/>
<ul>
<li>Keine <br/></li>
<li>PrintTicketSettings <br/></li>
<li>AdminSettings <br/></li>
<li>DeviceSettings <br/></li>
</ul></td>
<td>Gibt an, ob die Option zur Auswahl oder zur Verwendung verfügbar ist. <br/></td>
<td>Die zulässigen Werte des eingeschränkten Attributs haben die folgende Bedeutung. Beachten Sie, dass diese Werte in der Reihenfolge aufgeführt sind, von der am wenigsten restriktiven (Keine) bis zur restriktivsten (DeviceSettings).<br/> Keine <br/>
<ul>
<li>Die Option ist nicht eingeschränkt. <br/></li>
</ul>
PrintTicketSettings <br/>
<ul>
<li>Die Option wird durch die PrintTicket-Einstellungen eingeschränkt. Dies bedeutet, dass das Ändern der Konfiguration die Einschränkung entfernen kann. <br/></li>
</ul>
AdminSettings <br/>
<ul>
<li>Die Option wird durch die Einstellungen des Administrators eingeschränkt. Die Option kann vom Benutzer nicht aktiviert werden.<br/></li>
</ul>
DeviceSettings <br/>
<ul>
<li>Die Option wird durch die Geräteeinstellungen oder die optionen für physisch installierte Geräte eingeschränkt. Die Option kann weder vom Benutzer noch vom Administrator aktiviert werden.<br/></li>
</ul>
Wenn der PrintCapabilities-Anbieter Werte des eingeschränkten Attributs meldet, sollte die restriktivste gefundene Einschränkung gemeldet werden. Wenn beispielsweise eine Option sowohl durch eine Administratoreinstellung als auch durch eine Geräteeinstellung eingeschränkt wird, sollte der PrintCapabilities-Anbieter DeviceSettings melden.<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>URI<br/></td>
<td>Dieses XML-Attribut erstellt eine Verknüpfung zwischen einem Namespace-URI (Uniform Resource Identifier) und dem Namespacepräfix, das im XML QName angezeigt wird. Sie müssen einen solchen Link zu dem Namespace-URI einrichten, der für das Druckschemaframework definiert ist, bevor Sie eines der Framework-definierten Elementtags, Attribute, Namensattribute und so weiter verwenden können. Sie können diesen Namespace als Standardnamespace deklarieren, um zu vermeiden, dass die Elementtags tatsächlich mit einem Namespacepräfix qualifiziert werden, obwohl alle anderen QNames explizit qualifiziert werden müssen. Der Standardnamespace muss im entsprechenden Stammelement definiert werden. Beachten Sie alle XML-Regeln und -Konventionen in Bezug auf die Verwendung des xmlns-Attributs.<br/> Der URI für das Druckschemaframework ist http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .<br/> Der URI für die Druckschemaschlüsselwörter ist https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




