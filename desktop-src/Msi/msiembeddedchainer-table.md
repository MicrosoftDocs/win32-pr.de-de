---
description: Verwenden Sie diese Tabelle, um eine Installation mit mehreren Paketen zu erstellen.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: MsiEmbeddedChainer-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfcf48f3cf3863f19819b3337a136d2540fa3254067cacc50fcf391256caa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945055"
---
# <a name="msiembeddedchainer-table"></a>MsiEmbeddedChainer-Tabelle

Verwenden Sie diese Tabelle, um eine [Installation mit mehreren Paketen zu erstellen.](multiple-package-installations.md) Jede Zeile in der MsiEmbeddedChainer-Tabelle verweist auf eine andere benutzerdefinierte Funktion, die zum Installieren mehrerer Windows Installer-Pakete aus einem einzelnen Paket verwendet werden kann. Die [ausführbaren Dateien](executable-files.md) für die benutzerdefinierten Funktionen werden im Paket Windows Installer gespeichert.

**[Windows Installer 4.0 oder früher:](not-supported-in-windows-installer-4-0.md)** Nicht unterstützt. Diese Tabelle ist ab Windows Installer 4.5 verfügbar.

**Windows Server 2008 R2 mit [aktivierter Remotedesktopdienste-Rolle:](../termserv/terminal-services-portal.md)** Nicht unterstützt. Eine Installation mehrerer Pakete mithilfe der MsiEmbeddedChainer-Tabelle schlägt fehl, wenn [die](../termserv/terminal-services-portal.md) Remotedesktopdienste aktiviert ist.

Um mehrere Pakete aus einem einzelnen Paket zu installieren, muss eine der in der Tabelle MsiEmbeddedChainer aufgeführten benutzerdefinierten Funktionen eine bedingte Anweisung im Feld Bedingung enthalten, die auswertet, um die Aktion auszuführen. Wenn mehrere Funktionen eine Bedingung haben, die als ausgeführt ausgewertet wird, kann nur eine Funktion ausgeführt werden. Dieser Fall ist ein Fehler, und es kann nicht garantiert werden, welche Funktion ausgeführt wird. Wenn für die Installation andere benutzerdefinierte Aktionen erforderlich sind, sollten diese in der [CustomAction-Tabelle](customaction-table.md) und den Sequenztabellen erstellt werden.

Die Funktionen müssen der aktuellen Installation beitreten, indem sie die [**MsiJoinTransaction-Funktion**](/windows/desktop/api/Msi/nf-msi-msijointransaction) aufrufen und die [**MsiEndTransaction-Funktion**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) aufrufen, um die Installation mehrerer Pakete zu übernehmen. Wenn die Funktionen vor dem Aufruf von **MsiEndTransaction zurückgeben,** führt das Installationsprogramm ein Rollback für alle Installationen aus.

Die MsiEmbeddedChainer-Tabelle enthält die folgenden Spalten.



| Spalte             | Typ                             | Key | Nullwerte zulässig |
|--------------------|----------------------------------|-----|----------|
| MsiEmbeddedChainer | [Identifier](identifier.md)     | J   | N        |
| Bedingung          | [Condition](condition.md)       | N   | J        |
| CommandLine        | [Formatiert](formatted.md)       | N   | J        |
| Quelle             | [CustomSource](customsource.md) | N   | N        |
| type               | [Integer](integer.md)           | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer
</dt> <dd>

Der Primärschlüssel für die Tabelle. Dieser Wert ist ein eindeutiger Bezeichner für die benutzerdefinierte Funktion, die in dieser Zeile beschrieben wird.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Eine bedingte Anweisung zum Ausführen der benutzerdefinierten Funktion. Sie können die in der Tabelle MsiEmbeddedChainer aufgeführten Funktionen aktivieren oder deaktivieren, indem Sie eine Transformation verwenden, die die von diesem Feld ausgewerteten Eigenschaftswerte ändert. Weitere Informationen finden Sie unter [Verwenden von Eigenschaften in bedingten Anweisungen.](using-properties-in-conditional-statements.md)

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>Commandline
</dt> <dd>

Der Wert in diesem Feld ist ein Teil der Befehlszeilenzeichenfolge, die an die ausführbare Datei übergeben wird, die in der Spalte Source angegeben ist. Das Installationsprogramm fügt den Wert in diesem Feld an das Transaktionshand handle an, um die Befehlszeile zu generieren. Wenn der Wert in dieser Spalte NULL ist, besteht die Befehlszeile nur aus dem Transaktionshand handle.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Quelle
</dt> <dd>

Der Speicherort der ausführbaren Datei für die benutzerdefinierte Funktion. Wenn der Wert in der Spalte Typ 2 ist, kann diese Spalte einen externen Schlüssel in der [Binärtabelle enthalten.](binary-table.md) Wenn der Wert in der Spalte Typ 18 ist, kann diese Spalte einen externen Schlüssel in der [Dateitabelle enthalten.](file-table.md) Wenn der Wert in der Spalte Typ 50 ist, kann diese Spalte einen externen Schlüssel in der [Property-Tabelle enthalten.](property-table.md)

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Typ
</dt> <dd>

Die in der Tabelle MsiEmbeddedChainer aufgeführten Funktionen werden mithilfe der folgenden numerischen Typen benutzerdefinierter Aktionen beschrieben. Diese Spalte kann nur die Werte für die folgenden drei numerischen Typen enthalten: Jede andere Kombination benutzerdefinierter Aktionsflags wird ignoriert.



| Benutzerdefinierter Aktionstyp                                 | Benutzerdefinierte Aktionsflags                                                | Hexadezimal | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [Benutzerdefinierter Aktionstyp 2](custom-action-type-2.md)   | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |
| [Benutzerdefinierter Aktionstyp 18](custom-action-type-18.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |
| [Benutzerdefinierter Aktionstyp 50](custom-action-type-50.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Windows Installer verhindert nicht, dass die benutzerdefinierten Funktionen in dieser Tabelle während der Ankündigung der Anwendung ausgeführt werden. Sie können eine bedingte Anweisung in der Spalte Bedingung verwenden, um zu verhindern, dass eine Funktion während der Ankündigung ausgeführt wird.

Der Windows Installer stellt auch einen nicht eingebetteten externen Benutzeroberflächenhandler bereit, um eine umfassende Benutzeroberfläche auf der Grundlage des Pakets Windows Installer zu erstellen. Weitere Informationen zur Verwendung eines externen Benutzeroberflächenhandlers mit dem Windows Installer finden Sie unter Überwachen einer [Installation mit msiSetExternalUI.](monitoring-an-installation-using-msisetexternalui.md)

In [der Tabelle MsiPackageCertificate](msipackagecertificate-table.md) sind digitale Signaturzertifikate aufgeführt, mit denen die Identität der Installationspakete überprüft wird, die eine Installation mit mehreren Paketen ausführen. Sie können diese Tabelle verwenden, um zu reduzieren, wie oft ihre Installation mit mehreren Paketen eine Eingabeaufforderung zur Benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) anzeigt, die eine Antwort eines Administrators erfordert.

 

 
