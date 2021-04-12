---
title: Komplexer channelType-Typ
description: Definiert einen Kanal, zu dem Anbieter Ereignisse protokollieren können.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- "\"ChannelType\", komplexer Typ, Ereignisprotokoll"
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81158306285631748830d8aaaaf9cf329d7c0af1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478144"
---
# <a name="channeltype-complex-type"></a>Komplexer channelType-Typ

Definiert einen Kanal, zu dem Anbieter Ereignisse protokollieren können.

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



| Element                                                                  | type                                                                                   | BESCHREIBUNG                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schlags**](eventmanifestschema-logging-channeltype-element.md)       | [**Channelloggingtype**](eventmanifestschema-channelloggingtype-complextype.md)       | Definiert die Eigenschaften der Protokolldatei, die den Kanal sichert, z. b. die Kapazität und ob die Protokolldatei sequenziell oder zirkulär ist.<br/>                                                         |
| [**liche**](eventmanifestschema-publishing-channeltype-element.md) | [**Channelpublishingtype**](eventmanifestschema-channelpublishingtype-complextype.md) | Definiert die Protokollierungs Eigenschaften für die Sitzung, die vom Kanal verwendet wird. Nur Debug-und analytische Kanäle und Kanäle, die benutzerdefinierte Isolation verwenden, können Protokollierungs Eigenschaften für Ihre Sitzung angeben.<br/> |



## <a name="attributes"></a>Attributes



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>type</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>access</td>
<td>Zeichenfolge</td>
<td>Ein SDDL-Zugriffs Deskriptor ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Deskriptor Definition Language</a> ), der den Zugriff auf die Protokolldatei steuert, die den Kanal sichert. Wenn das <strong>Isolations</strong> Attribut auf "Application" oder "System" festgelegt ist, steuert der Zugriffs Deskriptor den Lesezugriff auf die Datei (die Schreibberechtigungen werden ignoriert). Wenn das <strong>Isolations</strong> Attribut auf Custom festgelegt ist, steuert der Zugriffs Deskriptor den Schreibzugriff auf den Kanal und den Lesezugriff auf die Datei.<br/></td>
</tr>
<tr class="even">
<td>Chid</td>
<td>token</td>
<td>Ein Bezeichner, der den Kanal in der Liste der vom Anbieter definierten oder importierten Kanäle eindeutig identifiziert. Verwenden Sie diesen Wert, wenn Sie in einem Ereignis auf den Kanal verweisen. Wenn Sie keinen channelbezeichner angeben, verwenden Sie den Namen des Kanals, um auf diesen Kanal in einer Ereignis Definition zu verweisen.<br/></td>
</tr>
<tr class="odd">
<td>enabled</td>
<td>boolean</td>
<td>Bestimmt, ob der Kanal aktiviert ist. Auf " <strong>true</strong> " festlegen, um die Protokollierung auf dem Kanal zuzulassen. andernfalls <strong>false</strong>. Der Standardwert ist <strong>false</strong> (die Protokollierung ist deaktiviert).<br/> Da es sich bei Debug-und analytischen Kanaltypen um Kanäle mit hohem Volumen handelt, sollten Sie den Kanal nur aktivieren, wenn Sie ein Problem mit einer Komponente untersuchen, die in diesen Kanal schreibt. Andernfalls sollte der Kanal deaktiviert bleiben.<br/> Jedes Mal, wenn Sie einen Debug-und analysekanal aktivieren, löscht der Dienst die Ereignisse aus dem Kanal.<br/></td>
</tr>
<tr class="even">
<td>Isolierung</td>
<td>Zeichenfolge</td>
<td>Der Isolations Wert definiert die Standard Zugriffsberechtigungen für den Kanal. Sie können einen der folgenden Werte angeben:
<ul>
<li><strong>Anwendung</strong></li>
<li><strong>System</strong></li>
<li><strong>Benutzerdefiniert</strong></li>
</ul>
Die Standard Isolation ist die <strong>Anwendung</strong>. Die Standard Berechtigungen für die <strong>Anwendung</strong> werden (mit SDDL angezeigt): <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
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

