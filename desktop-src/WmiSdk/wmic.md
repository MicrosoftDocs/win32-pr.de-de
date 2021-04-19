---
description: Das WMI-Befehlszeilen Hilfsprogramm (WMIC) stellt eine Befehlszeilenschnittstelle für WMI bereit.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070b21cb21381fb989b81795a6c7e0b787b5c89a
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222928"
---
# <a name="wmic"></a>wmic

Das WMI-Befehlszeilen Hilfsprogramm (WMIC) stellt eine Befehlszeilenschnittstelle für Windows-Verwaltungsinstrumentation (WMI) bereit. WMIC ist kompatibel mit vorhandenen Shells und Utility-Befehlen. Im folgenden finden Sie ein Allgemeines Referenz Thema für WMIC. Weitere Informationen und Richtlinien zur Verwendung von WMIC, einschließlich zusätzlicher Informationen zu Aliasen, Verben, Switches und Befehlen, finden [Sie unter Using Windows-Verwaltungsinstrumentation Command-Line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) und [WMIC-Take Command-Line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).

## <a name="alias"></a>Alias

Ein Alias ist ein benutzerfreundliches Umbenennen einer Klasse, einer Eigenschaft oder einer Methode, die das verwenden und Lesen von WMI erleichtert. Sie können bestimmen, welche Aliase für WMIC verfügbar sind, indem Sie **/?** ausführen. Sie können die Aliase für eine bestimmte Klasse auch mit dem **<className> /?** ausführen. Weitere Informationen finden Sie unter [WMIC Aliases](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).

## <a name="switch"></a>Schalter

