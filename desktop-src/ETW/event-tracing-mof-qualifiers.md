---
description: Verwenden Sie die Qualifizierer, die in diesem Abschnitt definiert sind, wenn Sie die MOF-Klasse, Ereignis-MOF-Klasse, Ereignistyp-MOF-Klasse und die Eigenschaften der MOF-Klasse des Ereignis Typs erstellen
ms.assetid: 3bc82074-05a7-411f-884f-5da1fd08112b
title: Ereignis Ablauf Verfolgung für MOF
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7b4250b73e84d46a19dab307d0c263ab1cc7782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868663"
---
# <a name="event-tracing-mof-qualifiers"></a>Ereignis Ablauf Verfolgung für MOF

Verwenden Sie die Qualifizierer, die in diesem Abschnitt definiert sind, wenn Sie die [MOF-Klasse](#provider-mof-class-qualifiers), [Ereignis-MOF](#event-mof-class-qualifiers)-Klasse, [Ereignistyp-MOF](#event-type-mof-class-qualifiers)-Klasse und [die Eigenschaften der MOF-Klasse des Ereignis Typs](#property-qualifiers)erstellen Ein Beispiel, das einige dieser Qualifizierer enthält, finden [Sie unter Veröffentlichen Ihres Ereignis Schemas](publishing-your-event-schema.md).

## <a name="provider-mof-class-qualifiers"></a>MOF-Klassen Qualifizierer

In der folgenden Tabelle sind die Qualifizierer aufgelistet, die Sie für die MOF-Klasse eines Anbieters angeben können



| Qualifizierer | Datentyp  | BESCHREIBUNG                                                                                                                                                                                                                                                  |
|-----------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**  | **String** | Erforderlich. Zeichen folgen-GUID, die einen Anbieter eindeutig identifiziert. Beispiel: GUID ("{3F 92e6e0-9886-434e-85dB-0d11d3904c0a}"). Dies ist dieselbe GUID, die Sie verwenden, wenn Sie die [**registertraceguids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) -Funktion aufrufen, um den Anbieter zu registrieren. |



 

## <a name="event-mof-class-qualifiers"></a>MOF-Klassen Qualifizierer

In der folgenden Tabelle sind die Qualifizierer aufgelistet, die Sie für eine Ereignisklasse angeben können (die übergeordnete Klasse, die Verwandte Ereignistyp Klassen gruppiert).

| Qualifizierer        | Datentyp   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**         | **String**  | Erforderlich. Zeichen folgen-GUID, die eine Ereignisklasse identifiziert. Beispiel: GUID ("{3F 92e6e0-9886-434e-85dB-0d11d3904c0a}"). Ereignis Anbieter verwenden die GUID, um den [**Ereignis Ablauf \_ Verfolgungs Header festzulegen \_ . GUID**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Member, damit Consumer die Klasse der empfangenen Ereignisse ermitteln können.                                                                                                                                                                                                                                                                                  |
| **Eventversion** | **Integer** | Dieser Qualifizierer ist für die neueste Version einer Ereignis Ablauf Verfolgungs Klasse optional und ist für alle älteren Versionen der-Klasse erforderlich. Die neueste Version der-Klasse gibt entweder weder den **eventversion** -Qualifizierer noch die höchste Versionsnummer an. Die Versionsnummern beginnen mit 0 (z. b. eventversion (0)). Wenn Sie eine neue Version der-Klasse erstellen, müssen Sie in der Regel auch die vorherige Version in VN umbenennen <classname> \_ , wobei n eine inkrementelle Zahl ist, beginnend bei 0. Ein Beispiel finden Sie unter " [**fleio**](fileio.md) " und " [**fleio \_ v0**](fileio-v0.md)".<br/> |



 

## <a name="event-type-mof-class-qualifiers"></a>MOF-Klasse für Ereignistyp

In der folgenden Tabelle sind die Qualifizierer aufgelistet, die Sie für eine Ereignistyp Klasse angeben können (die Klasse, die die Ereignis Eigenschaften Daten definiert).



| Qualifizierer         | Wert       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EventType**     | **Integer** | Erforderlich. Bezeichnet die Ereignistyp Klasse. Beispiel: EventType (1). Der Ereignis Anbieter verwendet den gleichen Ereignistyp Wert, um den [**Ereignis Ablauf \_ Verfolgungs Header festzulegen \_ . Class. Type**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header). Wenn dieselbe MOF-Klasse für mehrere Ereignis Typen verwendet wird (da Sie dieselben Ereignisdaten verwenden), geben Sie den Ereignistyp Wert als Array von ganzen Zahlen an, z. b. EventType {12,15} . |
| **EventTypeName** | **String**  | Optional. Beschreibt den Ereignistyp. Beispiel: eventtypame ("Start"). Wenn dieselbe MOF-Klasse für mehrere Ereignis Typen verwendet wird (da Sie dieselben Ereignisdaten verwenden), geben Sie den Ereignistyp Namen als Zeichen folgen Array an, z. b. eventtykame {"Start", "End"}. Die Elemente des eventtypame-Arrays entsprechen direkt dem EventType-Array.                 |



 

## <a name="property-qualifiers"></a>Eigenschaften Qualifizierer

In der folgenden Tabelle sind die Qualifizierer aufgelistet, die Sie für eine Eigenschaft angeben können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Qualifizierer</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Bitmap</strong></td>
<td>Gibt die Bitpositionen an, die Zeichen folgen Werten zugeordnet werden. Wenn Sie diesen Qualifizierer angeben, müssen Sie auch den <strong>BitValues</strong> -Qualifizierer angeben.</td>
</tr>
<tr class="even">
<td><strong>BitValues</strong></td>
<td>Zeichen folgen Werte. Wenn auch der <strong>Bitmap</strong> -Qualifizierer angegeben wird, entsprechen die Zeichen folgen direkt den Werten im <strong>Bitmap</strong> -Qualifizierer. Angenommen, der Eigenschafts Wert ist ein einbasierter Index in den Wert Zeichenfolgen (Bit 1 entspricht der ersten Zeichenfolge in der Liste).</td>
</tr>
<tr class="odd">
<td><strong>Erweiterung</strong></td>
<td>Bietet zusätzliche Informationen zur Nutzung (Interpretation) der Daten. Beim Erweiterungs Wert wird die Groß-/Kleinschreibung beachtet. Fügen Sie den Wert in Anführungszeichen ein, z. b. Erweiterung ( &quot; GUID &quot; ). Mögliche Erweiterungs Werte sind: <dl> <dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>GUID</dt> <dd> Gibt an, dass die Eigenschafts Daten eine GUID sind. Der MOF-Datentyp muss ein <strong>Objekt</strong>sein. Es wird erwartet, dass die Nutzlast eine <strong>GUID</strong> -Struktur ist.<br/> </dd> <dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>Ipaddr und IPAddrV4</dt> <dd> Die Daten sind eine IP-V4-Adresse. Der MOF-Datentyp muss ein <strong>Objekt</strong>sein. Es wird erwartet, dass die Nutzlast eine Länge ohne Vorzeichen hat. Jedes Byte der unsignierten Länge stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.<br/> <strong>Vor Windows Vista:</strong> Die IPAddrV4-Erweiterung wird nicht unterstützt.<br/> </dd> <dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> <dd> Bei den Daten handelt es sich um eine IP-Adresse. Der MOF-Datentyp muss ein <strong>Objekt</strong>sein. Die Nutzlast wird als <strong>IN6_ADDR</strong> Struktur erwartet. <br/> <strong>Vor Windows Vista:</strong> Die IPAddrV6-Erweiterung wird nicht unterstützt.<br/> </dd> <dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>Noprint</dt> <dd> Gibt an, dass der Consumer diese Daten nicht ausdrucken soll.<br/> </dd> <dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</dt> <dd> Die Daten identifizieren eine Portnummer. Der MOF-Datentyp muss ein <strong>Objekt</strong>sein. Die Nutzlast wird als Ganzzahl ohne Vorzeichen Short erwartet.<br/> </dd> <dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RString</dt> <dd> Zeilen vorzeichenzeichen wurden durch Leerzeichen ersetzt. Es wird erwartet, dass die Nutzlast eine auf NULL endende ANSI-Zeichenfolge ist.<br/> </dd> <dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>Rwstring</dt> <dd> Zeilen vorzeichenzeichen wurden durch Leerzeichen ersetzt. Es wird erwartet, dass die Nutzlast eine NULL-terminierte Zeichenfolge mit breit Zeichen ist.<br/> </dd> <dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</dt> <dd> Die Daten repräsentieren eine binäre Blob-sid. Der MOF-Datentyp muss ein <strong>Objekt</strong>sein. <br/> Die SID hat eine Variable Länge. Der Wert, der in den ersten 4 Bytes (<strong>ulong</strong>) enthalten ist, gibt an, ob das BLOB eine sid enthält. Wenn die ersten 4 Bytes (<strong>ulong</strong>) des BLOBs ungleich NULL sind, enthält das BLOB eine SID. Der erste Teil des BLOB enthält die TOKEN_USER (die-Struktur wird an einer 8-Byte-Grenze ausgerichtet), und der zweite Teil enthält die SID. So beheben Sie den SID-Teil des BLOBs:<br/>
<ul>
<li>Legen Sie einen Byte Zeiger auf den Anfang des BLOBs fest.</li>
<li>Multiplizieren Sie die Zeiger Größe für das Ereignisprotokoll um 2, und fügen Sie das Produkt zum Byte Zeiger hinzu (der <strong>pointersize</strong> -Member von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> der den Wert der Zeiger Größe enthält).</li>
</ul>
<br/> Sie können das folgende Makro verwenden, um die Länge der SID zu bestimmen. <br/>
<pre class="syntax" data-space="preserve"><code>#define SeLengthSid( Sid ) \
  (8 + (4 * ((SID *)Sid)->SubAuthorityCount))</code></pre>
</dd> <dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> <dd> Gibt an, dass die Eigenschaft einen Zeiger Wert enthält. Die Größe des Zeiger Werts hängt von dem Betriebssystem ab, das zum Protokollieren des Ereignisses verwendet wird. die Nutzlast enthält einen 4-Byte-Wert für 32-Bit-Systeme oder einen 8-Byte-Wert für 64-Bit-Systeme. Der MOF-Datentyp muss ein <strong>Objekt</strong>sein.<br/> Consumer sollten den Datentyp und den <strong>Format</strong> Qualifizierer ignorieren, wenn die-Eigenschaft die <strong>sizet</strong> -Erweiterung enthält. Um die Größe der Daten zu ermitteln, die für die Eigenschaft gelesen werden sollen, verwenden Sie Folgendes:
<ul>
<li>Der <strong>pointersize</strong> -Member von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Der <strong>Flags</strong> -Member von <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<br/> <strong>Vor Windows Vista:</strong> Der Wert für " <strong>pointersize</strong> " ist möglicherweise nicht korrekt. Auf einem 64-Bit-Computer protokolliert z. b. eine 32-Bit-Anwendung 4-Byte-Zeiger. in der Sitzung wird jedoch " <strong>pointersize</strong> " auf 8 festgelegt.<br/> </dd> <dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>Konfigur</dt> <dd> Die Daten repräsentieren ein BLOB. Die ersten vier Bytes (UInt32) geben die Größe des BLOBs an. Der MOF-Datentyp muss ein <strong>Objekt</strong>sein. <br/> </dd> <dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>Wmitime</dt> <dd> Übersetzt den Zeitstempel in die Systemzeit. Der MOF-Datentyp muss ein <strong>Objekt</strong>sein. Es wird erwartet, dass die Nutzlast eine Ganzzahl 64 ohne Vorzeichen ist.<br/> <strong>Vor Windows Vista:</strong> Nicht verfügbar.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Format</strong></td>
<td>Definiert das Format der Eigenschafts Daten. Beispielsweise &quot; bedeutet das Einschließen von Format (w &quot; ) für eine Zeichen folgen Eigenschaft, dass die Zeichenfolge eine Breite Zeichenfolge ist. Dabei sind folgende Werte möglich:
<table>
<thead>
<tr class="header">
<th>Begriff</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="c"></span><span id="C"></span>scher<br/></td>
<td>Zeigen Sie den Eigenschafts Wert als ASCII-Zeichen an. Sie können diesen Qualifizierer mit <strong>Uint8</strong> -Datentypen verwenden.<br/></td>
</tr>
<tr class="even">
<td><span id="s"></span><span id="S"></span>Hymnen<br/></td>
<td>Behandelt das Array von Zeichen als eine mit NULL endenden Zeichenfolge. Die Zeichenfolge ist eine Zeichenfolge mit breit Zeichen, wenn der Datentyp <strong>char16</strong>ist. Andernfalls ist die Zeichenfolge eine ASCII-Zeichenfolge.<br/></td>
</tr>
<tr class="odd">
<td><span id="w"></span><span id="W"></span>Löw<br/></td>
<td>Der Eigenschafts Wert ist eine Zeichenfolge mit breit Zeichen. Sie können diesen Qualifizierer mit <strong>Zeichen</strong> folgen-Datentypen verwenden. <br/></td>
</tr>
<tr class="even">
<td><span id="x"></span><span id="X"></span>Stuben<br/></td>
<td>Zeigen Sie den Eigenschafts Wert als hexadezimale Zahl an. Sie können diesen Qualifizierer mit 16-, 32-und 64-Bit-ganzzahligen Datentypen verwenden.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><strong>Zeiger</strong></td>
<td><p>Gibt an, dass die Eigenschaft einen Zeiger Wert enthält. Die Größe des Zeiger Werts hängt von dem Betriebssystem ab, das zum Protokollieren des Ereignisses verwendet wird. die Nutzlast enthält einen 4-Byte-Wert für 32-Bit-Systeme oder einen 8-Byte-Wert für 64-Bit-Systeme. Der MOF-Datentyp muss ein <strong>Objekt</strong>sein.</p>
<p>Consumer sollten den Datentyp und den <strong>Format</strong> Qualifizierer ignorieren, wenn die-Eigenschaft die <strong>sizet</strong> -Erweiterung enthält. Um die Größe der Daten zu ermitteln, die für die Eigenschaft gelesen werden sollen, verwenden Sie Folgendes:</p>
<ul>
<li>Der <strong>pointersize</strong> -Member von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Der <strong>Flags</strong> -Member von <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<p><strong>Vor Windows Vista:</strong> Der Wert für " <strong>pointersize</strong> " ist möglicherweise nicht korrekt. Auf einem 64-Bit-Computer protokolliert z. b. eine 32-Bit-Anwendung 4-Byte-Zeiger. in der Sitzung wird jedoch " <strong>pointersize</strong> " auf 8 festgelegt.</p>
<p>Beachten Sie, dass einige Ereignisse <strong>PointerType</strong> anstelle eines <strong>Zeigers</strong>verwenden. Verwenden Sie <strong>PointerType</strong>nicht.</p></td>
</tr>
<tr class="even">
<td><strong>Stringbeendigung</strong></td>
<td>Gibt an, wie die Zeichen folgen Eigenschaft beendet wird. Beispielsweise bedeutet stringbeendigung ( &quot; nullterminiert), dass &quot; die Zeichen folgen Eigenschaft NULL-terminiert ist. Dabei sind folgende Werte möglich:
<dl> <dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>Gewertet</strong></dt> <dd>
<p>Die Länge der Zeichenfolge wird als <strong>UShort</strong> -Wert am Anfang der Zeichenfolge eingebettet.</p>
</dd> <dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>Nicht gezählt</strong></dt> <dd>
<p>Die Zeichenfolge ist nicht NULL-terminiert, und die Länge der Zeichenfolge wird nicht am Anfang der Zeichenfolge eingebettet. In diesem Fall sollte die Zeichenfolge das letzte Element sein und den gesamten Raum bis zum Ende der Ereignisdaten belegen.</p>
</dd> <dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>NullTerminated</strong></dt> <dd>
<p>Die Zeichenfolge wird mit Null beendet. Wenn Sie den <strong>stringbeendigung</strong> -Qualifizierer nicht angeben, wird davon ausgegangen, dass die Zeichenfolge mit NULL endet.</p>
</dd> <dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>Reverumgezählt</strong></dt> <dd>
<p>Die Länge der Zeichenfolge wird als <strong>UShort</strong> -Wert im Big-Endian-Format am Anfang der Zeichenfolge eingebettet.</p>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Valuebeschreibungen</strong></td>
<td>Stellt Beschreibungen für jeden Wert im <strong>Values</strong> -Qualifizierer bereit. Die Funktionen " <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>tdhenenerateproviderfieldinformation</strong></a> " und " <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>tdhqueryproviderfieldinformation</strong></a> " geben diese Beschreibungen zurück, wenn Sie versuchen, Schlüsselwort-und levelinformationen abzurufen. Die Beschreibungen sind optional. Wenn Sie die Beschreibungen nicht angeben, geben die Funktionen <strong>null</strong>zurück. Weitere Informationen finden Sie unter <a href="#specifying-level-and-enable-flags-values-for-a-provider">Angeben von Werten für Ebene und Aktivierungsflags für einen Anbieter</a> .</td>
</tr>
<tr class="even">
<td><strong>ValueMap</strong></td>
<td>Gibt die ganzzahligen Index-oder Flagwerte an, die Zeichen folgen Werten zugeordnet werden. Wenn Sie diesen Qualifizierer angeben, müssen Sie auch den <strong>Values</strong> -Qualifizierer und optional den <strong>ValueType</strong> -Qualifizierer angeben. Beachten Sie, dass etw die WMI-Option der Verwendung von Zeichen folgen für Werte Zuordnungs Werte nicht unterstützt.
<p>Im folgenden Beispiel wird die Verwendung der ValueMap-, Values-und ValueType-Qualifizierer veranschaulicht.</p>
<pre class="syntax" data-space="preserve"><code>ValueType(&quot;flag&quot;),
ValueMap {&quot;0x01&quot;, &quot;0x02&quot;, &quot;0x04&quot;, &quot;0x08&quot;},
Values {&quot;ValueMapFlag1&quot;, &quot;ValueMapFlag2&quot;, &quot;ValueMapFlag4&quot;, &quot;ValueMapFlag8&quot;}]</code></pre></td>
</tr>
<tr class="odd">
<td><strong>Werte</strong></td>
<td>Zeichen folgen Werte. Wenn auch der <strong>ValueMap</strong> -Qualifizierer angegeben wird, entsprechen die Zeichen folgen direkt den Werten im <strong>ValueMap</strong> -Qualifizierer. Nehmen Sie andernfalls an, dass der Eigenschafts Wert ein NULL basierter Index in den Wert Zeichenfolgen ist.</td>
</tr>
<tr class="even">
<td><strong>ValueType</strong></td>
<td>Gibt an, ob die <strong>ValueMap</strong> -Werte ganzzahlige Indexwerte oder bitflagwerte sind. Wenn Sie diesen Qualifizierer nicht angeben, werden ganzzahlige Indexwerte angenommen. Verwenden Sie ValueType (Index), um anzugeben, dass die Werte ganzzahlige Indexwerte sind &quot; &quot; . Verwenden Sie ValueType (Flag), um anzugeben, dass es sich bei den Werten um Bitflag-Werte handelt &quot; &quot; .</td>
</tr>
<tr class="odd">
<td><strong>Wmidataid</strong></td>
<td>Jede Eigenschaft muss den <strong>wmidataid</strong> -Qualifizierer enthalten. <strong>Wmidataid</strong> definiert die Reihenfolge, in der der Consumer die Ereignisdaten liest. Der Wert für <strong>wmidataid</strong> beginnt bei 1 und Inkrementen für jede Eigenschaft in der Klasse. Beispielsweise wmidataid (1).</td>
</tr>
<tr class="even">
<td><strong>XMLFragment</strong></td>
<td>Gibt an, dass die Daten im XML-Format vorliegen und ohne weitere Formatierung angezeigt werden können.</td>
</tr>
</tbody>
</table>



 

## <a name="specifying-level-and-enable-flags-values-for-a-provider"></a>Angeben von Werten für Ebene und Aktivierungsflags für einen Anbieter

Um die Ebenen und Aktivierungsflags zu dokumentieren, die ein Controller zum Aktivieren des Anbieters verwendet, fügen Sie die Eigenschaften "Level" und "Flags" in die MOF-Klasse des Anbieters ein. Bei den Eigenschaftsnamen für die Ebene und die Flags wird die groß- Die Eigenschaften müssen die **Werte** und **ValueMap** -Qualifizierer enthalten, die die möglichen Werte für Ebene und Aktivierungsflag angeben. Die **ValueMap** für die Werte zum Aktivieren des Flags muss Bitwerte (Flagwerte) sein. Der **valuebeschreibungen** -Qualifizierer ist optional, sollte jedoch verwendet werden, um Beschreibungen für jeden möglichen Wert bereitzustellen. Die Beschreibungen werden verwendet, wenn eine Person die Funktionen " [**tdhenenerateproviderfieldinformation**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) " und " [**tdhqueryproviderfieldinformation**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) " aufruft, um die möglichen Ebenen zu erhalten und Flags (Schlüsselwörter) für den Anbieter zu aktivieren.

Im folgenden Beispiel wird eine Anbieter Klasse gezeigt, die die möglichen Werte für Ebene und Aktivierungsflags angibt.

``` syntax
[Dynamic,
 Description("IIS_Trace") : amended,
 guid("{3a2a4e84-4c21-4981-ae10-3fda0d9b0f83}"),
 locale("MS\\0x409")]
class IIS_Trace : EventTrace
{
    [Description ("Enable Flags") : amended,
        ValueDescriptions{
             "Allow_tracing_only_selected_requests ",
             "IIS_authentication_events ",
             "IIS_security_events ",
             "IIS_filter_events ",
             "IIS_static_file_events ",
             "IIS_CGI_events ",
             "IIS_compression_events ",
             "IIS_cache_events ",
             "IIS_request_notifications_events ",
             "IIS_module_events ",
             "IIS_FastCGI_events "},
        DefineValues{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        Values{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        ValueMap{
             "0x00000001",
             "0x00000002",
             "0x00000004",
             "0x00000008",
             "0x00000010",
             "0x00000020",
             "0x00000040",
             "0x00000080",
             "0x00000100",
             "0x00000200",
             "0x00001000"}: amended
    ]
    uint32 Flags;

    [Description ("Levels") : amended,
        ValueDescriptions{
            "Abnormal exit or termination",
            "Severe errors that need logging",
            "Warnings such as allocation failure",
            "Includes non-error cases",
            "Detailed traces from intermediate steps" } : amended,
         DefineValues{
            "TRACE_LEVEL_FATAL",
            "TRACE_LEVEL_ERROR",
            "TRACE_LEVEL_WARNING"
            "TRACE_LEVEL_INFORMATION",
            "TRACE_LEVEL_VERBOSE" },
        Values{
            "Fatal",
            "Error",
            "Warning",
            "Information",
            "Verbose" },
        ValueMap{
            "0x1",
            "0x2",
            "0x3",
            "0x4",
            "0x5" },
        ValueType("index")
    ]
    uint32 Level;
};
```

 

 
