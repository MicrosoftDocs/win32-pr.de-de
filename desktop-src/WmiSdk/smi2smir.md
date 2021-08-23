---
description: Der SNMP-Compiler wird als einzelne ausführbare Datei im Befehlszeilenmodus ausgeführt.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3909ef1df4047ba0b797fe4a01088c62e60b287969445d311214180e4fa441a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050168"
---
# <a name="smi2smir"></a>smi2smir

Der SNMP-Compiler wird als einzelne ausführbare Datei im Befehlszeilenmodus ausgeführt. Der Compiler akzeptiert ein SNMP-Informationsmodul als Eingabe und alle zusätzlichen Module, die zum Auflösen externer Verweise erforderlich sind. Verwenden Sie eines der folgenden Beispiele für die Befehlszeilensyntax.

Weitere Informationen dazu, wann dieser Compiler verwendet wird, finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a>Switches

<dl> <dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Diagnoseargumente.

<dl> <dt>

<span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _Diagnoseebene_*_>_*
</dt> <dd>

Typ der anzuzeigende Diagnose. Der Standardwert ist 2.

Im Folgenden finden Sie eine Liste der Diagnoseebenenwerte, die festgelegt werden können:

-   0 = Automatisch
-   1 = Schwerwiegend
-   2 = Schwerwiegend und Warnung
-   3 = Schwerwiegende Meldungen, Warnungen und Informationsmeldungen

</dd> <dt>

<span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _count_*_>_*
</dt> <dd>

Maximale Anzahl von schwerwiegenden Und Warnmeldungen, die angezeigt werden sollen; *count* muss eine positive ganze Dezimalzahl sein. Wenn **/c** nicht angegeben ist, gibt es keine Beschränkung für die Anzahl der Fehler, die gemeldet werden können.

</dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Versionsargumente.

<dl> <dt>

<span id="_v1"></span><span id="_V1"></span>**/v1**
</dt> <dd>

Gibt die strikte Übereinstimmung mit dem SNMPv1-SMI an. Der Compiler meldet einen Fehler, wenn er Nicht-SNMPv1-Anweisungen erkennt.

</dd> <dt>

<span id="_v2c"></span><span id="_V2C"></span>**/v2c**
</dt> <dd>

Gibt die strikte Übereinstimmung mit dem SNMPv2-SMI an. Der Compiler meldet einen Fehler, wenn er Nicht-SNMPv2-Anweisungen erkennt.

</dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Befehlsargumente.

<dl> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Löscht das angegebene Modul aus dem SMIR.

</dd> <dt>

<span id="_p"></span><span id="_P"></span>**/p**
</dt> <dd>

Löscht alle Module im SMIR.

</dd> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Listet alle Module im SMIR auf.

</dd> <dt>

<span id="_lc"></span><span id="_LC"></span>**/lc**
</dt> <dd>

Führt eine lokale Syntaxüberprüfung für das Modul aus.

</dd> <dt>

<span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<** _CommandModifier_*_>\]_*
</dt> <dd>

Führt lokale und externe Überprüfungen für das Modul aus.

</dd> <dt>

<span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**/a \[ <** _CommandModifier_*_>\]_*
</dt> <dd>

Führt lokale und externe Überprüfungen durch und lädt das Modul in das SMIR.

</dd> <dt>

<span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**/sa \[ <** _CommandModifier_*_>\]_*
</dt> <dd>

Entspricht **/a**, funktioniert aber im Hintergrund.

</dd> <dt>

<span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**/g \[ <** _CommandModifier_*_>\]_*
</dt> <dd>

Generiert eine SMIR-MOF-Datei, die Sie später mit dem MOF-Compiler in WMI laden können. Wird vom SNMP-Klassenanbieter verwendet, um Klassen dynamisch für einen oder mehrere Namespaces bereitzustellen. Verwenden Sie diese Option, wenn Sie nicht wissen, welche MIBs von den verwalteten SNMP-Geräten unterstützt werden. Der SNMP-Klassenanbieter überprüft das Gerät zur Laufzeit auf das Vorhandensein dieses MIB und stellt die Klassen dynamisch für den Namespace bereit.

</dd> <dt>

<span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**/gc \[ <** _CommandModifier_*_>\]_*
</dt> <dd>

Generiert eine statische MOF-Datei, die später als statische Klassen für einen bestimmten Namespace in WMI geladen werden kann. Verwenden Sie diese Option, wenn Sie wissen, welche MIBs von den verwalteten SNMP-Geräten unterstützt werden. Sie können die zu generierende MOF-Datei definieren, indem Sie die Ausgabe des Befehls an eine angegebene Datei leiten. Verwenden Sie nicht mit **/ext/o.**

</dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Befehlsmodifizierer.

<dl> <dt>

<span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**Verzeichnis "/i** _<"_*_>_*
</dt> <dd>

Gibt ein Verzeichnis an, das nach abhängigen MIB-Modulen durchsucht werden soll. Verwenden Sie mit **/a**, **/ec**, **/g**, **/gc** und **/sa**. Die **Option /i** kann mehrmals im Befehl angezeigt werden. Verzeichnisse werden in der im Befehl angegebenen Reihenfolge durchsucht.