Ein Switch ist eine WMIC-Option, die Sie Global oder optional festlegen können. Eine Liste der verfügbaren Switches finden Sie unter [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verben

Geben Sie den Aliasnamen gefolgt vom Verb ein, um Verben in WMIC zu verwenden. Wenn ein-Alias kein Verb unterstützt, erhalten Sie die Meldung, dass der Anbieter nicht in der Lage ist, den Vorgang auszuführen. Weitere Informationen finden Sie unter [WMIC Verbs](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).

Die meisten Aliase unterstützen die folgenden Verben.

<dl> <dt>

<span id="ASSOC"></span><span id="assoc"></span>Assoc
</dt> <dd>

Gibt das Ergebnis der Abfrage zurück, `Associators of (<wmi_object>)` bei der *<WMI- \_ Objekt>* der Pfad von Objekten ist, die von den **path** -oder **Class** -Befehlen zurückgegeben werden. Die Ergebnisse sind Instanzen, die dem-Objekt zugeordnet sind. Wenn Assoc mit einem Alias verwendet wird, werden die Klassen mit der Klasse zurückgegeben, die dem Alias zugrunde liegt. Standardmäßig wird die Ausgabe im HTML-Format zurückgegeben.

Das Assoc-Verb verfügt über die folgenden Schalter.



| Schalter                         | BESCHREIBUNG                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS:<classname> | Zurückgegebene Endpunkte, die dem Quell Objekt zugeordnet sind, müssen zu der angegebenen Klasse gehören oder davon abgeleitet werden.      |
| /RESULTROLE:<rolename>   | Zurückgegebene Endpunkte müssen eine bestimmte Rolle in Zuordnungen mit dem Quell Objekt wiedergeben.                              |
| /ASSOCCLASS:<assocclass> | Zurückgegebene Endpunkte müssen mithilfe der angegebenen Klasse oder einer davon abgeleiteten Klasse mit der Quelle verknüpft werden. |



 

Beispiel: **OS Assoc**

</dd> <dt>

<span id="CALL"></span><span id="call"></span>Erfordern
</dt> <dd>

Führt eine Methode aus.

Beispiel: **Dienst, bei dem Caption = ' Telnet ' den StartService aufruft**

> [!Note]  
> Verwenden Sie **/?**, um die verfügbaren Methoden für eine bestimmte Klasse zu bestimmen. Beispiel: **Dienst, bei dem Caption = ' Telnet ' aufgerufen/?** Listet die verfügbaren Funktionen für die Dienstklasse auf.

 

</dd> <dt>

<span id="CREATE"></span><span id="create"></span>Stelle
</dt> <dd>

Erstellt eine neue-Instanz und legt die Eigenschaftswerte fest. Create kann nicht zum Erstellen einer neuen Klasse verwendet werden.

Beispiel: **Environment Create Name = "Temp"; VariableValue = "New"**

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>Lösch
</dt> <dd>

Löscht die aktuelle Instanz oder den Satz von Instanzen. DELETE kann verwendet werden, um eine Klasse zu löschen.

Beispiel: **Process WHERE Name = "CALC.EXE" Delete**

</dd> <dt>

<span id="GET"></span><span id="get"></span>Erhalten
</dt> <dd>

Ruft bestimmte Eigenschaftswerte ab.

Get verfügt über die folgenden Schalter.



| Schalter                               | BESCHREIBUNG                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /Value                               | Die Ausgabe wird mit jedem Wert formatiert, der in einer separaten Zeile und mit dem Namen der Eigenschaft aufgeführt ist.                                           |
| /ALL                                 | Die Ausgabe wird als Tabelle formatiert.                                                                                                            |
| Tragen<translation table> | Übersetzen Sie die Ausgabe mithilfe der Übersetzungstabelle, die durch den Befehl benannt wird. Die Übersetzungstabellen BasicXML und NoComma sind in WMIC enthalten. |
| Jeden<interval>              | Wiederholen Sie den Befehl alle <interval> Sekunden.                                                                                         |
| Ges<format specifier>     | Gibt ein Schlüsselwort oder einen XSL-Dateinamen an, um die Daten zu formatieren.                                                                                  |



 

Beispiel: **Process Get Name**

</dd> <dt>

<span id="LIST"></span><span id="list"></span>List
</dt> <dd>

Zeigt Daten an. List ist das Standardverb.

Die Liste enthält die folgenden adversb.



| Adverbfilter   | Beschreibung                                                  |
|----------|--------------------------------------------------------------|
| KURZ    | Der Kernsatz der Eigenschaften.                                  |
| FULL     | Vollständiger Satz von Eigenschaften. Dies ist das standardmäßige adverbfilter für List. |
| INSTANCE | Nur Instanzpfade.                                         |
| STATUS   | Der Status der Objekte.                                       |
| SYSTEM   | Systemeigenschaften.                                           |



 

Die Liste enthält die folgenden Schalter.



| Schalter                               | BESCHREIBUNG                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Tragen<translation table> | Übersetzen Sie die Ausgabe mithilfe der Übersetzungstabelle, die durch den Befehl benannt wird. Die Übersetzungstabellen BasicXML und NoComma sind in WMIC enthalten. |
| Jeden<interval>              | Wiederholen Sie den Befehl alle <interval> Sekunden.                                                                                         |
| Ges<format specifier>     | Gibt ein Schlüsselwort oder einen XSL-Dateinamen an, um die Daten zu formatieren.                                                                                  |



 

Beispiel: **Prozesslisten Brief**

</dd> <dt>

<span id="SET"></span><span id="set"></span>Set
</dt> <dd>

Weist Eigenschaften Werte zu. Beispiel: **Umgebungs Satz Name = "Temp"**, **VariableValue = "New"**

</dd> </dl>

## <a name="switches"></a>Switches

Globale Switches werden verwendet, um Standardwerte für die WMIC-Umgebung festzulegen. Sie können den aktuellen Wert der von diesen Schaltern festgelegten Bedingungen anzeigen, indem Sie den **Kontext** Befehl eingeben.

<dl> <dt>

<span id="_NAMESPACE"></span><span id="_namespace"></span>/Namespace
</dt> <dd>

Der Namespace, der vom Alias verwendet wird. Der Standardwert ist root \\ CIMV2.

Beispiel: **/Namespace: \\ \\ root**

</dd> <dt>

<span id="_ROLE"></span><span id="_role"></span>/Role
</dt> <dd>

Namespace-WMIC sucht in der Regel nach Aliasen und anderen WMIC-Informationen.

Beispiel: **/role: \\ \\ root**

</dd> <dt>

<span id="_NODE"></span><span id="_node"></span>/Node
</dt> <dd>

Computer Namen, durch Kommas getrennt. Alle Befehle werden synchron auf allen Computern ausgeführt, die in diesem Wert aufgeführt sind. Dateinamen müssen & vorangestellt sein. Computer Namen innerhalb einer Datei müssen durch Kommas getrennt oder in separaten Zeilen enthalten sein.

</dd> <dt>

<span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL
</dt> <dd>

Identitätswechselebene.

Beispiel: **/IMPLEVEL: Anonymous**

</dd> <dt>

<span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL
</dt> <dd>

Authentifizierungs Ebene.

Beispiel: **/AUTHLEVEL: Pkt**

</dd> <dt>

<span id="_LOCALE"></span><span id="_locale"></span>/LOCALE
</dt> <dd>

Konfigurations.

Beispiel: **/locale: ms \_ 411**

</dd> <dt>

<span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES
</dt> <dd>

Aktivieren oder deaktivieren Sie alle Berechtigungen.

Beispiel: **/privileges: enable** oder **/privileges: deaktivieren**

</dd> <dt>

<span id="_TRACE"></span><span id="_trace"></span>/Trace
</dt> <dd>

Zeigt den Erfolg oder Misserfolg aller Funktionen an, die zum Ausführen von WMIC-Befehlen verwendet werden.

Beispiel: **/Trace: on** oder **/Trace: Off**

</dd> <dt>

<span id="_RECORD"></span><span id="_record"></span>/RECORD
</dt> <dd>

Zeichnet die gesamte Ausgabe in eine XML-Datei auf. Die Ausgabe wird auch an der Eingabeaufforderung angezeigt.

Beispiel: **/Record:** _MyOutput.xml_

</dd> <dt>

<span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE
</dt> <dd>

In der Regel werden Lösch Befehle bestätigt.

Beispiel: **/Interactive: on** oder **/Interactive: Off**

</dd> <dt>

<span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast **on** \|  \| *timeoutinmilliseconds*
</dt> <dd>

Wenn auf den/Node-Computern ein Ping-Befehl gesendet wird, bevor WMIC-Befehle an Sie gesendet werden. Wenn ein Computer nicht antwortet, werden die WMIC-Befehle nicht an ihn gesendet.

Beispiel: "/FailFast: on" oder "/FailFast: Off"

**WMIC-/FailFast: 1000**

</dd> <dt>

<span id="_USER"></span><span id="_user"></span>/User
</dt> <dd>

Benutzername, der von WMIC beim Zugriff auf die in den Aliasen angegebenen/Node-Computer oder-Computer verwendet wird. Sie werden aufgefordert, das Kennwort einzugeben. Ein Benutzername darf nicht mit dem lokalen Computer verwendet werden.

Beispiel: **/User:**_jsmith_

</dd> <dt>

<span id="_PASSWORD"></span><span id="_password"></span>/Password
</dt> <dd>

Kennwort, das von WMIC beim Zugriff auf/Node-Computer verwendet wird. Das Kennwort ist in der Befehlszeile sichtbar.

Beispiel: **/Password:**_Password_

</dd> <dt>

<span id="_OUTPUT"></span><span id="_output"></span>/Output
</dt> <dd>

Gibt einen Modus für alle Ausgabe Umleitungen an. Die Ausgabe wird nicht in der Befehlszeile angezeigt, und das Ziel wird vor Beginn der Ausgabe gelöscht. Gültige Werte sind stdout, Zwischenablage oder ein Dateiname.

Beispiel: **/Output: Zwischenablage**

</dd> <dt>

<span id="_APPEND"></span><span id="_append"></span>/Append
</dt> <dd>

Gibt einen Modus für alle Ausgabe Umleitungen an. Die Ausgabe wird nicht in der Befehlszeile angezeigt, und das Ziel wird vor Beginn der Ausgabe nicht gelöscht, und die Ausgabe wird an das Ende des aktuellen Inhalts des Ziels angehängt. Gültige Werte sind stdout, Zwischenablage oder ein Dateiname.

Beispiel: **/Append: Zwischenablage**

</dd> <dt>

<span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE
</dt> <dd>

Wird mit dem Schalter **List** und **Get/every** verwendet. Wenn Aggregate auf ON fest steht, werden die Ergebnisse in List und Get angezeigt, wenn für alle Computer in der/Node entweder geantwortet oder ein Timeout aufgetreten ist. Wenn Aggregate auf OFF eingestellt ist, werden die Ergebnisse in List und Get angezeigt, sobald Sie empfangen werden.

Beispiel: **/Aggregate: Off** oder **/Aggregate: on**

</dd> </dl>

## <a name="commands"></a>Befehle

Die folgenden WMIC-Befehle sind jederzeit verfügbar. Weitere Informationen finden Sie unter [WMIC-Befehle](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).

<dl> <dt>

<span id="CLASS"></span><span id="class"></span>Klassi
</dt> <dd>

Escapezeichen aus dem Standardalias Modus von WMIC, um direkt auf Klassen im WMI-Schema zuzugreifen. Weitere Informationen zu verfügbaren WMI-Klassen finden Sie unter [WMI-Klassen](wmi-classes.md).

Beispiel: **WMIC/Output: c: \\ClassOutput.htm Klasse Win32 \_ Sound Device**

</dd> <dt>

<span id="PATH"></span><span id="path"></span>ADS
</dt> <dd>

Escapezeichen aus dem Standardalias Modus von WMIC, um direkt auf Instanzen im WMI-Schema zuzugreifen.

Beispiel: **WMIC/Output: c: \\PathOutput.txt Pfad Win32 \_ Sound Device Get/Value**

</dd> <dt>

<span id="CONTEXT"></span><span id="context"></span>Kontext
</dt> <dd>

Zeigt die aktuellen Werte aller globalen Switches an.

Beispiel: **WMIC-Kontext**

</dd> <dt>

<span id="QUIT"></span><span id="quit"></span>Beendeten
</dt> <dd>

Beenden Sie den WMIC-Vorgang.

Beispiel: **WMIC Quit**

</dd> <dt>

<span id="EXIT"></span><span id="exit"></span>Abstiegs
</dt> <dd>

Beenden Sie den WMIC-Vorgang.

Beispiel: **WMIC Exit**

</dd> </dl>

## <a name="examples"></a>Beispiele

Das [Skript zum Festlegen von IP/Subnetz/Gateway/DNS mithilfe von WMIC](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) Sample in der TechNet Gallery beschreibt, wie IP-, Subnetz-, Gateway-und DNS-Einstellungen geändert und aktualisiert werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

