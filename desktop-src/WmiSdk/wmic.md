---
description: Das WMI-Befehlszeilenprogramm (WMIC) stellt eine Befehlszeilenschnittstelle für WMI bereit.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0248ea4ac6a584816da20e8feb8d278d7feab0a018739fa4328c3023179d4b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921000"
---
# <a name="wmic"></a>wmic

Das WMI-Befehlszeilenprogramm (WMIC) stellt eine Befehlszeilenschnittstelle für die Windows Management Instrumentation (WMI) bereit. WMIC ist mit vorhandenen Shells und Hilfsprogrammbefehlen kompatibel. Im Folgenden finden Sie ein allgemeines Referenzthema für WMIC. Weitere Informationen und Richtlinien zur Verwendung von WMIC, einschließlich zusätzlicher Informationen zu Aliasen, Verben, Switches und Befehlen, finden Sie unter [Using Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).

## <a name="alias"></a>Alias

Ein Alias ist eine benutzerfreundliche Umbenennung einer Klasse, Eigenschaft oder Methode, die die Verwendung und das Lesen von WMI vereinfacht. Sie können ermitteln, welche Aliase für WMIC über /? verfügbar **sind.** ausführen. Sie können die Aliase für eine bestimmte Klasse auch mithilfe von **<className> /? bestimmen.** ausführen. Weitere Informationen finden Sie unter [WMIC-Aliase.](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10))

## <a name="switch"></a>Schalter

Ein Switch ist eine WMIC-Option, die Sie global oder optional festlegen können. Eine Liste der verfügbaren Switches finden Sie unter [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verben

Um Verben in WMIC zu verwenden, geben Sie den Aliasnamen gefolgt vom Verb ein. Wenn ein Alias kein Verb unterstützt, erhalten Sie die Meldung "Der Anbieter ist nicht in der Lage, den versuchten Vorgang zu versuchen". Weitere Informationen finden Sie unter [WMIC-Verben.](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10))

Die meisten Aliase unterstützen die folgenden Verben.

<dl> <dt>

<span id="ASSOC"></span><span id="assoc"></span>Assoc
</dt> <dd>

Gibt das Ergebnis der Abfrage zurück, `Associators of (<wmi_object>)` *wobei<\_ wmi->* der Pfad von Objekten ist, die von den **PATH-** oder **CLASS-Befehlen zurückgegeben** werden. Die Ergebnisse sind Instanzen, die dem -Objekt zugeordnet sind. Wenn ASSOC mit einem Alias verwendet wird, werden die Klassen zurückgegeben, deren Klasse dem Alias zugrunde liegt. Standardmäßig wird die Ausgabe im HTML-Format zurückgegeben.

Das ASSOC-Verb verfügt über die folgenden Schalter.



| Schalter                         | BESCHREIBUNG                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS:<classname> | Zurückgegebene Endpunkte, die dem Quellobjekt zugeordnet sind, müssen zur angegebenen Klasse gehören oder von ihr abgeleitet werden.      |
| /RESULTROLE:<rolename>   | Zurückgegebene Endpunkte müssen in Zuordnungen mit dem Quellobjekt eine bestimmte Rolle spielen.                              |
| /ASSOCCLASS:<assocclass> | Zurückgegebene Endpunkte müssen der Quelle über die angegebene Klasse oder eine ihrer abgeleiteten Klassen zugeordnet werden. |



 

Beispiel: **OS ASSOC**

</dd> <dt>

<span id="CALL"></span><span id="call"></span>Aufrufen
</dt> <dd>

Führt eine Methode aus.

Beispiel: **DIENST WHERE CAPTION='TELNET' CALL STARTSERVICE**

> [!Note]  
> Verwenden Sie /? , um die für eine bestimmte Klasse verfügbaren **Methoden zu bestimmen.** Beispiel: **SERVICE WHERE CAPTION='TELNET' CALL /?** listet die verfügbaren Funktionen für die Dienstklasse auf.

 

</dd> <dt>

<span id="CREATE"></span><span id="create"></span>Erstellen
</dt> <dd>

Erstellt eine neue -Instanz und legt die Eigenschaftswerte fest. CREATE kann nicht verwendet werden, um eine neue Klasse zu erstellen.

Beispiel: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>Löschen
</dt> <dd>

Löscht die aktuelle Instanz oder den Satz von -Instanzen. DELETE kann verwendet werden, um eine Klasse zu löschen.

Beispiel: **PROCESS WHERE NAME="CALC.EXE" DELETE**

</dd> <dt>

<span id="GET"></span><span id="get"></span>Erhalten
</dt> <dd>

Ruft bestimmte Eigenschaftswerte ab.

GET verfügt über die folgenden Schalter.



