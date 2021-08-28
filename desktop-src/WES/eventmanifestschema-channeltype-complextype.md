---
title: Komplexer ChannelType-Typ
description: Definiert einen Kanal, an den Anbieter Ereignisse protokollieren können.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- Komplexer ChannelType-Typ EventLog
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b780d68d419fa29d5ee13995f1b66a412fc89323
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627966"
---
# <a name="channeltype-complex-type"></a>Komplexer ChannelType-Typ

Definiert einen Kanal, an den Anbieter Ereignisse protokollieren können.

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                  | Typ                                                                                   | Beschreibung                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Protokollierung**](eventmanifestschema-logging-channeltype-element.md)       | [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)       | Definiert die Eigenschaften der Protokolldatei, die den Kanal sichern, z. B. die Kapazität und ob die Protokolldatei sequenziell oder kreisförmig ist.<br/>                                                         |
| [**Publishing**](eventmanifestschema-publishing-channeltype-element.md) | [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) | Definiert die Protokollierungseigenschaften für die Sitzung, die der Kanal verwendet. Nur Debug- und Analysekanäle und Kanäle, die benutzerdefinierte Isolation verwenden, können Protokollierungseigenschaften für ihre Sitzung angeben.<br/> |



## <a name="attributes"></a>Attributes



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>access</td>
<td>string</td>
<td>Ein <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">SDDL-Zugriffsdeskriptor (Security Descriptor Definition Language),</a> der den Zugriff auf die Protokolldatei steuert, die den Kanal unterstützt. Wenn das <strong>Isolationsattribut</strong> auf Anwendung oder System festgelegt ist, steuert der Zugriffsdeskriptor den Lesezugriff auf die Datei (die Schreibberechtigungen werden ignoriert). Wenn das <strong>Isolationsattribut</strong> auf Benutzerdefiniert festgelegt ist, steuert der Zugriffsdeskriptor den Schreibzugriff auf den Kanal und den Lesezugriff auf die Datei.<br/></td>
</tr>
<tr class="even">
<td>Chid</td>
<td>token</td>
<td>Ein Bezeichner, der den Kanal in der Liste der Kanäle, die der Anbieter definiert oder importiert, eindeutig identifiziert. Verwenden Sie diesen Wert, wenn Sie auf den Kanal in einem Ereignis verweisen. Wenn Sie keinen Kanalbezeichner angeben, verwenden Sie den Namen des Kanals, um in einer Ereignisdefinition auf diesen Kanal zu verweisen.<br/></td>
</tr>
<tr class="odd">
<td>enabled</td>
<td>boolean</td>
<td>Bestimmt, ob der Kanal aktiviert ist. Legen Sie auf <strong>TRUE fest,</strong> um die Protokollierung im Kanal zu ermöglichen. andernfalls <strong>FALSE.</strong> Der Standardwert ist <strong>FALSE</strong> (die Protokollierung ist deaktiviert).<br/> Da es sich bei den Kanaltypen Debug und Analytics um Kanäle mit hohem Volumen handelt, sollten Sie den Kanal nur aktivieren, wenn Sie ein Problem mit einer Komponente untersuchen, die in diesen Kanal schreibt. Andernfalls sollte der Kanal deaktiviert bleiben.<br/> Jedes Mal, wenn Sie einen Debug- und Analysekanal aktivieren, werden die Ereignisse vom Dienst aus dem Kanal entfernt.<br/></td>
</tr>
<tr class="even">
<td>Isolierung</td>
<td>string</td>
<td>Der Isolationswert definiert die Standardzugriffsberechtigungen für den Kanal. Sie können einen der folgenden Werte angeben:
<ul>
<li><strong>Anwendung</strong></li>
<li><strong>System</strong></li>
<li><strong>Benutzerdefiniert</strong></li>
</ul>
Die Standardisolation ist <strong>Application</strong>. Die Standardberechtigungen <strong>für Anwendung</strong> sind (mit SDDL dargestellt): <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Text</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p>Die Standardberechtigungen <strong>für System</strong> sind (mit SDDL dargestellt):</p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Text</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Die Standardberechtigungen für <strong>die benutzerdefinierte</strong> Isolation sind identisch mit anwendungsspezifischen Berechtigungen.</p>
<p>Kanäle, die <strong>Anwendungsisolation</strong> angeben, verwenden dieselbe ETW-Sitzung. Dasselbe gilt für die <strong>Systemisolation.</strong> Wenn Sie jedoch benutzerdefinierte <strong>Isolation</strong> angeben, erstellt der Dienst eine separate ETW-Sitzung für den Kanal. Mithilfe <strong>der</strong> benutzerdefinierten Isolation können Sie die Zugriffsberechtigungen für den Kanal und die Hintergrunddatei steuern. Da nur 64 ETW-Sitzungen verfügbar sind, sollten Sie die Verwendung der benutzerdefinierten <strong>Isolation</strong> einschränken.</p></td>
</tr>
<tr class="odd">
<td>message</td>
<td>Zeichenfolge</td>
<td><p>Der lokalisierte Anzeigename für den Kanal. Die Meldungszeichenfolge verweist auf eine lokalisierte Zeichenfolge im <a href="eventmanifestschema-stringtable-resources-element.md"><strong>StringTable-Abschnitt</strong></a> des Manifests.</p></td>
</tr>
<tr class="even">
<td>name</td>
<td>anyURI</td>
<td><p>Der Name des Channels. Der Name muss innerhalb der Liste der vom Anbieter verwendeten Kanäle eindeutig sein. Die Konvention zum Benennen von Kanälen besteht im Anfügen des Kanaltyps an den Namen des Anbieters. Beispiel: Wenn der Name des Anbieters Company-Product-Component ist und Sie einen Betriebskanal definieren, würde der Name Company-Product-Component/Operational sein.</p>
<p>Kanalnamen müssen weniger als 255 Zeichen lang sein und dürfen nicht die folgenden Zeichen enthalten: '>', '<', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td>Symbol</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td><p>Das Symbol, das verwendet werden soll, um auf den Kanal in Ihrer Anwendung zu verweisen. Der <a href="message-compiler--mc-exe-.md"><strong>Nachrichtencompiler (MC.exe)</strong></a> verwendet das -Symbol, um eine Konstante für den Kanal in der Headerdatei zu erstellen, die der Compiler generiert. Wenn Sie kein Symbol angeben, generiert der Compiler den Namen für Sie.</p></td>
</tr>
<tr class="even">
<td>Typ</td>
<td>string</td>
<td><p>Identifiziert den Kanaltyp. Sie können einen der folgenden Typen angeben:</p>
<ul>
<li><strong>Administrator</strong></li>
<li><strong>Bei Betrieb</strong></li>
<li><strong>Analytic</strong></li>
<li><strong>Debuggen</strong></li>
</ul>
<p>Kanäle vom Administratortyp unterstützen Ereignisse, die auf Endbenutzer, Administratoren und Supportmitarbeiter zielen. Ereignisse, die in die Administratorkanäle geschrieben werden, sollten über eine klar definierte Lösung verfügen, auf die der Administrator agieren kann. Ein Beispiel für ein Administratorereignis ist ein Ereignis, das auftritt, wenn eine Anwendung keine Verbindung mit einem Drucker herstellen kann. Diese Ereignisse sind entweder gut dokumentiert, oder ihnen ist eine Meldung zugeordnet, die dem Leser direkte Anweisungen dazu gibt, was zur Behebung des Problems getan werden muss.</p>
<p>Betriebstypkanäle unterstützen Ereignisse, die zum Analysieren und Diagnostizieren eines Problems oder Auftretens verwendet werden. Sie können zum Auslösen von Tools oder Aufgaben anhand des Problems oder des Vorkommens verwendet werden. Beispielsweise handelt es sich um ein Vorgangsereignis, wenn ein Drucker einem System hinzugefügt oder daraus entfernt wird.</p>
<p>Kanäle des Analysetyps unterstützen Ereignisse, die in hohem Volumen veröffentlicht werden. Sie beschreiben Programmvorgänge und geben Probleme an, die nicht durch Benutzereingriffe behoben werden können.</p>
<p>Debugtypkanäle unterstützen Ereignisse, die ausschließlich von Entwicklern verwendet werden, um ein Problem für das Debuggen zu diagnostizieren.</p>
<p>Analyse- und Debugkanäle sind standardmäßig deaktiviert und sollten nur aktiviert werden, um die Ursache eines Problems zu ermitteln. Beispielsweise würden Sie den Kanal aktivieren, das Szenario ausführen, das das Problem verursacht, den Kanal deaktivieren und dann die Ereignisse abfragen. Beachten Sie, dass das Aktivieren des Kanals den Kanal vorhandener Ereignisse freit. Wenn der Analyse- und Debugkanal eine zirkuläre Hintergrunddatei verwendet, müssen Sie den Kanal deaktivieren, um seine Ereignisse abfragen zu können.</p>
<p>Alle Administratorkanäle verwenden dieselbe ETW-Sitzung. gleiches gilt für Betriebskanäle. Jeder Analyse- und Debugkanal verwendet jedoch eine separate ETW-Sitzung. Dies ist ein weiterer Grund, diese Kanaltypen nur bei Bedarf zu aktivieren (es ist eine begrenzte Anzahl von ETW-Sitzungen verfügbar).</p></td>
</tr>
<tr class="odd">
<td>value</td>
<td><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></td>
<td><p>Ein numerischer Bezeichner, der den Kanal in der Liste der vom Anbieter definierten Kanäle eindeutig identifiziert. Der Nachrichtencompiler weist den Wert zu, wenn er nicht angegeben ist.</p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Wenn der Name des Kanals der Kanalbenennungskonvention entspricht, listet der Windows Ereignisanzeige den Kanal mithilfe der Zeichenfolge auf, die dem umgekehrten Schrägstrich folgt. Wenn der Kanalname beispielsweise Company-Product-Component/Operational lautet, listet der Ereignisanzeige den Kanal unter dem Anbieter Company-Product-Component als Betriebsbereit auf. Andernfalls wird der gesamte Kanalname unter dem Anbieter angezeigt. Der lokalisierte Anzeigename wird verwendet, sofern angegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




`
