---
description: Verwenden Sie die in diesem Abschnitt definierten Qualifizierer, wenn Sie die MOF-Anbieterklasse, die MOF-Ereignisklasse, die MOF-Ereignisklasse und die Eigenschaften der MOF-Ereignisklasse erstellen.
ms.assetid: 3bc82074-05a7-411f-884f-5da1fd08112b
title: MOF-Qualifizierer für die Ereignisablaufverfolgung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 578699b04c5ba2d0f39afb2e8ff5141151bd208b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628439"
---
# <a name="event-tracing-mof-qualifiers"></a>MOF-Qualifizierer für die Ereignisablaufverfolgung

Verwenden Sie die in diesem Abschnitt definierten Qualifizierer, wenn Sie die [MOF-Anbieterklasse,](#provider-mof-class-qualifiers)die [MOF-Ereignisklasse,](#event-mof-class-qualifiers)die [MOF-Ereignisklasse](#event-type-mof-class-qualifiers)und [die Eigenschaften der MOF-Ereignisklasse](#property-qualifiers)erstellen. Ein Beispiel, das einige dieser Qualifizierer enthält, finden Sie unter [Veröffentlichen ihres Ereignisschemas.](publishing-your-event-schema.md)

## <a name="provider-mof-class-qualifiers"></a>Anbieter-MOF-Klassenqualifizierer

In der folgenden Tabelle sind die Qualifizierer aufgeführt, die Sie für eine MOF-Anbieterklasse angeben können.



| Qualifizierer | Datentyp  | Beschreibung                                                                                                                                                                                                                                                  |
|-----------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**  | **String** | Erforderlich. Zeichenfolgen-GUID, die einen Anbieter eindeutig identifiziert. Beispiel: Guid("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Dies ist die gleiche GUID, die Sie verwenden, wenn Sie die [**RegisterTraceGuids-Funktion**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) aufrufen, um Ihren Anbieter zu registrieren. |



 

## <a name="event-mof-class-qualifiers"></a>Mof-Ereignisklassenqualifizierer

In der folgenden Tabelle sind die Qualifizierer aufgeführt, die Sie für eine Ereignisklasse angeben können (die übergeordnete Klasse, die verwandte Ereignistypklassen gruppiert).

| Qualifizierer        | Datentyp   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**         | **String**  | Erforderlich. Zeichenfolgen-GUID, die eine Klasse von Ereignissen identifiziert. Beispiel: Guid("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Ereignisanbieter verwenden die GUID, um den [**EVENT \_ TRACE HEADER \_ festzulegen. Guid-Member,**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) sodass Consumer die Klasse der empfangenen Ereignisse bestimmen können.                                                                                                                                                                                                                                                                                  |
| **EventVersion** | **Integer** | Dieser Qualifizierer ist für die neueste Version einer Ereignisablaufverfolgungsklasse optional und für alle älteren Versionen der -Klasse erforderlich. Die neueste Version der -Klasse gibt entweder nicht den **EventVersion-Qualifizierer** an oder hat die höchste Versionsnummer. Versionsnummern beginnen mit 0, z.B. EventVersion(0). Wenn Sie eine neue Version der -Klasse erstellen, benennen Sie in der Regel auch die vorherige Version in <classname> \_ Vn um, wobei n eine inkrementelle Zahl ist, die bei 0 beginnt. Ein Beispiel finden Sie unter [**FileIo**](fileio.md) und [**FileIo \_ V0.**](fileio-v0.md)<br/> |



 

## <a name="event-type-mof-class-qualifiers"></a>MOF-Klassenqualifizierer des Ereignistyps

In der folgenden Tabelle sind die Qualifizierer aufgeführt, die Sie für eine Ereignistypklasse angeben können (die Klasse, die die Ereigniseigenschaftsdaten definiert).



| Qualifizierer         | Wert       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EventType**     | **Integer** | Erforderlich. Identifiziert die Ereignistypklasse. Beispiel: EventType(1). Der Ereignisanbieter verwendet den gleichen Ereignistypwert, um [**EVENT \_ TRACE HEADER \_ festzulegen. Class.Type**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header). Wenn dieselbe MOF-Klasse für mehrere Ereignistypen verwendet wird (da sie die gleichen Ereignisdaten verwenden), geben Sie den Ereignistypwert als Array von ganzen Zahlen an, z. {12,15} B. EventType. |
| **EventTypeName** | **String**  | Optional. Beschreibt den Ereignistyp. Beispiel: EventTypeName("Start"). Wenn dieselbe MOF-Klasse für mehrere Ereignistypen verwendet wird (da sie die gleichen Ereignisdaten verwenden), geben Sie den Wert des Ereignistypnamens als Zeichenfolgenarray an, z. B. EventTypeName{"Start", "End"}. Die Elemente des EventTypeName-Arrays entsprechen direkt dem EventType-Array.                 |



 

## <a name="property-qualifiers"></a>Eigenschaftsqualifizierer

In der folgenden Tabelle sind die Qualifizierer aufgeführt, die Sie für eine Eigenschaft angeben können.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Qualifizierer</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Bitmap</strong></td>
<td>Gibt die Bitpositionen an, die Zeichenfolgenwerten zugeordnet werden. Wenn Sie diesen Qualifizierer angeben, müssen Sie auch den <strong>BitValues-Qualifizierer</strong> angeben.</td>
</tr>
<tr class="even">
<td><strong>BitValues</strong></td>
<td>Zeichenfolgenwerte. Wenn <strong></strong> auch der BitMap-Qualifizierer angegeben wird, entsprechen die Zeichenfolgen direkt den Werten im BitMap-Qualifizierer. <strong></strong> Andernfalls wird davon ausgegangen, dass der Eigenschaftswert ein einsbasierter Index in die Wertzeichenfolgen ist (Bit 1 entspricht der ersten Zeichenfolge in der Liste).</td>
</tr>
<tr class="odd">
<td><strong>Erweiterung</strong></td>
<td>Stellt zusätzliche Informationen zur Verwendung (Interpretation) der Daten bereit. Beim Erweiterungswert wird die Groß-/Kleinschreibung nicht beachtet. Fügen Sie den Wert in Anführungszeichen ein, z. B. Extension( &quot; GUID &quot; ). Mögliche Erweiterungswerte sind: <dl> <dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>Guid</dt> <dd> Gibt an, dass die Eigenschaftsdaten eine GUID sind. Der MOF-Datentyp muss <strong>objekt</strong>sein. Es wird erwartet, dass es sich bei der Nutzlast um eine <strong>GUID-Struktur</strong> handelt.<br/> </dd> <dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>IPAddr und IPAddrV4</dt> <dd> Bei den Daten handelt es sich um eine IP V4-Adresse. Der MOF-Datentyp muss <strong>objekt</strong>sein. Es wird erwartet, dass die Nutzlast eine Länge ohne Vorzeichen hat. Jedes Byte der Länge ohne Vorzeichen stellt einen der vier Teile der IP-Adresse (p1.p2.p3.p4) dar. Das Low-Order-Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 usw.<br/> <strong>Vor Windows Vista:</strong> Die Erweiterung IPAddrV4 wird nicht unterstützt.<br/> </dd> <dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> <dd> Bei den Daten handelt es sich um eine IP V6-Adresse. Der MOF-Datentyp muss <strong>objekt</strong>sein. Es wird erwartet, dass es sich bei der Nutzlast um eine <strong>IN6_ADDR-Struktur</strong> handelt. <br/> <strong>Vor Windows Vista:</strong> Die Erweiterung IPAddrV6 wird nicht unterstützt.<br/> </dd> <dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>NoPrint</dt> <dd> Gibt an, dass der Consumer diese Daten nicht drucken soll.<br/> </dd> <dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>Hafen</dt> <dd> Die Daten identifizieren eine Portnummer. Der MOF-Datentyp muss <strong>objekt</strong>sein. Es wird erwartet, dass es sich bei der Nutzlast um eine kurz ohne Vorzeichen handelt.<br/> </dd> <dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RString</dt> <dd> Neue Zeichen wurden durch Leerzeichen ersetzt. Es wird erwartet, dass es sich bei der Nutzlast um eine NULL-terminierte ANSI-Zeichenfolge handelt.<br/> </dd> <dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>RWString</dt> <dd> Neue Zeichen wurden durch Leerzeichen ersetzt. Es wird erwartet, dass es sich bei der Nutzlast um eine auf NULL endende Zeichenfolge mit Breitzeichen handelt.<br/> </dd> <dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</dt> <dd> Die Daten stellen eine binäre Blob-SID dar. Der MOF-Datentyp muss <strong>objekt</strong>sein. <br/> Die SID hat eine variable Länge. Der Wert, der in den ersten 4 Bytes<strong>(ULONG)</strong>enthalten ist, gibt an, ob das Blob eine SID enthält. Wenn die ersten 4 Bytes<strong>(ULONG)</strong>des Blobs ungleich 0 (null) sind, enthält das Blob eine SID. Der erste Teil des Blobs enthält die TOKEN_USER (die Struktur wird an einer 8-Byte-Grenze ausgerichtet), und der zweite Teil enthält die SID. So beheben Sie den SID-Teil des Blobs:<br/>
<ul>
<li>Festlegen eines Bytezeigers auf den Anfang des Blobs</li>
<li>Multiplizieren Sie die Zeigergröße für das Ereignisprotokoll mit 2, und fügen Sie das Produkt dem Bytezeiger hinzu (der <strong>PointerSize-Member</strong> von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> enthält den Zeigergrößenwert).</li>
</ul>
<br/> Sie können das folgende Makro verwenden, um die Länge der SID zu bestimmen. <br/>
<pre class="syntax" data-space="preserve"><code>#define SeLengthSid( Sid ) \
  (8 + (4 * ((SID *)Sid)->SubAuthorityCount))</code></pre>
</dd> <dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> <dd> Gibt an, dass die -Eigenschaft einen Zeigerwert enthält. Die Größe des Zeigerwerts hängt vom Betriebssystem ab, das zum Protokollieren des Ereignisses verwendet wird. Die Nutzlast enthält einen 4-Byte-Wert für 32-Bit-Systeme oder einen 8-Byte-Wert für 64-Bit-Systeme. Der MOF-Datentyp muss <strong>objekt</strong>sein.<br/> Consumer sollten den Datentyp und den <strong>Formatqualifizierer</strong> ignorieren, wenn die Eigenschaft die <strong>SizeT-Erweiterung</strong> enthält. Verwenden Sie Folgendes, um die Größe der Daten zu bestimmen, die für die Eigenschaft gelesen werden sollen:
<ul>
<li>Der <strong>PointerSize-Member</strong> von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li><strong>Flags-Member</strong> von <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<br/> <strong>Vor Windows Vista:</strong> Der <strong>PointerSize-Wert</strong> ist möglicherweise nicht genau. Beispielsweise protokolliert eine 32-Bit-Anwendung auf einem 64-Bit-Computer 4-Byte-Zeiger. Die Sitzung legt <strong>PointerSize</strong> jedoch auf 8 fest.<br/> </dd> <dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>Variante</dt> <dd> Die Daten stellen ein Blob dar. Die ersten vier Bytes (uint32) geben die Größe des Blobs an. Der MOF-Datentyp muss <strong>objekt</strong>sein. <br/> </dd> <dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>Wmitime</dt> <dd> Übersetzt den Zeitstempel in die Systemzeit. Der MOF-Datentyp muss <strong>objekt</strong>sein. Es wird erwartet, dass die Nutzlast eine 64-Bit-Ganzzahl ohne Vorzeichen ist.<br/> <strong>Vor Windows Vista:</strong> Nicht verfügbar.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Format</strong></td>
<td>Definiert das Format der Eigenschaftsdaten. Wenn z. B. Format( &quot; w ) in eine Zeichenfolgeneigenschaft eingeschlossen &quot; wird, bedeutet dies, dass die Zeichenfolge eine breite Zeichenfolge ist. Mögliche Werte:
<table>
<thead>
<tr class="header">
<th>Begriff</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="c"></span><span id="C"></span>C<br/></td>
<td>Zeigt den Eigenschaftswert als ASCII-Zeichen an. Sie können diesen Qualifizierer mit <strong>uint8-Datentypen</strong> verwenden.<br/></td>
</tr>
<tr class="even">
<td><span id="s"></span><span id="S"></span>s<br/></td>
<td>Behandeln Sie das Array von Zeichen als auf NULL endende Zeichenfolge. Die Zeichenfolge ist eine Breitzeichenfolge, wenn der Datentyp <strong>char16</strong>ist. Andernfalls ist die Zeichenfolge eine ASCII-Zeichenfolge.<br/></td>
</tr>
<tr class="odd">
<td><span id="w"></span><span id="W"></span>W<br/></td>
<td>Der Eigenschaftswert ist eine Zeichenfolge mit Breitzeichen. Sie können diesen Qualifizierer mit <strong>Zeichenfolgendatentypen</strong> verwenden. <br/></td>
</tr>
<tr class="even">
<td><span id="x"></span><span id="X"></span>X<br/></td>
<td>Zeigt den Eigenschaftswert als Hexadezimalzahl an. Sie können diesen Qualifizierer mit 16-, 32- und 64-Bit-Ganzzahldatentypen verwenden.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><strong>Zeiger</strong></td>
<td><p>Gibt an, dass die -Eigenschaft einen Zeigerwert enthält. Die Größe des Zeigerwerts hängt vom Betriebssystem ab, das zum Protokollieren des Ereignisses verwendet wird. Die Nutzlast enthält einen 4-Byte-Wert für 32-Bit-Systeme oder einen 8-Byte-Wert für 64-Bit-Systeme. Der MOF-Datentyp muss <strong>objekt</strong>sein.</p>
<p>Consumer sollten den Datentyp und den <strong>Formatqualifizierer</strong> ignorieren, wenn die Eigenschaft die <strong>SizeT-Erweiterung</strong> enthält. Verwenden Sie Folgendes, um die Größe der Daten zu bestimmen, die für die Eigenschaft gelesen werden sollen:</p>
<ul>
<li>Der <strong>PointerSize-Member</strong> von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li><strong>Flags-Member</strong> von <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<p><strong>Vor Windows Vista:</strong> Der <strong>PointerSize-Wert</strong> ist möglicherweise nicht genau. Beispielsweise protokolliert eine 32-Bit-Anwendung auf einem 64-Bit-Computer 4-Byte-Zeiger. Die Sitzung legt <strong>PointerSize</strong> jedoch auf 8 fest.</p>
<p>Beachten Sie, dass einige Ereignisse <strong>PointerType</strong> anstelle von <strong>Pointer</strong>verwenden. verwenden Sie nicht <strong>PointerType.</strong></p></td>
</tr>
<tr class="even">
<td><strong>StringTermination</strong></td>
<td>Gibt an, wie die Zeichenfolgeneigenschaft beendet wird. StringTermination( NullTerminated ) gibt beispielsweise &quot; &quot; an, dass die Zeichenfolgeneigenschaft NULL-terminiert ist. Mögliche Werte:
<dl> <dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>Gezählt</strong></dt> <dd>
<p>Die Länge der Zeichenfolge wird am Anfang der Zeichenfolge als <strong>USHORT-Wert</strong> eingebettet.</p>
</dd> <dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>Nicht gezählt</strong></dt> <dd>
<p>Die Zeichenfolge ist nicht NULL-terminiert, und die Länge der Zeichenfolge wird nicht am Anfang der Zeichenfolge eingebettet. In diesem Fall sollte die Zeichenfolge das letzte Element sein und den gesamten Platz bis zum Ende der Ereignisdaten belegen.</p>
</dd> <dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>Nullterminated</strong></dt> <dd>
<p>Die Zeichenfolge ist NULL-terminiert. Wenn Sie den <strong>StringTermination-Qualifizierer</strong> nicht angeben, wird davon ausgegangen, dass die Zeichenfolge NULL-terminiert ist.</p>
</dd> <dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>ReverseCounted</strong></dt> <dd>
<p>Die Länge der Zeichenfolge wird am Anfang der Zeichenfolge als <strong>USHORT-Wert</strong> im Big-Endian-Format eingebettet.</p>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ValueDescriptions</strong></td>
<td>Stellt Beschreibungen für jeden Wert im <strong>Qualifizierer Werte</strong> bereit. Die Funktionen <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>TdhEnumerateProviderFieldInformation</strong></a> und <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>TdhQueryProviderFieldInformation</strong></a> geben diese Beschreibungen zurück, wenn Sie versuchen, Schlüsselwort- und Ebeneninformationen abzurufen. Die Beschreibungen sind optional. Wenn Sie die Beschreibungen nicht angeben, geben die Funktionen <strong>NULL</strong>zurück. Weitere Informationen finden Sie unter <a href="#specifying-level-and-enable-flags-values-for-a-provider">Angeben von Ebenen- und Aktivierungsflagswerten für einen Anbieter.</a></td>
</tr>
<tr class="even">
<td><strong>ValueMap</strong></td>
<td>Gibt den ganzzahligen Index oder die Flagwerte an, die Zeichenfolgenwerten zugeordnet sind. Wenn Sie diesen Qualifizierer angeben, <strong></strong> müssen Sie auch den Values-Qualifizierer und optional den <strong>ValueType-Qualifizierer</strong> angeben. Beachten Sie, dass ETW die WMI-Option für Zeichenfolgen für Wertzuordnungswerte nicht unterstützt.
<p>Das folgende Beispiel zeigt die Verwendung der ValueMap-, Values- und ValueType-Qualifizierer.</p>
<pre class="syntax" data-space="preserve"><code>ValueType(&quot;flag&quot;),
ValueMap {&quot;0x01&quot;, &quot;0x02&quot;, &quot;0x04&quot;, &quot;0x08&quot;},
Values {&quot;ValueMapFlag1&quot;, &quot;ValueMapFlag2&quot;, &quot;ValueMapFlag4&quot;, &quot;ValueMapFlag8&quot;}]</code></pre></td>
</tr>
<tr class="odd">
<td><strong>Werte</strong></td>
<td>Zeichenfolgenwerte. Wenn <strong></strong> auch der ValueMap-Qualifizierer angegeben wird, entsprechen die Zeichenfolgen direkt den Werten im <strong>ValueMap-Qualifizierer.</strong> Andernfalls wird davon ausgegangen, dass der Eigenschaftswert ein nullbasierter Index in die Wertzeichenfolgen ist.</td>
</tr>
<tr class="even">
<td><strong>ValueType</strong></td>
<td>Gibt an, ob die <strong>ValueMap-Werte</strong> ganzzahlige Indexwerte oder Bitflagwerte sind. Wenn Sie diesen Qualifizierer nicht angeben, werden ganzzahlige Indexwerte angenommen. Um anzugeben, dass es sich bei den Werten um ganzzahlige Indexwerte handelt, verwenden Sie ValueType( &quot; index &quot; ). Um anzugeben, dass es sich bei den Werten um Bitflagwerte handelt, verwenden Sie ValueType( &quot; flag &quot; ).</td>
</tr>
<tr class="odd">
<td><strong>WmiDataId</strong></td>
<td>Jede Eigenschaft muss den <strong>WmiDataId-Qualifizierer</strong> enthalten. <strong>WmiDataId</strong> definiert die Reihenfolge, in der der Consumer die Ereignisdaten liest. Der Wert für <strong>WmiDataId</strong> beginnt bei 1 und erhöht sich für jede Eigenschaft in der -Klasse. Beispiel: WmiDataId(1).</td>
</tr>
<tr class="even">
<td><strong>XMLFragment</strong></td>
<td>Gibt an, dass die Daten im XML-Format vorliegen und ohne weitere Formatierung angezeigt werden können.</td>
</tr>
</tbody>
</table>



 

## <a name="specifying-level-and-enable-flags-values-for-a-provider"></a>Angeben der Ebene und Aktivieren von Flagwerten für einen Anbieter

Um die Ebenen- und Aktivierungsflags zu dokumentieren, die ein Controller zum Aktivieren Ihres Anbieters verwenden würde, schließen Sie die Eigenschaften "Level" und "Flags" in die MOF-Klasse Ihres Anbieters ein. Bei den Eigenschaftsnamen Level und Flags wird die Groß-/Kleinschreibung beachtet. Die Eigenschaften müssen die **Qualifizierer Values** und **ValueMap** enthalten, die die mögliche Ebene angeben und Flagwerte aktivieren. Die **ValueMap** für die Enable-Flagwerte muss Bitwerte (Flagwerte) sein. Der **ValueDescriptions-Qualifizierer** ist optional. Sie sollten ihn jedoch verwenden, um Beschreibungen für jeden möglichen Wert bereitzustellen. Die Beschreibungen werden verwendet, wenn jemand die Funktionen [**TdhEnumerateProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) und [**TdhQueryProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) aufruft, um die mögliche Ebene abzurufen und Flagwerte (Schlüsselwörter) für den Anbieter zu aktivieren.

Das folgende Beispiel zeigt eine Anbieterklasse, die die mögliche Ebene angibt und Flagwerte aktiviert.

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

 

 
