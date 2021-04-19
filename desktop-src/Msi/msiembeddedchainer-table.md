---
description: Verwenden Sie diese Tabelle, um eine Installation mit mehreren Paketen zu verfassen.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: Msiembeddecodchainer-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902a33bce5d3a0aff3d2797fce94e5d272b61271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360016"
---
# <a name="msiembeddedchainer-table"></a>Msiembeddecodchainer-Tabelle

Verwenden Sie diese Tabelle, um eine [Installation mit mehreren Paketen](multiple-package-installations.md)zu verfassen. Jede Zeile in der Tabelle msiembeddedchainer verweist auf eine andere benutzerdefinierte Funktion, die verwendet werden kann, um mehrere Windows Installer Pakete von einem einzelnen Paket zu installieren. Die [ausführbaren Dateien](executable-files.md) für die benutzerdefinierten Funktionen werden innerhalb des Windows Installer Pakets gespeichert.

**[Windows Installer 4,0 oder früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt. Diese Tabelle ist ab Windows Installer 4,5 verfügbar.

**Windows Server 2008 R2 mit aktivierter [Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle:** Nicht unterstützt. Eine mehrfach Paketinstallation mithilfe der msiembeddedchainer-Tabelle schlägt fehl, wenn die [Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle aktiviert ist.

Wenn Sie mehrere Pakete aus einem einzelnen Paket installieren möchten, muss eine der in der Tabelle msiembeddedchainer aufgelisteten benutzerdefinierten Funktionen über eine Bedingungs Anweisung im Bedingungs Feld verfügen, die zum Ausführen der Aktion ausgewertet wird. Wenn mehr als eine Funktion eine Bedingung aufweist, die ausgeführt wird, kann nur eine Funktion ausgeführt werden. In diesem Fall handelt es sich um einen Fehler, und es kann nicht garantiert werden, welche Funktion ausgeführt wird. Wenn andere benutzerdefinierte Aktionen von der Installation benötigt werden, sollten diese in der [Tabelle "CustomAction](customaction-table.md) " und in den Sequenz Tabellen erstellt werden.

Die Funktionen müssen der aktuellen Installation beitreten, indem Sie die [**msijointransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) -Funktion aufrufen und die [**msiendtransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) -Funktion aufrufen, um die Installation mehrerer Pakete zu committen. Wenn die Funktionen vor dem Aufruf von " **msiendtransaction**" zurückgegeben werden, führt das Installationsprogramm ein Rollback aller

Die msiembeddebug-Tabelle enthält die folgenden Spalten.



| Spalte             | Typ                             | Schlüssel | Nullwerte zulässig |
|--------------------|----------------------------------|-----|----------|
| Msiembeddecodchainer | [Bezeichner](identifier.md)     | J   | N        |
| Bedingung          | [Condition](condition.md)       | N   | J        |
| CommandLine        | [Großformatige](formatted.md)       | N   | J        |
| `Source`             | [CustomSource](customsource.md) | N   | N        |
| type               | [Integer](integer.md)           | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>Msiembeddecodchainer
</dt> <dd>

Der Primärschlüssel für die Tabelle. Dieser Wert ist ein eindeutiger Bezeichner für die benutzerdefinierte Funktion, die in dieser Zeile beschrieben wird.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Eine bedingte Anweisung zum Ausführen der benutzerdefinierten Funktion. Sie können die in der Tabelle msiembeddedchainer aufgeführten Funktionen mithilfe einer Transformation aktivieren oder deaktivieren, die die von diesem Feld ausgewerteten Eigenschaftswerte ändert. Weitere Informationen finden Sie unter [Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md).

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>CommandLine
</dt> <dd>

Der Wert in diesem Feld ist ein Teil der Befehlszeilen Zeichenfolge, die an die in der Spalte Quelle identifizierte ausführbare Datei übermittelt wird. Das Installationsprogramm fügt den Wert in diesem Feld an den Transaktions Handle an, um die Befehlszeile zu generieren. Wenn der Wert in dieser Spalte NULL ist, besteht die Befehlszeile nur aus dem Transaktions handle.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Ausgangs
</dt> <dd>

Der Speicherort der ausführbaren Datei für die benutzerdefinierte Funktion. Wenn der Wert in der Type-Spalte 2 ist, kann diese Spalte einen externen Schlüssel in die [binäre Tabelle](binary-table.md)enthalten. Wenn der Wert in der Type-Spalte 18 ist, kann diese Spalte einen externen Schlüssel in die [Dateitabelle](file-table.md)enthalten. Wenn der Wert in der Type-Spalte 50 ist, kann diese Spalte einen externen Schlüssel in die [Eigenschaften Tabelle](property-table.md)enthalten.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte
</dt> <dd>

Die in der Tabelle msiembeddedchainer aufgeführten Funktionen werden mithilfe der folgenden numerischen Typen von benutzerdefinierten Aktionen beschrieben. Diese Spalte kann nur die Werte für die folgenden drei numerischen Typen enthalten: eine beliebige andere Kombination von benutzerdefinierten Aktionsflags wird ignoriert.



| Benutzerdefinierter Aktionstyp                                 | Benutzerdefinierte Aktionsflags                                                | Hexadezimal | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [Benutzerdefinierter Aktionstyp 2](custom-action-type-2.md)   | **msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypebinarydata** | 0x002       | 2       |
| [Benutzerdefinierter Aktionstyp 18](custom-action-type-18.md) | **msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypesourcefile** | 0x012       | 18      |
| [Benutzerdefinierter Aktionstyp 50](custom-action-type-50.md) | **msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypeproperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Windows Installer verhindert nicht, dass die benutzerdefinierten Funktionen in dieser Tabelle während der Ankündigung der Anwendung ausgeführt werden. Sie können eine bedingte Anweisung in der Spalte Bedingung verwenden, um zu verhindern, dass eine Funktion während der Ankündigung ausgeführt wird.

Der Windows Installer bietet auch einen nicht eingebetteten externen UI-Handler zum Erstellen einer umfassenden Benutzeroberfläche oberhalb des Windows Installer Pakets. Weitere Informationen zur Verwendung eines externen UI-Handlers mit dem Windows Installer finden Sie unter über [Wachen einer Installation mit msieintexternalui](monitoring-an-installation-using-msisetexternalui.md).

In der [Tabelle msipackagecertificate](msipackagecertificate-table.md) sind digitale Signatur Zertifikate aufgeführt, mit denen die Identität der Installationspakete überprüft wird, die eine Installation mit mehreren Paketen vornehmen. Sie können diese Tabelle verwenden, um zu reduzieren, wie oft bei der Installation mehrerer Pakete eine [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) angezeigt wird, die von einem Administrator eine Antwort erfordert.

 

 