| Schalter                               | BESCHREIBUNG                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | Die Ausgabe wird mit jedem Wert formatiert, der in einer separaten Zeile und mit dem Namen der Eigenschaft aufgeführt ist.                                           |
| /ALL                                 | Die Ausgabe wird als Tabelle formatiert.                                                                                                            |
| /TRANSLATE:<translation table> | Übersetzen Sie die Ausgabe mithilfe der Übersetzungstabelle, die durch den Befehl benannt wird. Die Übersetzungstabellen BasicXml und NoComma sind in WMIC enthalten. |
| /EVERY:<interval>              | Wiederholen Sie den Befehl alle <interval> Sekunden.                                                                                         |
| /FORMAT:<format specifier>     | Gibt ein Schlüsselwort oder einen XSL-Dateinamen zum Formatieren der Daten an.                                                                                  |



 

Beispiel: **PROCESS GET NAME**

</dd> <dt>

<span id="LIST"></span><span id="list"></span>Liste
</dt> <dd>

Zeigt Daten an. LIST ist das Standardverb.

LIST verfügt über die folgenden Adverbs.



| Adverb   | BESCHREIBUNG                                                  |
|----------|--------------------------------------------------------------|
| KURZ    | Kernsatz der Eigenschaften.                                  |
| FULL     | Vollständiger Satz von Eigenschaften. Dies ist der Standard-Adverb für LIST. |
| INSTANCE | Nur Instanzpfade.                                         |
| STATUS   | Status der Objekte.                                       |
| SYSTEM   | Systemeigenschaften.                                           |



 

LIST verfügt über die folgenden Schalter.



| Schalter                               | BESCHREIBUNG                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /TRANSLATE:<translation table> | Übersetzen Sie die Ausgabe mithilfe der Übersetzungstabelle, die durch den Befehl benannt wird. Die Übersetzungstabellen BasicXml und NoComma sind in WMIC enthalten. |
| /EVERY:<interval>              | Wiederholen Sie den Befehl alle <interval> Sekunden.                                                                                         |
| /FORMAT:<format specifier>     | Gibt ein Schlüsselwort oder einen XSL-Dateinamen zum Formatieren der Daten an.                                                                                  |



 

Beispiel: **PROCESS LIST BRIEF**

</dd> <dt>

<span id="SET"></span><span id="set"></span>Festgelegt
</dt> <dd>

Weist Eigenschaften Werte zu. Beispiel: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**

</dd> </dl>

## <a name="switches"></a>Optionen

Globale Switches werden verwendet, um Standardwerte für die WMIC-Umgebung festzulegen. Sie können den aktuellen Wert der von diesen Schaltern festgelegten Bedingungen anzeigen, indem Sie den **CONTEXT-Befehl** eingeben.

<dl> <dt>

<span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE
</dt> <dd>

Namespace, den der Alias in der Regel verwendet. Der Standardwert ist root \\ cimv2.

Beispiel: **/NAMESPACE: \\ \\ root**

</dd> <dt>

<span id="_ROLE"></span><span id="_role"></span>/ROLE
</dt> <dd>

Namespace-WMIC sucht in der Regel nach Aliasen und anderen WMIC-Informationen.

Beispiel: **/ROLE: \\ \\ root**

</dd> <dt>

<span id="_NODE"></span><span id="_node"></span>/NODE
</dt> <dd>

Computernamen, durch Kommas getrennt. Alle Befehle werden für alle in diesem Wert aufgeführten Computer synchron ausgeführt. Dateinamen müssen & vorangestellt werden. Computernamen innerhalb einer Datei müssen durch Kommas oder in separaten Zeilen getrennt sein.

</dd> <dt>

<span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL
</dt> <dd>

Identitätswechselebene.

Beispiel: **/IMPLEVEL:Anonymous**

</dd> <dt>

<span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL
</dt> <dd>

Authentifizierungsebene.

Beispiel: **/AUTHLEVEL:Pkt**

</dd> <dt>

<span id="_LOCALE"></span><span id="_locale"></span>/LOCALE
</dt> <dd>

Locale.

Beispiel: **/LOCALE:MS \_ 411**

</dd> <dt>

<span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES
</dt> <dd>

Aktivieren oder deaktivieren Sie alle Berechtigungen.

Beispiel: **/PRIVILEGES:ENABLE** oder **/PRIVILEGES:DISABLE**

</dd> <dt>

<span id="_TRACE"></span><span id="_trace"></span>/TRACE
</dt> <dd>

Zeigt den Erfolg oder Fehler aller Funktionen an, die zum Ausführen von WMIC-Befehlen verwendet werden.

Beispiel: **/TRACE:ON** oder **/TRACE:OFF**

</dd> <dt>

<span id="_RECORD"></span><span id="_record"></span>/RECORD
</dt> <dd>

Zeichnet die gesamte Ausgabe in einer XML-Datei auf. Die Ausgabe wird auch an der Eingabeaufforderung angezeigt.

Beispiel: **/RECORD:** _MyOutput.xml_

</dd> <dt>

<span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE
</dt> <dd>