</dd> <dt>

<span id="_ch"></span><span id="_CH"></span>**/ch**
</dt> <dd>

Generiert Kontextinformationen wie Datum, Uhrzeit, Host oder Benutzer im MOF-Dateiheader. Verwenden Sie mit **/g** und **/gc.**

</dd> <dt>

<span id="_t"></span><span id="_T"></span>**/t**
</dt> <dd>

Generiert [SnmpNotification-Klassen.](snmpnotification.md) Verwenden Sie mit **/a**, **/g** und **/sa**.

</dd> <dt>

<span id="_ext"></span><span id="_EXT"></span>**/ext**
</dt> <dd>

Generiert [SnmpExtendedNotification-Klassen.](snmpextendednotification.md) Verwenden Sie mit **/a**, **/g** und **/sa**.

</dd> <dt>

<span id="_t_o"></span><span id="_T_O"></span>**/t/o**
</dt> <dd>

Generiert nur [SnmpNotification-Klassen.](snmpnotification.md) Verwenden Sie mit **/a**, **/g** und **/sa**.

</dd> <dt>

<span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**
</dt> <dd>

Generiert nur [SnmpExtendedNotification-Klassen.](snmpextendednotification.md) Verwenden Sie mit **/a**, **/g** und **/sa**.

</dd> <dt>

<span id="_s"></span><span id="_S"></span>**/s**
</dt> <dd>

Der Text der DESCRIPTION-Klausel wird nicht zugeordnet. Verwenden Sie mit **/a**, **/g**, **/gc** und **/sa**. Verwenden Sie diese Option, wenn Sie die Speicheranforderungen minimieren möchten.

</dd> <dt>

<span id="_auto"></span><span id="_AUTO"></span>**/auto**
</dt> <dd>

Erstellt die MIB-Nachschlagetabelle neu, bevor der <*CommandArg*> Switch abgeschlossen wird. Verwenden Sie mit **/a,** **/ec,** **/g** und **/gc.**

</dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Registrierungsargumente.

<dl> <dt>

<span id="_pa"></span><span id="_PA"></span>**/pa**
</dt> <dd>

Fügt der Registrierung das angegebene Verzeichnis hinzu. Der Standardwert ist das aktuelle Verzeichnis.

</dd> <dt>

<span id="_pd"></span><span id="_PD"></span>**/pd**
</dt> <dd>

Löscht das angegebene Verzeichnis aus der Registrierung. Der Standardwert ist das aktuelle Verzeichnis.

</dd> <dt>

<span id="_pl"></span><span id="_PL"></span>**/pl**
</dt> <dd>

Listet die MIB-Suchverzeichnisse in der Registrierung auf.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Erstellt die gesamte MIB-Nachschlagetabelle neu.

</dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Modulinformationsargumente.

<dl> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Gibt den ASN.1-Namen des angegebenen Moduls zurück.

</dd> <dt>

<span id="_ni"></span><span id="_NI"></span>**/ni**
</dt> <dd>

Gibt die ASN.1-Namen aller Importmodule zurück, auf die vom Eingabemodul verwiesen wird.

</dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> <dd>

Der Compiler akzeptiert die folgenden Hilfeargumente.

<dl> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Zeigt Hilfe zur SNMP-Compilersyntax an.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Zeigt Hilfe zur SNMP-Compilersyntax an.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

SNMP-Informationsmodule werden in einer Teilmenge der Abstract Syntax Notation One (ASN.1) geschrieben. Der Compiler führt die folgenden Funktionen aus:

-   Lädt die Daten aus dem SNMP-Informationsmodul.
-   Überprüfungsvorgänge für das Informationsmodul. Beispielsweise wird die lokale Syntax überprüft, und externe Verweise werden mit Informationen in den subsidiären Modulen überprüft.
-   Entfernen aller zuvor geladenen Daten aus dem SMIR oder Entfernen geladener Daten aus einem Informationsmodul.
-   Gibt den ASN.1-Modulnamen einer angegebenen Datei oder die ASN.1-Modulnamen aller importierten Module in einer angegebenen Datei zurück.
-   Zurückgeben der ASN.1-Modulnamen aller derzeit im SMIR geladenen SNMP-Informationsmodule.
-   Führt die automatische Auflösung importierter Module aus, anstatt von Benutzern zu verlangen, dass die erforderlichen Module manuell angegeben werden.
-   Führt einen Automatischlademodus aus, der keine Ausgabe generiert, aber während eines Installationsvorganges zum Laden von Daten in SMIR verwendet werden kann.
-   Gibt die Daten aus dem SNMP-Informationsmodul in SMIR aus.
-   Erstellt optional eine statische oder SMIR MOF-Datei, die die Ausgabe des Informationsmoduls enthält.

    Bei Bedarf können Sie die statische MOF-Datei in einen WMI-Namespace laden. Eine MOF-Datei mit SMIR enthält den Namen des SNMP-Namespace, in dem sich die Klassen befinden sollen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Datei pra.mof als Ausgabe der Datei pra.mib definiert.

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

 

 




