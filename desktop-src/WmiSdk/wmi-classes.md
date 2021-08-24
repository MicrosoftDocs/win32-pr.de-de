---
description: Dieser Abschnitt enthält Informationen zur WMI-Klasse und zur Referenzseite.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: WMI-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1da15af60f1d1a32d652c8776e20ef36d65c1ff158dc6ac7465886361c5862c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757510"
---
# <a name="wmi-classes"></a>WMI-Klassen

Dieser Abschnitt enthält Informationen zur WMI-Klasse und zur Referenzseite. Weitere Informationen zum Abrufen von Klassen- oder Instanzdaten finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md) In der folgenden Liste werden bestimmte WMI-Klasseninformationen aufgelistet, beschrieben und Links zu diesen enthalten. Weitere Informationen und Skriptcodebeispiele für die Verwendung von WMI-Klassen zum Abrufen einer Vielzahl von Betriebssystem- und Hardwaredaten finden Sie unter [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md). Beispiele in C++ finden Sie unter [WMI C++-Anwendungsbeispiele.](wmi-c---application-examples.md) [Das Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md) zeigt, wie Sie Remotedaten abrufen. Sie können auch PowerShell verwenden, um auf WMI-Objekte zuzugreifen. Eine Liste der WMI-Klassen, die PowerShell-Codebeispiele enthalten, finden Sie [hier.](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi)



| `Section`                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMI-Systemklassen](wmi-system-classes.md)               | Vordefinierte Klassen, die in jedem Namespace im WMI-Kern (Windows Management Instrumentation) enthalten sind. Sie können eine WMI-Systemklasse erkennen, da der Name mit einem doppelten Unterstrich beginnt ( \_ \_ ). Diese Klassen stellen einen Großteil der grundlegenden Funktionen für WMI bereit. Die WMI-Systemklassen ähneln den Systemtabellen in SQL Server. |
| [MSFT-Klassen](msft-classes.md)                           | Andere Microsoft-Klassen, die die Möglichkeit bieten, mehrere Betriebssystemfeatures zu bearbeiten, z. B. Remoteereignisse und Richtlinienerweiterungen. Die [WMI-Klassen zur Problembehandlung](wmi-troubleshooting.md) sind MSFT-Klassen, die Daten zu WMI-Vorgängen bereitstellen.                                                                                               |
| [CIM-Klassen](cimclas.md)                                 | [*Common Information Model (CIM)-Schemaklassen.*](gloss-c.md) Wenn Sie eigene WMI-Klassen schreiben möchten, können Sie von einer oder mehreren dieser Klassen erben. Die WMI [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider) erben von den CIM-Klassen.                                                                          |
| [Standard-Consumerklassen](standard-consumer-classes.md) | Eine Gruppe von WMI-Ereignisverbrauchern, die eine Aktion auslösen, wenn ein beliebiges Ereignis empfangen wird. Weitere Informationen finden Sie unter [Überwachen von Ereignissen.](monitoring-events.md)                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>Codebeispiele für das WMI-Klassenskriptcenter

Die folgenden Scripting Center-Codebeispiele wirken sich auf mehrere WMI-Klassen in mehreren Namespaces aus.



| Link                                                                                                                                      | Beschreibung                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GUI WMI Explorer and WMI Method Help Generator](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | Beispielskript, das einen GUI-WMI-Explorer und einen WMI-Methoden-Hilfe-Generator bereitstellt.                                                                                                                                                        |
| [WMI-Explorer: Suche nach WMI-NameSpaces](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | Ermöglicht Benutzern die Suche nach Klassen in allen verfügbaren Namespaces auf den angegebenen Computern. Dieses Beispiel ist das Befehlszeilen-Verison des GUI-WMI-Explorer-Beispiels und kann als Erweiterung von Get-WmiObject -List betrachtet werden. |
| [Arposh Windows Systemverwaltungstool](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | AWSA wurde unter Berücksichtigung des Systemadministrators erstellt. Die Problembehandlung Windows Probleme erfordert eine vielzahl von Tools und Kenntnissen. AWSA vereint diese Tools an einem zentralen Ort und fügt zusätzliche Funktionen hinzu.       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>Benennungskonventionen für WMI-Klassen und -Eigenschaften

Eigenschaftennamen müssen der MOF-Syntax (Managed Object Format) entsprechen, die von der Distributed Management Task Force (VBF) definiert wird. Die anfänglichen Bezeichnerzeichen müssen aus den Buchstaben a bis z und dem Unterstrich ( \_ ) stammen. Alle zusätzlichen Zeichen müssen aus den Buchstaben a bis z, dem Unterstrich und den Ziffern 0 bis 9 stammen. Weitere Informationen finden Sie im Abschnitt Unicode-Verwendung der [CIM-Spezifikation Version 2.2.](https://www.dmtf.org/standards/cim)

SQL reservierte Wörter sollten nicht in Klassen- und Eigenschaftsnamen verwendet werden. Eine vollständige Liste der SQL wörter reservieren und weitere Informationen finden Sie im Abschnitt Richtlinien der [CIM-Spezifikation Version 2.2.](https://www.dmtf.org/standards/cim)

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>Dokumentkonventionen für eine WMI-Klassenverweisseite

In diesem Abschnitt werden die Dokumentkonventionen für eine WMI-Klassenverweisseite identifiziert und beschrieben.

Eine typische Verweisseite enthält einen Syntaxblock, eine Methodentabelle und eine Eigenschaftenliste.

-   Syntaxblock

    Eine vereinfachte Version von MOF-Code, die den Klassennamen, die übergeordnete Klasse (falls vorhanden) und die Klasseneigenschaften in alphabetischer Reihenfolge mit Datentypen enthält.

-   Tabelle "Methoden"

    Wenn eine Klasse über Methoden verfügt, werden die Methoden in der Tabelle direkt nach dem Syntaxblock aufgeführt. Jede implementierte Methode ist mit einer Verweisseite verknüpft.

-   Liste Eigenschaften

    Jede Klasseneigenschaft wird mit einem Datentyp, zugriffstyp (schreibgeschützt oder lese-/schreibgeschützt), Qualifizierern und einer Beschreibung der Eigenschaft aufgelistet.

## <a name="syntax-block"></a>Syntaxblock

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a>Tabelle "Methoden"



| Win32 \_ xyz-Methoden | Beschreibung                                |
|--------------------|--------------------------------------------|
| *SomeMethod*       | Kurze Beschreibung der Methode. |



 

## <a name="properties-list"></a>Liste Eigenschaften

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>Abc
</dt> <dd>

Datentyp: **uint16**

Zugriffstyp: Zeigt an, ob Sie über Lese-/Schreibzugriff oder schreibgeschützten Zugriff auf diese Eigenschaft verfügen.

Qualifizierer: Zeigt ggf. die Qualifizierer für die Eigenschaft an. Beispiel: **Schlüssel**, **Überschreiben Sie**.

Beschreibt die -Eigenschaft und stellt Vererbungsinformationen für die Eigenschaft bereit. Diese Eigenschaft wird z. B. von **CIM \_* xyz** geerbt. Es gibt einen Link zur übergeordneten Klasse, wenn Microsoft eine Implementierung dieser Klasse bereitstellt. Die CIM-Klassen sind jedoch nicht verfügbar.

</dd> <dt>

<span id="def"></span><span id="DEF"></span>Def
</dt> <dd>

Datentyp: **string**

Zugriffstyp: Schreibgeschützt

Beschreibung der Eigenschaft.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Enthält ggf. weitere Informationen zur -Klasse. Stellt ggf. auch Ableitungsinformationen bereit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> </dl>

 

 
