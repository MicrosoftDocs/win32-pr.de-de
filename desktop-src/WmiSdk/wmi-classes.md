---
description: Dieser Abschnitt enthält Informationen zur WMI-Klassen-und-Referenzseite.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: WMI-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa764d39c1fb048e125898a1f7e6d5cadf7f127d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368235"
---
# <a name="wmi-classes"></a>WMI-Klassen

Dieser Abschnitt enthält Informationen zur WMI-Klassen-und-Referenzseite. Weitere Informationen zum Abrufen von Klassen-oder Instanzdaten finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md). In der folgenden Liste sind Links zu bestimmten WMI-Klassen Informationen aufgelistet, beschrieben und bereitzustellen. Weitere Informationen und Skriptcode Beispiele für die Verwendung von WMI-Klassen zum Abrufen einer Vielzahl von Betriebssystem-und Hardware Daten finden Sie unter [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md). Beispiele in C++ finden Sie unter [WMI C++ Application examples](wmi-c---application-examples.md). [Beim Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md) wird das Abrufen von Remote Daten gezeigt. Sie können auch PowerShell-Zugriff auf WMI-Objekte verwenden; eine Liste der WMI-Klassen, die PowerShell-Codebeispiele enthalten, finden Sie [hier](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).



| `Section`                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMI-System Klassen](wmi-system-classes.md)               | Vordefinierte Klassen, die in jedem Namespace im WMI-Kern (Windows-Verwaltungsinstrumentation) enthalten sind. Sie können eine WMI-System Klasse erkennen, da der Name mit einem doppelten Unterstrich ( \_ \_ ) beginnt. Diese Klassen stellen einen großen Teil der grundlegenden Funktionen für WMI bereit. Die WMI-System Klassen sind den Systemtabellen in SQL Server ähnlich. |
| [MSFT-Klassen](msft-classes.md)                           | Andere Microsoft-Klassen, die die Möglichkeit bieten, mehrere Betriebssystemfunktionen zu bearbeiten, wie z. b. Remote Ereignisse und Richtlinien Erweiterungen. Die [WMI-Problem](wmi-troubleshooting.md) Behandlungs Klassen sind MSFT-Klassen, die Daten zu WMI-Vorgängen bereitstellen.                                                                                               |
| [CIM-Klassen](cimclas.md)                                 | [*Common Information Model (CIM)*](gloss-c.md) -Schema Klassen. Wenn Sie eigene WMI-Klassen schreiben möchten, können Sie von einer oder mehreren dieser Klassen erben. Die WMI- [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider) erben von den CIM-Klassen.                                                                          |
| [Standard Consumer-Klassen](standard-consumer-classes.md) | Ein Satz von WMI-Ereignisconsumern, die eine Aktion nach dem Empfang eines beliebigen Ereignisses auslöst. Weitere Informationen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md).                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>Code Beispiele für WMI-Klassen-Skript Center

Die folgenden Codebeispiele für das Skript Center wirken sich auf mehrere WMI-Klassen über mehrere Namespaces aus.



| Link                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GUI-WMI-Explorer und Hilfe-Generator der WMI-Methode](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | Beispielskript, das einen GUI-WMI-Explorer und Hilfe-Generator für WMI-Methoden bereitstellt.                                                                                                                                                        |
| [WMI-Explorer-durchsuchen von WMI-Namespaces](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | Ermöglicht es Benutzern, in allen verfügbaren Namespaces auf den angegebenen Computern nach Klassen zu suchen. Bei diesem Beispiel handelt es sich um die Befehlszeilen übersaison des GUI-WMI-Explorer-Beispiels, die als Erweiterung von Get-WmiObject-List angesehen werden können. |
| [Arposh Windows-System Verwaltungs Tool](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | Awsa wurde mit dem System Administrator erstellt. Die Problembehandlung für Windows-Probleme erfordert ein breites Spektrum an Tools und wissen. Awsa vereint diese Tools an einem zentralen Ort und bietet zusätzliche Funktionen.       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>Benennungs Konventionen für WMI-Klassen und-Eigenschaften

Eigenschaftsnamen müssen der von der verteilten Verwaltungs Task Force (DTMF) definierten Managed Object Format (MOF)-Syntax entsprechen. Die anfänglichen Bezeichnerzeichen müssen aus den Buchstaben a bis z und dem Unterstrich ( \_ ) bestehen. Alle weiteren Zeichen müssen aus den Buchstaben a bis z, dem Unterstrich und den Ziffern 0 bis 9 liegen. Weitere Informationen finden Sie im Abschnitt zur Unicode-Verwendung in der [CIM-Spezifikation, Version 2,2](https://www.dmtf.org/standards/cim).

SQL-Reserve Wörter sollten nicht in Klassen-und Eigenschaftsnamen verwendet werden. Eine vollständige Liste der SQL-Reserve Wörter und weitere Informationen finden Sie im Abschnitt "Richtlinien" in der [CIM-Spezifikation, Version 2,2](https://www.dmtf.org/standards/cim).

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>Dokument Konventionen für eine WMI-Klassenreferenz Seite

In diesem Abschnitt werden die Dokument Konventionen für eine WMI-Klassen Verweisseite identifiziert und beschrieben.

Eine typische Referenzseite enthält einen Syntax Block, eine Methoden Tabelle und eine Eigenschaften Liste.

-   Syntaxblock

    Eine vereinfachte Version von MOF-Code, die den Klassennamen, die übergeordnete Klasse (sofern vorhanden) und die Klasseneigenschaften in alphabetischer Reihenfolge mit Datentypen enthält.

-   Tabelle "Methoden"

    Wenn eine Klasse über Methoden verfügt, werden die Methoden in der Tabelle unmittelbar nach dem Syntax Block aufgelistet. Jede implementierte Methode ist mit einer Referenzseite verknüpft.

-   Liste Eigenschaften

    Jede Klassen Eigenschaft wird mit einem Datentyp, einem Zugriffstyp (schreibgeschützt oder Lese-/Schreibzugriff), Qualifizierern und einer Beschreibung der Eigenschaft aufgelistet.

## <a name="syntax-block"></a>Syntaxblock

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a>Tabelle "Methoden"



| Win32 \_ XYZ-Methoden | BESCHREIBUNG                                |
|--------------------|--------------------------------------------|
| *SomeMethod*       | Kurze Beschreibung der Funktionsweise der Methode. |



 

## <a name="properties-list"></a>Liste Eigenschaften

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>Sender
</dt> <dd>

Datentyp: **UInt16**

Zugriffstyp: zeigt an, ob Sie Lese-/Schreibzugriff oder schreibgeschützten Zugriff auf diese Eigenschaft haben.

Qualifizierer: zeigt die Qualifizierer für die Eigenschaft an, falls vorhanden. Beispiel: **Key**, **override**.

Beschreibt die-Eigenschaft und stellt Vererbungs Informationen für die-Eigenschaft bereit. Diese Eigenschaft wird z. b. von **CIM \_* XYZ * * * geerbt. Es gibt einen Link zur übergeordneten-Klasse, wenn Microsoft eine Implementierung dieser Klasse bereitstellt. Die CIM-Klassen sind jedoch nicht verfügbar.

</dd> <dt>

<span id="def"></span><span id="DEF"></span>auflösenden
</dt> <dd>

Datentyp: **Zeichenfolge**

Zugriffstyp: Schreibgeschützt

Die Beschreibung der Eigenschaft.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Gibt ggf. Weitere Informationen zur-Klasse. Bietet auch abderivationsinformationen, falls zutreffend.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> </dl>

 

 
