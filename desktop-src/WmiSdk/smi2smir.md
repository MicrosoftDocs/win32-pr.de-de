---
description: Der SNMP-Compiler wird als einzelne ausführbare Datei im Befehlszeilen Modus ausgeführt.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e1d757293b5ee128f2ce1bc2bd5ec8479d9b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218307"
---
# <a name="smi2smir"></a>smi2smir

Der SNMP-Compiler wird als einzelne ausführbare Datei im Befehlszeilen Modus ausgeführt. Der Compiler akzeptiert ein SNMP-Informationsmodul als Eingabe und akzeptiert alle zusätzlichen Module, die zum Auflösen externer Verweise erforderlich sind. Verwenden Sie eines der folgenden Beispiele für die Befehlszeilen Syntax.

Weitere Informationen zur Verwendung dieses Compilers finden [Sie unter Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a>Switches

<dl> <dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*Diagnosticargs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Diagnose Argumente.

<dl> <dt>

<span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _Diagnose Ebene_*_>_*
</dt> <dd>

Typ der anzuzeigenden Diagnose. Der Standardwert ist 2.

Im folgenden finden Sie eine Liste der Werte für die Diagnose Ebene, die festgelegt werden können:

-   0 = unbeaufsichtigt
-   1 = schwerwiegend
-   2 = schwerwiegend und Warnung
-   3 = schwerwiegende, Warn-und Informationsmeldungen

</dd> <dt>

<span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _Anzahl_*_>_*
</dt> <dd>

Maximale Anzahl von schwerwiegenden und Warnmeldungen, die angezeigt werden sollen. "count" muss eine positive ganze *Zahl* sein. Wenn **/c** nicht angegeben ist, gibt es keine Beschränkung für die Anzahl von Fehlern, die gemeldet werden können.

</dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*Versionargs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Versions Argumente.

<dl> <dt>

<span id="_v1"></span><span id="_V1"></span>**/v1**
</dt> <dd>

Gibt eine strikte Übereinstimmung mit dem SNMPv1 SMI an. Der Compiler meldet einen Fehler, wenn er nicht-SNMPv1-Anweisungen erkennt.

</dd> <dt>

<span id="_v2c"></span><span id="_V2C"></span>**/v2c**
</dt> <dd>

Gibt eine strikte Übereinstimmung mit dem SNMPv2 SMI an. Der Compiler meldet einen Fehler, wenn er nicht-SNMPv2-Anweisungen erkennt.

</dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*"Commandargs"*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Befehlsargumente.

<dl> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Löscht das angegebene Modul aus dem SMIR.

</dd> <dt>

<span id="_p"></span><span id="_P"></span>**/p**
</dt> <dd>

Löscht alle Module in SMIR.

</dd> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Listet alle Module in SMIR auf.

</dd> <dt>

<span id="_lc"></span><span id="_LC"></span>**/lc**
</dt> <dd>

Führt eine lokale Syntax Überprüfung für das Modul aus.

</dd> <dt>

<span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/EC** **\[<** _Commandmodifier_*_>\]_*
</dt> <dd>

Führt lokale und externe Überprüfungen für das Modul aus.

</dd> <dt>

<span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _Commandmodifier_*_>\]_*
</dt> <dd>

Führt lokale und externe Prüfungen durch und lädt das Modul in SMIR.

</dd> <dt>

<span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /sa ein. <** _Commandmodifier_*_>\]_*
</dt> <dd>

Identisch mit **/a**, funktioniert jedoch im Hintergrund.

</dd> <dt>

<span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _Commandmodifier_*_>\]_*
</dt> <dd>

Generiert eine SMIR. MOF-Datei, die Sie später mit dem MOF-Compiler in WMI laden können. Wird vom SNMP-Klassen Anbieter verwendet, um Klassen dynamisch für einen oder mehrere Namespaces bereitzustellen. Verwenden Sie diese Option, wenn Sie nicht wissen, welche MISB von den verwalteten SNMP-Geräten unterstützt werden. Der SNMP-Klassen Anbieter überprüft das Gerät zur Laufzeit auf das vorhanden sein dieses MIB und stellt die Klassen dynamisch für den Namespace bereit.

</dd> <dt>

<span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _Commandmodifier_*_>\]_*
</dt> <dd>

Generiert eine statische MOF-Datei, die später in WMI als statische Klassen für einen bestimmten Namespace geladen werden kann. Verwenden Sie diese Option, wenn Sie wissen, welche MISB von den verwalteten SNMP-Geräten unterstützt werden. Sie können die MOF-Datei definieren, die generiert werden soll, indem Sie die Ausgabe des Befehls an eine angegebene Datei weiterleiten. Verwenden Sie with **/ext/o** nicht.

</dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*Commandmodifier*>
</dt> <dd>

Der Compiler akzeptiert die folgenden befehlsmodifiziererer.

<dl> <dt>

<span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _Verzeichnis_*_>_*
</dt> <dd>

Gibt ein Verzeichnis an, das nach abhängigen MIB-Modulen durchsucht werden soll. Verwendung mit **/a**, **/EC**, **/g**, **/GC** und **/sa ein.**. Die **/i** -Option kann mehrmals im Befehl angezeigt werden. Verzeichnisse werden in der im Befehl angegebenen Reihenfolge durchsucht.

</dd> <dt>