<p>Die Standard Berechtigungen für <strong>System</strong> lauten (mit SDDL angezeigt):</p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<p>Die Standard Berechtigungen für die <strong>benutzerdefinierte</strong> Isolation sind identisch mit der Anwendung.</p>
<p>Kanäle, die die <strong>Anwendungs</strong> Isolation angeben, verwenden dieselbe ETW-Sitzung. Das gleiche gilt für die <strong>System</strong> Isolation. Wenn Sie jedoch eine <strong>benutzerdefinierte</strong> Isolation angeben, erstellt der Dienst eine separate ETW-Sitzung für den Kanal. Wenn Sie die <strong>benutzerdefinierte</strong> Isolation verwenden, können Sie die Zugriffsberechtigungen für den Kanal und die Sicherungsdatei steuern. Da nur 64 ETW-Sitzungen verfügbar sind, sollten Sie die Verwendung der <strong>benutzerdefinierten</strong> Isolierung einschränken.</p></td>
</tr>
<tr class="odd">
<td>message</td>
<td>Zeichenfolge</td>
<td><p>Der lokalisierte Anzeige Name für den Kanal. Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> -Abschnitt des Manifests.</p></td>
</tr>
<tr class="even">
<td>name</td>
<td>anyURI</td>
<td><p>Der Name des Channels. Der Name muss innerhalb der Liste der vom Anbieter verwendeten Kanäle eindeutig sein. Die Konvention für Benennungs Kanäle besteht darin, den Kanaltyp an den Namen des Anbieters anzufügen. Beispiel: Wenn der Name des Anbieters Company-Product-Component lautet und Sie einen Betriebskanal definieren, lautet der Name Company-Product-Component/Operational.</p>
<p>Channelnamen müssen weniger als 255 Zeichen umfassen und dürfen die folgenden Zeichen nicht enthalten: ">", "<', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td>Symbol</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>Csymboltype</strong></a></td>
<td><p>Das Symbol, das für den Verweis auf den Kanal in Ihrer Anwendung verwendet werden soll. Der <a href="message-compiler--mc-exe-.md"><strong>Nachrichten Compiler (MC.exe)</strong></a> verwendet das Symbol, um eine Konstante für den Kanal in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler den Namen für Sie.</p></td>
</tr>
<tr class="even">
<td>type</td>
<td>Zeichenfolge</td>
<td><p>Identifiziert den Typ des Kanals. Sie können einen der folgenden Typen angeben:</p>
<ul>
<li><strong>Administrator</strong></li>
<li><strong>Bei Betrieb</strong></li>
<li><strong>Analytic</strong></li>
<li><strong>Debuggen</strong></li>
</ul>
<p>Admin-typkanäle unterstützen Ereignisse, die Endbenutzern, Administratoren und Supportmitarbeitern als Ziel haben. Ereignisse, die in die admin-Kanäle geschrieben werden, sollten über eine klar definierte Lösung verfügen, auf der der Administrator agieren kann. Ein Beispiel für ein Admin-Ereignis ist ein Ereignis, das auftritt, wenn eine Anwendung keine Verbindung zu einem Drucker herstellt. Diese Ereignisse sind entweder gut dokumentiert oder verfügen über eine Nachricht, die dem Reader direkt Anweisungen zur Behebung des Problems liefert.</p>
<p>Operational Type Channels unterstützen Ereignisse, die zum Analysieren und Diagnostizieren eines Problems oder eines Vorkommens verwendet werden. Sie können zum Auslösen von Tools oder Aufgaben anhand des Problems oder des Vorkommens verwendet werden. Beispielsweise handelt es sich um ein Vorgangsereignis, wenn ein Drucker einem System hinzugefügt oder daraus entfernt wird.</p>
<p>Analytische typkanäle unterstützen Ereignisse, die in hohem Umfang veröffentlicht werden. Sie beschreiben Programmvorgänge und geben Probleme an, die nicht durch Benutzereingriffe behoben werden können.</p>
<p>Debug-typkanäle unterstützen Ereignisse, die ausschließlich von Entwicklern zum Diagnostizieren eines Problems beim Debuggen verwendet werden.</p>
<p>Analytische und Debugkanäle sind standardmäßig deaktiviert und sollten nur aktiviert werden, um die Ursache eines Problems zu bestimmen. Beispielsweise können Sie den Channel aktivieren, das Szenario ausführen, das das Problem verursacht, den Kanal deaktivieren und dann die Ereignisse Abfragen. Beachten Sie, dass durch Aktivieren des Kanals der Kanal vorhandener Ereignisse gelöscht wird. Wenn für den Analyse-und Debugkanal eine zirkuläre Unterstützungs Datei verwendet wird, müssen Sie den Kanal deaktivieren, um seine Ereignisse abzufragen.</p>
<p>Alle Administrator Kanäle verwenden dieselbe ETW-Sitzung. das gleiche gilt für Betriebs Kanäle. Allerdings wird für jeden Analyse-und Debugkanal eine separate ETW-Sitzung verwendet. Dies ist ein weiterer Grund, bei Bedarf nur diese Kanaltypen zu aktivieren (es ist eine begrenzte Anzahl von ETW-Sitzungen verfügbar).</p></td>
</tr>
<tr class="odd">
<td>value</td>
<td><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></td>
<td><p>Ein numerischer Bezeichner, der den Kanal innerhalb der Liste der vom Anbieter definierten Kanäle eindeutig identifiziert. Der Nachrichten Compiler weist den Wert zu, wenn er nicht angegeben ist.</p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Wenn der Name des Kanals der channelbenennungs Konvention folgt, listet der Windows-Ereignisanzeige den Kanal mithilfe der Zeichenfolge auf, die dem umgekehrten Schrägstrich folgt. Wenn der ChannelName beispielsweise Company-Product-Component/Operational ist, wird der Kanal vom Ereignisanzeige als betriebsbereit mit dem Anbieter Company-Product-Component aufgelistet. Andernfalls wird der gesamte Kanalname unter dem Anbieter angezeigt. Wenn angegeben, wird der lokalisierte Anzeige Name verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




`
