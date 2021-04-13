---
description: Die UpgradedImages-Tabelle enthält Informationen zu den aktualisierten Images des Produkts.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: UpgradedImages-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348958"
---
# <a name="upgradedimages-table-patchwizdll"></a>UpgradedImages-Tabelle (Patchwiz.dll)

Die UpgradedImages-Tabelle enthält Informationen zu den aktualisierten Images des Produkts. Bei dem aktualisierten Image muss es sich um ein vollständig dekomprimiertes Setup Image der neuesten Version des Produkts handeln, z. b. ein administratives Image oder ein nicht komprimiertes Setup Abbild von einer CD-ROM. Ein Windows Installer Patch-Paket aktualisiert ein Zielimage in ein aktualisiertes Image. Die UpgradedImages-Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) erforderlich und wird von [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md)verwendet.

In jeder Datenbank der Patcherstellung (PCP-Datei) ist eine UpgradedImages-Tabelle erforderlich, die mindestens einen Datensatz enthält. Diese Tabelle wird von [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md)verwendet.

Die UpgradedImages-Tabelle weist die folgenden Spalten auf.



| Spalte       | Typ | Schlüssel | Nullwerte zulässig |
|--------------|------|-----|----------|
| Upgraded     | text | J   | N        |
| Msipath      | text |     | N        |
| Patchmsipath | text |     | J        |
| SymbolPath  | text |     | J        |
| Familie       | text |     | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert
</dt> <dd>

Das aktualisierte Feld ist ein beliebiger Bezeichner, um die Ziel Images mit einem aktualisierten Image des Produkts zu verbinden.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>Msipath
</dt> <dd>

Dieses Feld gibt den vollständigen Pfad, einschließlich des Datei namens, zum Speicherort der MSI-Datei für das aktualisierte Image an. Dies ist der Speicherort der Quelldateien für das aktualisierte Image.

</dd> <dt>

<span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>Patchmsipath
</dt> <dd>

Der optionale patchmsipath verweist auf eine geänderte Kopie der aktualisierten Installations Datenbank, die zusätzliche, für den patchinstallations Vorgang spezifische Vorgänge enthält. Beispielsweise zusätzliche Dialogfelder oder benutzerdefinierte Aktionen, die von der [**Patch**](patch.md) -Eigenschaft abhängig sind.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath
</dt> <dd>

Eine durch Semikolons getrennte Liste von Ordnern, die nach Symbol Dateien durchsucht werden sollen, die zur Optimierung der Generierung des binären Patches verwendet werden kann. Beachten Sie, dass die Unterverzeichnisse der in diesem Feld angegebenen Ordner nicht durchsucht werden. Ein optimierter binärer Patch kann kleiner sein. Visual C++ müssen auf dem Computer installiert sein, der den Patch erzeugt und zum Erstellen der Symbol Dateien verwendet wird. Dieses Feld ist optional, und das Installationsprogramm erstellt einen binären Patch, auch wenn keine Symbol Dateien angegeben sind oder wenn die Symbol Dateien nicht zum Patchwiz.dll verfügbar sind.

</dd> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Ärzte
</dt> <dd>

Fremdschlüssel in der [Tabelle "ImageFamilies](imagefamilies-table-patchwiz-dll-.md)". Jedes aktualisierte Image darf nur einer Familie angehören.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Obwohl jedes aktualisierte Image in einer separaten Bild Familie gruppiert werden kann, kann das Gruppieren von aktualisierten Bildern, die gemeinsam Dateien gemeinsam nutzen, die. msp-Datei verkleinern.

Diese Tabelle akzeptiert Umgebungsvariablen als Pfade, die mit Version 4,0 von Patchwiz.dll beginnen.

 

 