<span id="_ch"></span><span id="_CH"></span>**/ch**
</dt> <dd>

Generiert Kontextinformationen, z. b. Datum, Uhrzeit, Host oder Benutzer, im MOF-Dateiheader. Verwendung mit **/g** und **/GC**.

</dd> <dt>

<span id="_t"></span><span id="_T"></span>**/t**
</dt> <dd>

Generiert [SnmpNotification](snmpnotification.md) -Klassen. Verwenden Sie mit **/a**, **/g** und **/sa ein.**.

</dd> <dt>

<span id="_ext"></span><span id="_EXT"></span>**/ext**
</dt> <dd>

Generiert [snmpextendednotification](snmpextendednotification.md) -Klassen. Verwenden Sie mit **/a**, **/g** und **/sa ein.**.

</dd> <dt>

<span id="_t_o"></span><span id="_T_O"></span>**/t/o**
</dt> <dd>

Generiert nur [SnmpNotification](snmpnotification.md) -Klassen. Verwenden Sie mit **/a**, **/g** und **/sa ein.**.

</dd> <dt>

<span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**
</dt> <dd>

Generiert nur [snmpextendednotification](snmpextendednotification.md) -Klassen. Verwenden Sie mit **/a**, **/g** und **/sa ein.**.

</dd> <dt>

<span id="_s"></span><span id="_S"></span>**/s**
</dt> <dd>

Ordnet den Text der Description-Klausel nicht zu. Verwendung mit **/a**, **/g**, **/GC** und **/sa ein.**. Verwenden Sie diese Option, wenn Sie die Speicheranforderungen minimieren möchten.

</dd> <dt>

<span id="_auto"></span><span id="_AUTO"></span>**/Auto**
</dt> <dd>

Erstellt die MIB-Nachschlage Tabelle neu, bevor die <*commandarg*> Switch abgeschlossen wird. Verwendung mit **/a**, **/EC**, **/g** und **/GC**.

</dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*Registryargs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Registrierungs Argumente.

<dl> <dt>

<span id="_pa"></span><span id="_PA"></span>**/pa**
</dt> <dd>

Fügt der Registrierung das angegebene Verzeichnis hinzu. Der Standardwert ist das aktuelle Verzeichnis.

</dd> <dt>

<span id="_pd"></span><span id="_PD"></span>**/PD**
</dt> <dd>

Löscht das angegebene Verzeichnis aus der Registrierung. Der Standardwert ist das aktuelle Verzeichnis.

</dd> <dt>

<span id="_pl"></span><span id="_PL"></span>**"/pl"**
</dt> <dd>

Listet die MIB-Such Verzeichnisse in der Registrierung auf.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Erstellt die gesamte MIB-Nachschlage Tabelle neu.

</dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*Moduleinfoargs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Modul Informations Argumente.

<dl> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Gibt den ASN. 1-Namen des angegebenen Moduls zurück.

</dd> <dt>

<span id="_ni"></span><span id="_NI"></span>**/ni**
</dt> <dd>

Gibt die ASN. 1-Namen aller Import Module zurück, auf die vom Eingabe Modul verwiesen wird.

</dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*Helparamegs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Hilfe Argumente.

<dl> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Zeigt die Hilfe zur SNMP-compilersyntax an.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Zeigt die Hilfe zur SNMP-compilersyntax an.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

SNMP-Informationsmodule werden in einer Teilmenge der abstrakten Syntax Notation One (ASN. 1) geschrieben, der der Compiler die folgenden Funktionen ausführt:

-   Lädt die Daten aus dem SNMP-Informationsmodul.
-   Überprüfungsvorgänge für das Informationsmodul. Er überprüft beispielsweise die lokale Syntax und überprüft externe Verweise auf Informationen in den Tochter Modulen.
-   Entfernen aller zuvor geladenen Daten aus dem SMIR oder Entfernen geladener Daten aus einem Informationsmodul.
-   Gibt den ASN. 1-Modulnamen einer angegebenen Datei zurück oder gibt die ASN. 1-Modulnamen aller importierten Module in einer angegebenen Datei zurück.
-   Zurückgeben der ASN.1-Modulnamen aller derzeit im SMIR geladenen SNMP-Informationsmodule.
-   Führt die automatische Auflösung importierter Module durch und erfordert nicht, dass Benutzer die erforderlichen Module manuell angeben müssen.
-   Führt einen Vorgang zum automatischen Laden aus, der keine Ausgabe generiert, aber zum Laden von Daten in SMIR während eines Installationsvorgangs verwendet werden kann.
-   Gibt die Daten aus dem SNMP-Informationsmodul in SMIR aus.
-   Erstellt optional eine statische oder SMIR-MOF-Datei, die die Ausgabe des Informations Moduls enthält.

    Falls erforderlich, können Sie die Datei "static. mof" in einen WMI-Namespace laden. Eine SMIR. MOF-Datei enthält den Namen des SNMP-Namespace, in dem sich die Klassen befinden sollten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Datei "Pra. mof" als Ausgabe aus der Datei "Pra. MIB" definiert.

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SNMP-Compilerfehlermeldungen](snmp-compiler-error-messages.md)
</dt> <dt>

[Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[Zugreifen auf SNMP-Geräte](accessing-snmp-devices.md)
</dt> </dl>

 

 




