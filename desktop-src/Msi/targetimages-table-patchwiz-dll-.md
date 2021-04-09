---
description: Die Tabelle TargetImages enthält Informationen zu den Ziel Images des Produkts. Ein Windows Installer Patch-Paket aktualisiert ein Zielimage in ein aktualisiertes Image.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: TargetImages-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868451"
---
# <a name="targetimages-table-patchwizdll"></a>TargetImages-Tabelle (Patchwiz.dll)

Die Tabelle TargetImages enthält Informationen zu den Ziel Images des Produkts. Ein Windows Installer Patch-Paket aktualisiert ein Zielimage in ein aktualisiertes Image.

In jeder Datenbank der Patcherstellung (PCP-Datei) ist eine TargetImages-Tabelle erforderlich, die mindestens einen Datensatz enthält. Diese Tabelle wird von der [uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) -Funktion verwendet.

Die TargetImages-Tabelle weist die folgenden Spalten auf.



| Spalte                | Typ    | Schlüssel | Nullwerte zulässig |
|-----------------------|---------|-----|----------|
| Ziel                | text    | J   | N        |
| Msipath               | text    |     | N        |
| SymbolPath           | text    |     | J        |
| Upgraded              | text    |     | N        |
| Auftrag                 | integer |     | N        |
| Productvalidateflags  | text    |     | J        |
| Ignoremissingsrcfiles | integer |     | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar
</dt> <dd>

Der Bezeichner für ein Zielbild. Das Patchpaket aktualisiert das in dieser Spalte angegebene Zielbild auf das aktualisierte Image, das in der aktualisierten Spalte angegeben ist. Es gibt ein oder mehrere Ziel Images für jedes aktualisierte Image. Das Zielimage muss ein vollständig dekomprimiertes Setup Abbild des Produkts sein, z. b. ein administratives Image oder ein nicht komprimiertes Setup Abbild auf einer CD-ROM. Beachten Sie, dass die [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion keine binären Patches für Dateien in kabinatendateien generiert. Der Wert in diesem Feld wird mit dem Wert im Feld aktualisiert verwendet, um die Namen der Transformationen zu generieren, die das Installationsprogramm dem Patchpaket hinzufügt.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>Msipath
</dt> <dd>

Dieses Feld gibt den vollständigen Pfad, einschließlich des Datei namens, zum Speicherort der MSI-Datei für das Zielbild an. Dies ist der Speicherort der Quelldateien für das Zielimage.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath
</dt> <dd>

Eine durch Semikolons getrennte Liste von Ordnern, die nach Symbol Dateien durchsucht werden sollen, die zur Optimierung der Generierung des binären Patches verwendet werden kann. Beachten Sie, dass die Unterverzeichnisse der in diesem Feld angegebenen Ordner nicht durchsucht werden. Ein optimierter binärer Patch kann kleiner sein. Microsoft Visual C++ müssen auf dem Computer installiert sein, der den Patch erzeugt und zum Erstellen der Symbol Dateien verwendet wird. Dieses Feld ist optional, und das Installationsprogramm erstellt einen binären Patch, auch wenn keine Symbol Dateien angegeben sind oder wenn die Symbol Dateien nicht zum Patchwiz.dll verfügbar sind.

</dd> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert
</dt> <dd>

Fremdschlüssel für die aktualisierte Spalte der [UpgradedImages-Tabelle](upgradedimages-table-patchwiz-dll-.md). Die [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion ignoriert alle aktualisierten Images, auf die nicht durch mindestens einen Datensatz der TargetImages-Tabelle verwiesen wird.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge
</dt> <dd>

Relative Reihenfolge des zielbilds. Da mehrere Ziele für ein aktualisiertes Image gepatcht werden können, bietet das Feld Order die Möglichkeit, die Transformationen in der Liste patchtransformationen zu sequenzieren. Im Allgemeinen ist die Reihenfolge vom ältesten zum neuesten Image.

</dd> <dt>

<span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>Productvalidateflags
</dt> <dd>

Das Feld productvalidateflags dient zum Angeben der Produkt Überprüfung, um zu vermeiden, dass irrelevante Transformationen angewendet werden. Der in diesem Feld eingegebene Wert muss eine 8-stellige hexadezimal Zahl und einer der gültigen Werte für den *ivalidation* -Parameter der [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) -Funktion sein. Der Standardwert ist 0x00000922, der gleich **msitransform Validate \_ \_ Updateversion** msitransform Validate  +  **\_ \_ netzwequalbaseversion**  +  **msitransform \_ Validate \_ UpgradeCode**  +  **msitransform \_ Validate \_ Product** ist.

</dd> <dt>

<span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>Ignoremissingsrcfiles
</dt> <dd>

Wenn dieses Feld auf einen Wert ungleich 0 (null) festgelegt ist, werden Dateien, die im Zielbild fehlen, vom Installationsprogramm ignoriert und während des Patchens unverändert gelassen. Dadurch können Patches erstellt werden, ohne dass das gesamte Bild erforderlich ist. Es sind nur die geänderten Dateien des Produkts und die MSI-Datei erforderlich. Dadurch kann die Zeit, die zum Generieren des Patches erforderlich ist, reduziert werden.

> [!Note]  
> Verwenden Sie nicht den ignoremissingsrcfiles-Wert mit trustmsi, der in der [Properties-Tabelle](properties-table-patchwiz-dll-.md)auf 1 festgelegt ist.

 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle akzeptiert Umgebungsvariablen als Pfade, die mit Version 4,0 von Patchwiz.dll beginnen.

 

 