In der Regel werden Löschbefehle bestätigt.

Beispiel: **/INTERACTIVE:ON** oder **/INTERACTIVE:OFF**

</dd> <dt>

<span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on** \| **off** \| *TimeoutInMilliseconds*
</dt> <dd>

Bei ON werden die /NODE-Computer vor dem Senden von WMIC-Befehlen an sie gepingt. Wenn ein Computer nicht reagiert, werden die WMIC-Befehle nicht an ihn gesendet.

Beispiel: "/FAILFAST:ON" oder "/FAILFAST:OFF"

**WMIC /FAILFAST:1000**

</dd> <dt>

<span id="_USER"></span><span id="_user"></span>/USER
</dt> <dd>

Benutzername, der von WMIC beim Zugriff auf die /NODE-Computer oder -Computer verwendet wird, die in den Aliasen angegeben sind. Sie werden aufgefordert, das Kennwort einzugeben. Ein Benutzername kann nicht mit dem lokalen Computer verwendet werden.

Beispiel: **/USER:**_JSMITH_

</dd> <dt>

<span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD
</dt> <dd>

Kennwort, das von WMIC beim Zugriff auf die /NODE-Computer verwendet wird. Das Kennwort wird in der Befehlszeile angezeigt.

Beispiel: **/PASSWORD:**_password_

</dd> <dt>

<span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT
</dt> <dd>

Gibt einen Modus für die gesamte Ausgabeumleitung an. Die Ausgabe wird nicht in der Befehlszeile angezeigt, und das Ziel wird gelöscht, bevor die Ausgabe beginnt. Gültige Werte sind STDOUT, CLIPBOARD oder ein Dateiname.

Beispiel: **/OUTPUT:CLIPBOARD**

</dd> <dt>

<span id="_APPEND"></span><span id="_append"></span>/APPEND
</dt> <dd>

Gibt einen Modus für die gesamte Ausgabeumleitung an. Die Ausgabe wird nicht in der Befehlszeile angezeigt, und das Ziel wird nicht gelöscht, bevor die Ausgabe beginnt und die Ausgabe an das Ende des aktuellen Inhalts des Ziels angefügt wird. Gültige Werte sind STDOUT, CLIPBOARD oder ein Dateiname.

Beispiel: **/APPEND:CLIPBOARD**

</dd> <dt>

<span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE
</dt> <dd>

Wird mit dem Schalter **LIST** und **GET /EVERY** verwendet. Wenn AGGREGATE auf ON festgelegt ist, zeigen LIST und GET ihre Ergebnisse an, wenn alle Computer in /NODE entweder geantwortet haben oder ein Time out aufgetreten sind. Wenn AGGREGATE auf OFF gesetzt ist, werden die Ergebnisse von LIST und GET angezeigt, sobald sie empfangen werden.

Beispiel: **/AGGREGATE:OFF** oder **/AGGREGATE:ON**

</dd> </dl>

## <a name="commands"></a>Befehle

Die folgenden WMIC-Befehle sind jederzeit verfügbar. Weitere Informationen finden Sie unter [WMIC-Befehle.](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10))

<dl> <dt>

<span id="CLASS"></span><span id="class"></span>Klasse
</dt> <dd>

Escape aus dem Standardaliasmodus von WMIC, um direkt auf Klassen im WMI-Schema zuzugreifen. Weitere Informationen zu verfügbaren WMI-Klassen finden Sie unter [WMI-Klassen.](wmi-classes.md)

Beispiel: **WMIC /OUTPUT:c: \\ClassOutput.htm CLASS Win32 \_ SoundDevice**

</dd> <dt>

<span id="PATH"></span><span id="path"></span>Pfad
</dt> <dd>

Escape aus dem Standardaliasmodus von WMIC, um direkt auf Instanzen im WMI-Schema zuzugreifen.

Beispiel: **WMIC /OUTPUT:c: \\PathOutput.txt PATH Win32 \_ SoundDevice GET /VALUE**

</dd> <dt>

<span id="CONTEXT"></span><span id="context"></span>Kontext
</dt> <dd>

Zeigt die aktuellen Werte aller globalen Switches an.

Beispiel: **WMIC CONTEXT**

</dd> <dt>

<span id="QUIT"></span><span id="quit"></span>Beenden
</dt> <dd>

Beenden Sie WMIC.

Beispiel: **WMIC QUIT**

</dd> <dt>

<span id="EXIT"></span><span id="exit"></span>Ausfahrt
</dt> <dd>

Beenden Sie WMIC.

Beispiel: **WMIC EXIT**

</dd> </dl>

## <a name="examples"></a>Beispiele

Das [Skript zum Festlegen von IP/Subnetz/Gateway/DNS mithilfe des WMIC-Beispiels](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) im TechNet-Katalog beschreibt das Ändern und Aktualisieren von IP-, Subnetz-, Gateway- und DNS-Einstellungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

