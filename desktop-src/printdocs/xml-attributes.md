---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: XML-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dd05effe6f3ea79afd0972867cb2734ace1a71
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106366573"
---
# <a name="xml-attributes"></a>XML-Attribute

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Es gibt eine Reihe von XML-Attributen, die in mehreren Elementtypen angezeigt werden, die im Druck Schema Framework definiert sind. XML-Attribute mit demselben Namen haben in der Regel dieselbe Bedeutung und befolgen dieselben Regeln, unabhängig von dem Elementtyp, in dem Sie sich befinden. Daher werden die XML-Attribute hier nach Namen und nicht nach Ihrem Host Elementtyp aufgelistet. Privat definierte XML-Attribute sind nicht zulässig. Nur die hier definierten XML-Attribute können in einem printfunktionen-Dokument oder einem PrintTicket verwendet werden, und dann nur im definierten Kontext.

Obwohl Privatparteien keine neuen Definitionen in den Namespace einer anderen Partei einführen dürfen, ist es zulässig, vorhandene Namen aus einem anderen privaten Namespace zu verwenden, solange die Verwendung mit der von der anderen Partei eingerichteten Nutzung konsistent ist. Daher kann eine Option ScoredProperty-Elemente enthalten, die von mehreren verschiedenen Parteien definiert werden, die sich jeweils in unterschiedlichen Namespaces befinden.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributname</th>
<th>Datentypen und Werte</th>
<th>Zweck</th>
<th>Notizen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name <br/></td>
<td>XML-QName<br/></td>
<td>Dieses XML-Attribut identifiziert die-Element Instanz. Es unterscheidet ein Element von einem anderen desselben Elementtyps. Dieses XML-Attribut wird so weit verbreitet verwendet, dass es als Name-Attribut bezeichnet wird.<br/></td>
<td>Die folgenden Einschränkungen beziehen sich auf das Name-Attribut.<br/>
<ul>
<li>Das Name-Attribut muss in der Form eines gültigen XML-definierten QName vorliegen. Das heißt, er muss durch einen gültigen XML-Namespace qualifiziert werden. Die QNames, die als Werte von namens Attributen angezeigt werden, müssen explizit Namespace qualifiziert werden, auch wenn ein Standard Namespace definiert ist. <br/></li>
<li>Der Zeichen Inhalt muss ein gültiger XML-definierter QName sein. <br/></li>
<li>Privat definierte Namen müssen mit einem Namespace qualifiziert werden, der eindeutig mit der Partei verknüpft ist, die das Name-Attribut eingeführt hat.<br/></li>
<li>Gleich geordnete Eindeutigkeits Anforderung: keine zwei gleich geordneten Elemente, die zum selben Elementtyp gehören, haben möglicherweise dasselbe Name-Attribut. Die einzige Ausnahme sind Options Elemente, bei denen das Name-Attribut verwendet werden kann, um eine Option zu definieren. Daher können mehrere gleich geordnete Options Elemente dasselbe Name-Attribut aufweisen.<br/></li>
<li>Die folgenden Elementtypen können namens Attribute enthalten: Eigenschaft, ScoredProperty, ParameterDef, Option und Feature.<br/></li>
<li>namens Attribute müssen in jedem der Elementtypen angezeigt werden, die Sie enthalten, es sei denn, es gibt einige zuvor definierte Elemente der öffentlichen Druck Schema Option (z. b. DocumentNUp).<br/></li>
</ul>
Im folgenden Beispiel wird gezeigt, wie eine Options Instanz mit einem ' Name '-Attribut identifiziert wird. Dies ist die korrekte Methode zum Definieren von Options Elementen. Ein Anbieter sollte keine unbenannten Optionen haben, es sei denn, Sie sind öffentlich im Druck Schema definiert, z. b. in DocumentNUp.<br/>
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
<td>Pixeln <br/></td>
<td>Enumeration<br/> Zurzeit sind keine Werte definiert.<br/></td>
<td>Das propagierte Attribut wird in der ersten Version des Print Schema-Frameworks nicht verwendet. Es ist hier dokumentiert, damit printfunktionalitäten oder PrintTicket-Validierungscode, der für die ursprüngliche Version des Print Schema-Frameworks implementiert wurde, alle nachfolgenden Schema Versionen ohne Fehler verarbeiten kann.<br/></td>

</tr>
<tr class="odd">
<td>schwierige <br/></td>
<td>Enumeration<br/> Zulässige Werte:<br/>
<ul>
<li>Keine <br/></li>
<li>Printticketsettings <br/></li>
<li>Adminsettings <br/></li>
<li>Geräte-Manager <br/></li>
</ul></td>
<td>Gibt an, ob die Option für die Auswahl oder zur Verwendung verfügbar ist. <br/></td>
<td>Die zulässigen Werte des eingeschränkten Attributs haben folgende Bedeutungen. Beachten Sie, dass diese Werte in der Reihenfolge aufgelistet werden, von der geringsten Einschränkung (keine) bis zu den meisten restriktiveren (Geräte-Manager).<br/> Keine <br/>
<ul>
<li>Die Option ist nicht eingeschränkt. <br/></li>
</ul>
Printticketsettings <br/>
<ul>
<li>Die Option wird durch die PrintTicket-Einstellungen eingeschränkt. Dies bedeutet, dass das Ändern der Konfiguration die Einschränkung entfernen kann. <br/></li>
</ul>
Adminsettings <br/>
<ul>
<li>Die Option wird durch die Einstellungen des Administrators eingeschränkt. die Option kann vom Benutzer nicht aktiviert werden.<br/></li>
</ul>
Geräte-Manager <br/>
<ul>
<li>Die Option wird durch die Geräteeinstellungen oder die physisch installierten Geräteoptionen eingeschränkt. die Option kann weder vom Benutzer noch vom Administrator aktiviert werden.<br/></li>
</ul>
Wenn der PrintValues-Anbieter Werte des eingeschränkten Attributs meldet, sollte die restriktivste Einschränkung gemeldet werden. Wenn eine Option beispielsweise durch eine Administrator Einstellung und eine Geräteeinstellung eingeschränkt ist, sollte der printSettings-Anbieter devicesettings melden.<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>URI<br/></td>
<td>Dieses XML-Attribut stellt eine Verknüpfung zwischen einem Namespace-URI (Uniform Resource Identifier) und dem Namespace Präfix her, der im XML-QName angezeigt wird. Sie müssen einen solchen Link zum Namespace-URI einrichten, der für das Druck Schema Framework definiert ist, bevor Sie eines der Framework-definierten Element Tags, Attribute, namens Attribute usw. verwenden können. Sie können diesen Namespace als Standard deklarieren, um zu vermeiden, dass die Element Tags tatsächlich mit einem Namespace Präfix qualifiziert werden, obwohl alle anderen QNames explizit qualifiziert werden müssen. Der Standard Namespace muss im entsprechenden Root-Element definiert werden. Beachten Sie alle XML-Regeln und-Konventionen hinsichtlich der Verwendung des xmlns-Attributs.<br/> Der URI für das Druck Schema-Framework ist http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .<br/> Der URI für die Schlüsselwörter des Druck Schemas ist https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




