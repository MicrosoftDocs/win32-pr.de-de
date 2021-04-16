---
title: Nachrichten Compiler (MC.exe)
description: Wird verwendet, um Instrumentierungs Manifeste und Nachrichtentext Dateien zu kompilieren.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- Message Compiler-Ereignisprotokoll (MC.exe)
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 5eb852dcbb13800705db0a0f19d912de899f9b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524240"
---
# <a name="message-compiler-mcexe"></a>Nachrichten Compiler (MC.exe)

Wird verwendet, um Instrumentierungs Manifeste und Nachrichtentext Dateien zu kompilieren. Der Compiler generiert die Nachrichten Ressourcen Dateien, mit denen Ihre Anwendung verknüpft ist.

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [Argumente, die sowohl für Meldungs Textdateien als auch für Manifest-Dateien](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [Spezifische Argumente für Manifest-Dateien](#arguments-specific-to-manifest-files)
-   [Argumente, die zum Erstellen von Code verwendet werden, den Ihr Anbieter zum Protokollieren von Ereignissen verwendet](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [Spezifische Argumente für Meldungs Textdateien](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a>Argumente, die sowohl für Meldungs Textdateien als auch für Manifest-Dateien

<dl> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Zeigt die Verwendungs Informationen für den Nachrichten Compiler an.

</dd> <dt>

<span id="-c"></span><span id="-C"></span>**-c**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler das Customer-Bit (Bit 28) in allen Nachrichten-IDs festlegen muss. Weitere Informationen zum Kunden Bit finden Sie unter Winerror. h.

</dd> <dt>

<span id="-cp"></span><span id="-CP"></span>**-CP-** *Codierung*
</dt> <dd>

Verwenden Sie dieses Argument, um die Zeichencodierung anzugeben, die für alle generierten Textdateien verwendet wird. Gültige Namen sind "ANSI" (Standard), "UTF-8" und "UTF-16". Die Unicode-Codierungen fügen eine Byte Reihenfolge-Markierung hinzu.

</dd> <dt>

<span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e-** *Erweiterung*
</dt> <dd>

Verwenden Sie dieses Argument, um die Erweiterung anzugeben, die für die Header Datei verwendet werden soll. Sie können bis zu drei Zeichen ohne den Zeitraum angeben. Der Standardwert ist. h.

</dd> <dt>

<span id="-h_path"></span><span id="-H_PATH"></span>**-h** *Pfad*
</dt> <dd>

Verwenden Sie dieses Argument, um den Ordner anzugeben, in dem der Compiler die generierte Header Datei platzieren soll. Der Standardwert ist das aktuelle Verzeichnis.

</dd> <dt>

<span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *Länge*
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler eine Warnung generiert, wenn eine beliebige Nachricht die *Länge* von Zeichen überschreitet.

</dd> <dt>

<span id="-r_path"></span><span id="-R_PATH"></span>**-r-** *Pfad*
</dt> <dd>

Verwenden Sie dieses Argument, um den Ordner anzugeben, in dem der Compiler das generierte ressourcencompilerskript (RC-Datei) und die generierten. bin-Dateien (binäre Ressourcen) platzieren soll, die das ressourcencompilerskript enthält. Der Standardwert ist das aktuelle Verzeichnis.

</dd> <dt>

<span id="-z_name"></span><span id="-Z_NAME"></span>**-z-** *Name*
</dt> <dd>

Verwenden Sie dieses Argument, um den Standardbasis Namen zu überschreiben, den der Compiler für die generierten Dateien verwendet. Standardmäßig wird der Basisname der Datei *Namen* -Eingabedatei verwendet.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Die Datei oder Meldungs Textdatei des Instrumentierungs Manifests. Die Datei muss im aktuellen Verzeichnis vorhanden sein. Sie können eine Manifest-Datei, eine Meldungs Textdatei oder beides angeben. Der Dateiname muss die Erweiterung enthalten. Die Konvention besteht in der Verwendung einer. man-Erweiterung für Manifest-Dateien und der Erweiterung ". MC" für Meldungs Textdateien.

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a>Spezifische Argumente für Manifest-Dateien

<dl> <dt>

<span id="-s_path"></span><span id="-S_PATH"></span>**-s-** *Pfad*
</dt> <dd>

Verwenden Sie dieses Argument, um eine Baseline Ihrer Instrumentierung zu erstellen. Geben Sie den Pfad zum Ordner an, in dem sich die grundlegenden Manifest-Dateien befinden. Bei nachfolgenden Releases verwenden Sie das Argument **-t** , um das neue Manifest anhand der Baseline auf Kompatibilitätsprobleme zu überprüfen.

**Vor MC-Version 1.12.7051:** Nicht verfügbar

</dd> <dt>

<span id="-t_path"></span><span id="-T_PATH"></span>**-t** *Pfad*
</dt> <dd>

Verwenden Sie dieses Argument, wenn Sie eine neue Version des Manifests erstellen und es auf die Anwendungs Kompatibilität mit der Baseline überprüfen möchten, die Sie mit dem **-s-** Argument erstellt haben. Der Pfad muss auf den Ordner verweisen, der enthält. BIN-Dateien, die der baselinevorgang erstellt hat (siehe Schalter **-s** ).

**Vor MC-Version 1.12.7051:** Nicht verfügbar

</dd> <dt>

<span id="-w_path"></span><span id="-W_PATH"></span>**-w** *Pfad*
</dt> <dd>

Der Compiler ignoriert dieses Argument und überprüft das Manifest automatisch.

**Vor MC-Version 1.12.7051:** Verwenden Sie dieses Argument, um den Ordner anzugeben, der die Schema Datei "eventman. xsd" enthält, die der Compiler verwendet, um das Manifest zu validieren. Der Windows SDK schließt die Schema Datei "eventman. xsd" in den \\ includeordner ein. Wenn Sie dieses Argument nicht angeben, überprüft der Compiler das Manifest nicht.

</dd> <dt>

<span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *Pfad*
</dt> <dd>

Der Compiler ignoriert dieses Argument.

**Vor MC-Version 1.12.7051:** Verwenden Sie dieses Argument, um den Ordner anzugeben, der die Winmeta.xml Datei enthält. Die Winmeta.xml-Datei enthält die erkannten Eingabe-und Ausgabetypen sowie die vordefinierten Kanäle, Ebenen und OpCodes. Die Windows SDK enthält die Winmeta.xml Datei im \\ Ordner include.

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a>Argumente, die zum Erstellen von Code verwendet werden, den Ihr Anbieter zum Protokollieren von Ereignissen verwendet

Sie können die folgenden compilerargumente verwenden, um Kernel Modus-oder Benutzermoduscode zu generieren, den Sie zum Protokollieren von Ereignissen verwenden können. Sie können auch anfordern, dass der Compiler Code generiert, um das Schreiben von Ereignissen auf Computern vor Windows Vista zu unterstützen. Wenn die Anwendung in c# geschrieben ist, kann der Compiler eine c#-Klasse generieren, die Sie zum Protokollieren von Ereignissen verwenden können. Diese Argumente sind ab der MC-Version 1.12.7051 verfügbar, die mit der Windows 7-Version des Windows SDK ausgeliefert wird.

<dl> <dt>

<span id="-co"></span><span id="-CO"></span>**-Co**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Protokollierungs Dienst die benutzerdefinierte Funktion für jedes Ereignis aufruft, das Sie protokollieren (die Funktion wird aufgerufen, nachdem das Ereignis protokolliert wurde). Die benutzerdefinierte Funktion muss über die folgende Signatur verfügen.


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



Sie müssen auch die folgende-Direktive in Ihren Code einschließen.

`#define MCGEN_CALLOUT pFnUserFunction`

Sie sollten Ihre Implementierung so kurz wie möglich halten, um Protokollierungs Probleme zu vermeiden. der Dienst protokolliert Ihre Ereignisse nicht mehr, bis die Funktion zurückgegeben wird.

Sie können dieses Argument mit dem **-km-** oder **-um-** Argument verwenden.

</dd> <dt>

<span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-CS-** *Namespace*
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler eine c#-Klasse generiert, die auf der .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) -Klasse basiert.

</dd> <dt>

<span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-CSS-** *Namespace*
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler eine statische c#-Klasse generiert, die auf der .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) -Klasse basiert.

</dd> <dt>

<span id="-km"></span><span id="-KM"></span>**-km**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler den Kernelmoduscode generiert, mit dem die im Manifest definierten Ereignisse protokolliert werden.

</dd> <dt>

<span id="-mof"></span><span id="-MOF"></span>**-MOF**
</dt> <dd>

Veraltet. Verwenden Sie dieses Argument, damit der Compiler Code generiert, den Sie zum Protokollieren von Ereignissen auf Computern vor Windows Vista verwenden können. Mit dieser Option wird auch eine MOF-Datei erstellt, die die MOF-Klassen für jedes im Manifest definierte Ereignis enthält. Um die Klassen in der MOF-Datei zu registrieren, damit Consumer die Ereignisse decodieren können, verwenden Sie den MOF-Compiler (Mofcomp.exe). Ausführliche Informationen zur Verwendung des MOF-Compilers finden Sie unter [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).

Wenn Sie diesen Switch verwenden möchten, müssen Sie die folgenden Einschränkungen einhalten:

-   Jede Ereignis Definition muss die Attribute "Task" und "Opcode" enthalten.
-   Jeder Task muss das eventguid-Attribut enthalten.
-   Die Vorlagen Daten, auf die das Ereignis verweist, dürfen Folgendes nicht enthalten:
    -   Datenelemente, die die Eingabetypen Win: binary oder Win: SYSTEMTIME angeben
    -   Strukturen
    -   Arrays mit variabler Größenanpassung; Sie können jedoch Arrays mit fester Länge angeben.
    -   Zeichen folgen-Datentypen können das length-Attribut nicht angeben

Sie müssen dieses Argument mit dem **-um-**, **-CS**-, **-CSS**-oder **-km** -Argument verwenden.

</dd> <dt>

<span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p-** *Präfix*
</dt> <dd>

Verwenden Sie dieses Argument, um das Standard Präfix zu überschreiben, das der Compiler für die Protokollierungs Makronamen und Methodennamen verwendet. Das Standard Präfix ist "EventWrite". Die Zeichenfolge beachtet die Groß-/Kleinschreibung.

Sie können dieses Argument mit dem **-um-**, **-CS**-, **-CSS**-oder **-km** -Argument verwenden.

</dd> <dt>

<span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P-** *Präfix*
</dt> <dd>

Verwenden Sie dieses Argument, um Zeichen vom Anfang des symbolischen Namens zu entfernen, den Sie für das Ereignis angegeben haben. Bei dem Vergleich wird Groß- und Kleinschreibung nicht unterschieden. Der Compiler verwendet den symbolischen Namen, um die Namen der Protokollierungs Makros und Methodennamen zu bilden.

Der Standardname für ein Protokollierungs Makro ist EventWrite *Symbolname*, wobei *Symbolname* der symbolische Name ist, den Sie für das Ereignis angegeben haben. Wenn Sie z. b. das Symbol Attribut des Ereignisses auf printerconnection festlegen, wäre der Makro Name EventWrite teprinterconnection. Wenn Sie den Drucker aus dem Namen entfernen möchten, verwenden Sie den **-P-** **Drucker**, der "EventWrite Connection" ergibt.

Sie können dieses Argument mit dem **-um-**, **-CS**-, **-CSS**-oder **-km** -Argument verwenden.

</dd> <dt>

<span id="-um"></span><span id="-UM"></span>**-um**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler den Benutzermoduscode generiert, mit dem die im Manifest definierten Ereignisse protokolliert werden.

</dd> </dl>

Damit der Compiler Protokollierungs Code generieren kann, müssen Sie das **-um**-, **-CS**-, **-CSS**-oder **-km** -Argument angeben. Diese Argumente schließen sich gegenseitig aus.

Um anzugeben, wo die vom Compiler generierten h-, CS-und MOF-Dateien abgelegt werden sollen, verwenden Sie das Argument **-h** . Wenn Sie das **-h-** Argument nicht angeben, werden die Dateien in den aktuellen Ordner eingefügt.

Verwenden Sie das Argument **-r** , um anzugeben, wo die RC-Datei und Binärdateien (die die Metadatenressourcen enthalten), die der Compiler generiert, platziert werden sollen. Wenn Sie das Argument **-r** nicht angeben, werden die Dateien in den aktuellen Ordner eingefügt.

Der Compiler verwendet den Basis Namen der Eingabedatei als Basis Namen für die generierten Dateien. Um einen Basisnamen anzugeben, verwenden Sie das **-z-** Argument.

### <a name="arguments-specific-to-message-text-files"></a>Spezifische Argumente für Meldungs Textdateien

<dl> <dt>

<span id="-a"></span><span id="-A"></span>**-a**
</dt> <dd>

Verwenden Sie dieses Argument, um anzugeben, dass die Datei *Namen* -Eingabedatei Inhalt in der System Standard-Windows-ANSI-Codepage (CP_ACP) enthält. Dies ist die Standardoption. Verwenden Sie **-u** für Unicode. Wenn die Eingabedatei eine BOM enthält, wird dieses Argument ignoriert.

</dd> <dt>

<span id="-A"></span><span id="-a"></span>**-A**
</dt> <dd>

Veraltet. Verwenden Sie dieses Argument, um anzugeben, dass die Nachrichten in der Datei Output. bin ANSI lauten sollen.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>**-b**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler den Basis Namen der Datei *Namen-Eingabedatei* für die. bin-Dateinamen verwendet. Der Standardwert ist die Verwendung von "msg".

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Verwenden Sie dieses Argument, um Dezimalwerte für den Schweregrad und die Anlagen Konstanten in der Header Datei anstelle von hexadezimalen Werten zu verwenden.

</dd> <dt>

<span id="-n"></span><span id="-N"></span>**-n**
</dt> <dd>

Verwenden Sie dieses Argument, um anzugeben, dass Nachrichten unmittelbar nach dem Nachrichtentext beendet werden. Der Standardwert ist das Beenden des Nachrichten Texts mit CR/LF.

</dd> <dt>

<span id="-o"></span><span id="-O"></span>**-o**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler eine OLE2-Header Datei mithilfe von **HRESULT** -Definitionen anstelle von Statuscodes generiert. Die Verwendung von Statuscodes ist die Standardeinstellung.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>**-u**
</dt> <dd>

Verwenden Sie dieses Argument, um anzugeben, dass die Eingabedatei des *Datei namens* UTF-16LE-Inhalt enthält. Der Standardwert ist ANSI-Inhalt. Wenn die Eingabedatei eine BOM enthält, wird dieses Argument ignoriert.

</dd> <dt>

<span id="-U"></span><span id="-u"></span>**-U**
</dt> <dd>

Verwenden Sie dieses Argument, um anzugeben, dass die Nachrichten in der Datei Output. bin Unicode lauten sollen. Dies ist die Standardoption.

</dd> <dt>

<span id="-v"></span><span id="-V"></span>**-v**
</dt> <dd>

Verwenden Sie dieses Argument, um die ausführliche Ausgabe zu generieren.

</dd> <dt>

<span id="-x_path"></span><span id="-X_PATH"></span>**-x-** *Pfad*
</dt> <dd>

Verwenden Sie dieses Argument, um den Ordner anzugeben, in dem der Compiler die dbg-C-Includedatei platzieren soll. Die dbg-Datei ordnet den symbolischen Namen Nachrichten-IDs zu.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Argumente " **-A** " und " **-MOF** " sind veraltet und werden in Zukunft entfernt.

Der Compiler akzeptiert als Eingabe eine Manifest-Datei (. man) oder eine Nachrichtentext Datei (. MC) und generiert die folgenden Dateien:

-   *Dateiname*. h

    Eine C/C++-Header Datei, die die Ereignis Deskriptoren, die Anbieter-GUID und Symbolnamen enthält, auf die in der Anwendung verwiesen wird.

-   *Dateiname* Temp. bin

    Eine binäre Ressourcen Datei, die den Anbieter und die Ereignis Metadaten enthält. Dies ist die Vorlagen Ressource, die durch das Temp-Suffix des Basis namens der Datei gekennzeichnet ist.

-   Msg00001. bin

    Eine binäre Ressourcen Datei für jede Sprache, die Sie angeben (z. b. wenn das Manifest Nachrichten Zeichenfolgen in "en-US" und "fr-FR" enthält), generiert der Compiler "Msg00001. bin" und "Msg00002. bin".

-   *Dateiname*. RC

    Ein ressourcencompilerskript, das die Anweisungen enthält, mit denen die einzelnen bin-Dateien als Ressource eingeschlossen werden.

Bei Argumenten, die einen Pfad annehmen, kann der Pfad ein absoluter, relativer oder UNC-Pfad sein, und er kann Umgebungsvariablen enthalten.

**Vor MC-Version 1.12.7051:** Der Compiler lässt keine relativen Pfade oder Umgebungsvariablen zu.

Der Windows SDK schließt den Compiler (mc.exe) in den \\ bin-Ordner ein.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Manifest mithilfe der compilerstandardwerte kompiliert.

``` syntax
mc spooler.man
```

Im folgenden Beispiel wird das Manifest kompiliert und die Header-und Ressourcen Dateien in den angegebenen Ordnern platziert.

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 2000 Professional \[nur Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 2000 Server \[nur Desktop-Apps\]       |
