---
title: Nachrichtencompiler (MC.exe)
description: Wird zum Kompilieren von Instrumentierungsmanifesten und Meldungstextdateien verwendet.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- Message Compiler (MC.exe) EventLog
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 1ba213a1d7047b61ba7ba875adf9c281726eaae123ae018aea9920050b201644
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470940"
---
# <a name="message-compiler-mcexe"></a>Nachrichtencompiler (MC.exe)

Wird zum Kompilieren von Instrumentierungsmanifesten und Meldungstextdateien verwendet. Der Compiler generiert die Nachrichtenressourcendateien, mit denen Ihre Anwendung verknüpft ist.

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [Argumente, die sowohl für Nachrichtentextdateien als auch für Manifestdateien gelten](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [Spezifische Argumente für Manifestdateien](#arguments-specific-to-manifest-files)
-   [Argumente für das Generieren von Code, den Ihr Anbieter zum Protokollieren von Ereignissen verwenden würde](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [Argumente, die für Nachrichtentextdateien spezifisch sind](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a>Argumente, die sowohl für Nachrichtentextdateien als auch für Manifestdateien gelten

<dl> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Zeigt die Nutzungsinformationen für den Nachrichtencompiler an.

</dd> <dt>

<span id="-c"></span><span id="-C"></span>**-c**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler das Kundenbit (Bit 28) in allen Nachrichten-IDs festgelegt hat. Informationen zum Kundenbit finden Sie unter winerror.h.

</dd> <dt>

<span id="-cp"></span><span id="-CP"></span>**-cp-Codierung** 
</dt> <dd>

Verwenden Sie dieses Argument, um die Zeichencodierung anzugeben, die für alle generierten Textdateien verwendet wird. Gültige Namen sind "ansi" (Standard), "utf-8" und "utf-16". Die Unicode-Codierungen fügen eine Bytereihenfolgemarkierung hinzu.

</dd> <dt>

<span id="-e_extension"></span><span id="-E_EXTENSION"></span> *-e-Erweiterung*
</dt> <dd>

Verwenden Sie dieses Argument, um die Erweiterung anzugeben, die für die Headerdatei verwendet werden soll. Sie können bis zu einer Erweiterung mit drei Zeichen angeben, ohne den Punkt einzuschließt. Der Standardwert ist .h.

</dd> <dt>

<span id="-h_path"></span><span id="-H_PATH"></span>**-h** *Pfad*
</dt> <dd>

Verwenden Sie dieses Argument, um den Ordner anzugeben, in dem der Compiler die generierte Headerdatei speichern soll. Der Standardwert ist das aktuelle Verzeichnis.

</dd> <dt>

<span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *Länge*
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler eine Warnung generiert, wenn eine Nachricht *die Länge* von Zeichen überschreitet.

</dd> <dt>

<span id="-r_path"></span><span id="-R_PATH"></span>**-r-Pfad** 
</dt> <dd>

Verwenden Sie dieses Argument, um den Ordner anzugeben, in dem der Compiler das generierte Ressourcencompilerskript (RC-Datei) und die generierten BIN-Dateien (binäre Ressourcen) platzieren soll, die das Ressourcencompilerskript enthält. Der Standardwert ist das aktuelle Verzeichnis.

</dd> <dt>

<span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *Name*
</dt> <dd>

Verwenden Sie dieses Argument, um den Standardbasisnamen zu überschreiben, den der Compiler für die generierten Dateien verwendet. Standardmäßig wird der Basisname der *Dateinamen-Eingabedatei* verwendet.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Dateiname*
</dt> <dd>

Die Instrumentierungsmanifestdatei oder Meldungstextdatei. Die Datei muss im aktuellen Verzeichnis vorhanden sein. Sie können eine Manifestdatei, eine Nachrichtentextdatei oder beides angeben. Der Dateiname muss die Erweiterung enthalten. Die Konvention besteht darin, eine MAN-Erweiterung für Manifestdateien und eine MC-Erweiterung für Nachrichtentextdateien zu verwenden.

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a>Spezifische Argumente für Manifestdateien

<dl> <dt>

<span id="-s_path"></span><span id="-S_PATH"></span>**-s-Pfad** 
</dt> <dd>

Verwenden Sie dieses Argument, um eine Baseline Ihrer Instrumentierung zu erstellen. Geben Sie den Pfad zu dem Ordner an, der die Basismanifestdateien enthält. Für nachfolgende Releases verwenden Sie dann das Argument **-t,** um das neue Manifest anhand der Baseline auf Kompatibilitätsprobleme zu überprüfen.

**Vor MC-Version 1.12.7051:** Nicht verfügbar

</dd> <dt>

<span id="-t_path"></span><span id="-T_PATH"></span>**-t** *Pfad*
</dt> <dd>

Verwenden Sie dieses Argument, wenn Sie eine neue Version Des Manifests erstellen und es auf Anwendungskompatibilität mit der Baseline überprüfen möchten, die Sie mit dem Argument **-s** erstellt haben. Der Pfad muss auf den Ordner zeigen, der enthält. BIN-Dateien, die vom Baselinevorgang erstellt wurden (siehe Schalter **-s).**

**Vor MC-Version 1.12.7051:** Nicht verfügbar

</dd> <dt>

<span id="-w_path"></span><span id="-W_PATH"></span>**-w** *pfad*
</dt> <dd>

Der Compiler ignoriert dieses Argument und überprüft automatisch das Manifest.

**Vor MC-Version 1.12.7051:** Verwenden Sie dieses Argument, um den Ordner anzugeben, der die Schemadatei Eventman.xsd enthält, die der Compiler zum Überprüfen des Manifests verwendet. Das Windows SDK enthält die Schemadatei Eventman.xsd im \\ Ordner Include. Wenn Sie dieses Argument nicht angeben, überprüft der Compiler das Manifest nicht.

</dd> <dt>

<span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W-Pfad** 
</dt> <dd>

Der Compiler ignoriert dieses Argument.

**Vor MC-Version 1.12.7051:** Verwenden Sie dieses Argument, um den Ordner anzugeben, der die Winmeta.xml Datei enthält. Die Winmeta.xml-Datei enthält die erkannten Eingabe- und Ausgabetypen sowie die vordefinierten Kanäle, Ebenen und Opcodes. Das Windows SDK enthält die Winmeta.xml-Datei im \\ Ordner Include.

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a>Argumente für das Generieren von Code, den Ihr Anbieter zum Protokollieren von Ereignissen verwenden würde

Sie können die folgenden Compilerargumente verwenden, um Kernelmodus- oder Benutzermoduscode zu generieren, den Sie zum Protokollieren von Ereignissen verwenden können. Sie können auch anfordern, dass der Compiler Code generiert, um das Schreiben von Ereignissen auf Computern vor Windows Vista zu unterstützen. Wenn Ihre Anwendung in C# geschrieben ist, kann der Compiler eine C#-Klasse generieren, die Sie zum Protokollieren von Ereignissen verwenden können. Diese Argumente sind ab MC-Version 1.12.7051 verfügbar, die mit der Windows 7-Version des Window SDK ausgeliefert wird.

<dl> <dt>

<span id="-co"></span><span id="-CO"></span>**-co**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Protokollierungsdienst Ihre benutzerdefinierte Funktion für jedes Ereignis aufruft, das Sie protokollieren (die Funktion wird aufgerufen, nachdem das Ereignis protokolliert wurde). Ihre benutzerdefinierte Funktion muss über die folgende Signatur verfügen.


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



Sie müssen auch die folgende -Direktive in Ihren Code einschließen.

`#define MCGEN_CALLOUT pFnUserFunction`

Sie sollten Ihre Implementierung so kurz wie möglich halten, um Protokollierungsprobleme zu vermeiden. Der Dienst protokolliert Ihre Ereignisse erst dann, wenn die Funktion zurückgegeben wird.

Sie können dieses Argument mit dem Argument **-km** oder **-um** verwenden.

</dd> <dt>

<span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs-Namespace** 
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler eine C#-Klasse basierend auf der .NET 3.5 [EventProvider-Klasse](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) generiert.

</dd> <dt>

<span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css-Namespace** 
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler eine statische C#-Klasse basierend auf der [EventProvider-Klasse](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) von .NET 3.5 generiert.

</dd> <dt>

<span id="-km"></span><span id="-KM"></span>**-km**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler den Kernelmoduscode generiert, den Sie zum Protokollieren der im Manifest definierten Ereignisse verwenden würden.

</dd> <dt>

<span id="-mof"></span><span id="-MOF"></span>**-mof**
</dt> <dd>

Veraltet. Verwenden Sie dieses Argument, damit der Compiler Code generiert, mit dem Sie Ereignisse auf Computern vor Windows Vista protokollieren können. Mit dieser Option wird auch eine MOF-Datei erstellt, die die MOF-Klassen für jedes im Manifest definierte Ereignis enthält. Verwenden Sie den MOF-Compiler (Mofcomp.exe), um die Klassen in der MOF-Datei zu registrieren, damit Consumer die Ereignisse decodieren können. Ausführliche Informationen zur Verwendung des MOF-Compilers finden Sie unter [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).

Um diesen Schalter verwenden zu können, müssen Sie die folgenden Einschränkungen einhalten:

-   Jede Ereignisdefinition muss die Attribute task und opcode enthalten.
-   Jede Aufgabe muss das attribut eventGuid enthalten.
-   Die Vorlagendaten, auf die die Ereignisverweise verweisen, dürfen Folgendes nicht enthalten:
    -   Datenelemente, die die Eingabetypen win:Binary oder win:SYSTEMTIME angeben
    -   Strukturen
    -   Arrays variabler Größe; Sie können jedoch Arrays fester Länge angeben.
    -   Zeichenfolgendatentypen können das Length-Attribut nicht angeben.

Sie müssen dieses Argument mit dem Argument **-um,** **-cs,** **-css** oder **-km** verwenden.

</dd> <dt>

<span id="-p_prefix"></span><span id="-P_PREFIX"></span> *-p-Präfix*
</dt> <dd>

Verwenden Sie dieses Argument, um das Standardpräfix zu überschreiben, das der Compiler für die Namen der Protokollierungsmakros und Methodennamen verwendet. Das Standardpräfix ist "EventWrite". Die Zeichenfolge beachtet die Groß-/Kleinschreibung.

Sie können dieses Argument mit dem Argument **-um**, **-cs**, **-css** oder **-km** verwenden.

</dd> <dt>

<span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span> *-P-Präfix*
</dt> <dd>

Verwenden Sie dieses Argument, um Zeichen vom Anfang des symbolischen Namens zu entfernen, den Sie für das Ereignis angegeben haben. Bei dem Vergleich wird Groß- und Kleinschreibung nicht unterschieden. Der Compiler verwendet den symbolischen Namen, um die Protokollierungsmakronamen und Methodennamen zu bilden.

Der Standardname für ein Protokollierungsmakro ist EventWrite *SymbolName,* wobei *SymbolName* der symbolische Name ist, den Sie für das Ereignis angegeben haben. Wenn Sie beispielsweise das Symbolattribut des Ereignisses auf PrinterConnection festlegen, würde der Makroname EventWritePrinterConnection sein. Um Printer aus dem Namen zu entfernen, verwenden Sie **-P** **Printer,** was zu EventWriteConnection führt.

Sie können dieses Argument mit dem **Argument -um,** **-cs,** **-css** oder **-km** verwenden.

</dd> <dt>

<span id="-um"></span><span id="-UM"></span>**-um**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler den Benutzermoduscode generiert, den Sie zum Protokollieren der in Ihrem Manifest definierten Ereignisse verwenden würden.

</dd> </dl>

Damit der Compiler Protokollierungscode generieren kann, müssen Sie das **Argument -um,** **-cs,** **-css** oder **-km angeben.** diese Argumente schließen sich gegenseitig aus.

Verwenden Sie das -h-Argument, um anzugeben, wo die vom Compiler generierten H-, CS- und **MOF-Dateien gespeichert werden.** Wenn Sie das Argument **-h nicht angeben,** werden die Dateien im aktuellen Ordner abgelegt.

Verwenden Sie das **Argument -r,** um anzugeben, wo die RC-Datei und binäre Dateien gespeichert werden (die die Metadatenressourcen enthalten), die der Compiler generiert. Wenn Sie das Argument **-r nicht** angeben, werden die Dateien im aktuellen Ordner abgelegt.

Der Compiler verwendet den Basisnamen der Eingabedatei als Basisnamen der generierten Dateien. Verwenden Sie das Argument **-z,** um einen Basisnamen anzugeben.

### <a name="arguments-specific-to-message-text-files"></a>Spezifische Argumente für Nachrichtentextdateien

<dl> <dt>

<span id="-a"></span><span id="-A"></span>**-a**
</dt> <dd>

Verwenden Sie dieses Argument, um anzugeben, dass die *Dateinameneingabedatei* Inhalt in der standardmäßigen SYSTEM-Windows ANSI-Codepage (CP_ACP) enthält. Dies ist die Standardoption. Verwenden **Sie -u** für Unicode. Wenn die Eingabedatei eine BOM enthält, wird dieses Argument ignoriert.

</dd> <dt>

<span id="-A"></span><span id="-a"></span>**-A**
</dt> <dd>

Veraltet. Verwenden Sie dieses Argument, um anzugeben, dass die Nachrichten in der BIN-Ausgabedatei ANSI sein sollen.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>**-b**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler den Basisnamen der *Dateinameneingabedatei* für die BIN-Dateinamen verwendet. Standardmäßig wird "MSG" verwendet.

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Verwenden Sie dieses Argument, um Dezimalwerte für die Schweregrad- und Facility-Konstanten in der Headerdatei anstelle von Hexadezimalwerten zu verwenden.

</dd> <dt>

<span id="-n"></span><span id="-N"></span>**-n**
</dt> <dd>

Verwenden Sie dieses Argument, um anzugeben, dass Nachrichten unmittelbar nach dem Nachrichtentext beendet werden. Standardmäßig wird der Nachrichtentext mit einer CR/LF beendet.

</dd> <dt>

<span id="-o"></span><span id="-O"></span>**-o**
</dt> <dd>

Verwenden Sie dieses Argument, damit der Compiler eine OLE2-Headerdatei **mithilfe von HRESULT-Definitionen** anstelle von Statuscodes generiert. Die Verwendung von Statuscodes ist die Standardeinstellung.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>**-u**
</dt> <dd>

Verwenden Sie dieses Argument, um anzugeben, dass *die Dateinameneingabedatei* UTF-16LE-Inhalt enthält. Der Standardwert ist ANSI-Inhalt. Wenn die Eingabedatei eine BOM enthält, wird dieses Argument ignoriert.

</dd> <dt>

<span id="-U"></span><span id="-u"></span>**-U**
</dt> <dd>

Verwenden Sie dieses Argument, um anzugeben, dass die Nachrichten in der BIN-Ausgabedatei Unicode sein sollen. Dies ist die Standardoption.

</dd> <dt>

<span id="-v"></span><span id="-V"></span>**-v**
</dt> <dd>

Verwenden Sie dieses Argument, um eine ausführliche Ausgabe zu generieren.

</dd> <dt>

<span id="-x_path"></span><span id="-X_PATH"></span>**-x-Pfad** 
</dt> <dd>

Verwenden Sie dieses Argument, um den Ordner anzugeben, in dem der Compiler die DBG-C-Includedatei platzieren soll. Die DBG-Datei ordnet Nachrichten-IDs ihren symbolischen Namen zu.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Argumente -A** **und -mof** sind veraltet und werden in Zukunft entfernt.

Der Compiler akzeptiert als Eingabe eine Manifestdatei (MAN) oder eine Meldungstextdatei (.mc) und generiert die folgenden Dateien:

-   *Dateiname*.h

    Eine C/C++-Headerdatei, die die Ereignisdeskriptoren, anbieter-GUID und Symbolnamen enthält, auf die Sie in Ihrer Anwendung verweisen.

-   *Dateiname* TEMP.bin

    Eine binäre Ressourcendatei, die die Anbieter- und Ereignismetadaten enthält. Dies ist die Vorlagenressource, die durch das TEMP-Suffix des Basisnamens der Datei bezeichnet wird.

-   Msg00001.bin

    Eine binäre Ressourcendatei für jede sprache, die Sie angeben (wenn Ihr Manifest z. B. Meldungszeichenfolgen in en-US und fr-FR enthält, generiert der Compiler "Msg00001.bin" und "Msg00002.bin").

-   *Dateiname*.rc

    Ein Ressourcencompilerskript, das die Anweisungen enthält, die jede BIN-Datei als Ressource enthalten.

Bei Argumenten, die einen Pfad verwenden, kann der Pfad ein absoluter, relativer oder UNC-Pfad sein und Umgebungsvariablen enthalten.

**Vor MC-Version 1.12.7051:** Der Compiler lässt keine relativen Pfade oder Umgebungsvariablen zu.

Das Windows SDK enthält den Compiler (mc.exe) im \\ Ordner Bin.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Manifest mithilfe der Compiler-Standardwerte kompiliert.

``` syntax
mc spooler.man
```

Im folgenden Beispiel wird das Manifest kompiliert und die Header- und Ressourcendateien in den angegebenen Ordnern platziert.

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 2000 Professional \[nur Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 2000 Server \[nur Desktop-Apps\]       |
