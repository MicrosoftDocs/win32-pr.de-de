---
description: Die Tabelle TargetImages enthält Informationen zu den Zielimages des Produkts. Ein Windows Installer-Patchpaket aktualisiert ein Zielimage in ein aktualisiertes Image.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: TargetImages-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec35a9090f89e93e807cda9429ae48d8cc28d175acc4c83e97150e3a98ce5fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893590"
---
# <a name="targetimages-table-patchwizdll"></a>TargetImages-Tabelle (Patchwiz.dll)

Die Tabelle TargetImages enthält Informationen zu den Zielimages des Produkts. Ein Windows Installer-Patchpaket aktualisiert ein Zielimage in ein aktualisiertes Image.

Eine TargetImages-Tabelle, die mindestens einen Datensatz enthält, ist in jeder Patcherstellungsdatenbank (PCP-Datei) erforderlich. Diese Tabelle wird von der [UiCreatePatchPackage-Funktion](uicreatepatchpackage-patchwiz-dll-.md) verwendet.

Die Tabelle TargetImages enthält die folgenden Spalten.



| Spalte                | Typ    | Key | Nullwerte zulässig |
|-----------------------|---------|-----|----------|
| Ziel                | text    | J   | N        |
| MsiPath               | text    |     | N        |
| SymbolPaths           | text    |     | J        |
| Upgraded              | text    |     | N        |
| Auftrag                 | integer |     | N        |
| ProductValidateFlags  | text    |     | J        |
| IgnoreMissingSrcFiles | integer |     | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Ziel
</dt> <dd>

Bezeichner für ein Zielbild. Das Patchpaket aktualisiert das in dieser Spalte angegebene Zielimage auf das aktualisierte Image, das in der Spalte Aktualisiert angegeben ist. Es gibt mindestens ein Zielimage für jedes aktualisierte Image. Das Zielimage muss ein vollständig unkomprimiertes Setupimage des Produkts sein, z. B. ein Administratives Image oder ein nicht komprimiertes Setupimage auf einer CD-ROM. Beachten Sie, dass die [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) keine binären Patches für Dateien in Schränken generiert. Der Wert in diesem Feld wird zusammen mit dem Wert im Feld Upgrade verwendet, um die Namen der Transformationen zu generieren, die das Installationsprogramm dem Patchpaket hinzufügt.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

Dieses Feld gibt den vollständigen Pfad einschließlich des Dateinamens zum Speicherort der .msi-Datei für das Zielimage an. Dies ist der Speicherort der Quelldateien für das Zielimage.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Eine durch Semikolons getrennte Liste von Ordnern, die nach Symboldateien durchsucht werden sollen, die zum Optimieren der Generierung des binären Patches verwendet werden können. Beachten Sie, dass die in diesem Feld angegebenen Unterverzeichnisse von Ordnern nicht durchsucht werden. Ein optimierter binärer Patch ist möglicherweise kleiner. Microsoft Visual C++ müssen auf dem Computer installiert sein, der den Patch generiert und zum Erstellen der Symboldateien verwendet wird. Dieses Feld ist optional, und das Installationsprogramm erstellt einen binären Patch, auch wenn keine Symboldateien angegeben sind oder wenn die Symboldateien für Patchwiz.dll nicht mehr verfügbar sind.

</dd> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert
</dt> <dd>

Fremdschlüssel für die Spalte "Upgraded" der [Tabelle "UpgradedImages".](upgradedimages-table-patchwiz-dll-.md) Die [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) ignoriert alle aktualisierten Images, auf die nicht von mindestens einem Datensatz der Tabelle TargetImages verwiesen wird.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Bestellung
</dt> <dd>

Relative Reihenfolge des Zielbilds. Da mehrere Ziele auf ein aktualisiertes Image gepatcht werden können, bietet das Feld Order eine Möglichkeit, die Transformationen in der Liste der Patchtransformationen zu sequenzieren. In der Regel ist die Reihenfolge vom ältesten zum neuesten Bild.

</dd> <dt>

<span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags
</dt> <dd>

Das Feld ProductValidateFlags wird verwendet, um die Produktüberprüfung anzugeben, um das Anwenden irrelevanter Transformationen zu vermeiden. Der in dieses Feld eingegebene Wert muss eine achtstellige Hexadezimalzahl und einer der gültigen Werte für den *iValidation-Parameter* der [**MsiCreateTransformSummaryInfo-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) sein. Der Standardwert ist 0x00000922, der **MSITRANSFORM \_ VALIDATE \_ UPDATEVERSION**  +  **MSITRANSFORM \_ VALIDATE \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ VALIDATE \_ UPGRADECODE**  +  **MSITRANSFORM \_ VALIDATE \_ PRODUCT** entspricht.

</dd> <dt>

<span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles
</dt> <dd>

Wenn dieses Feld auf einen Wert ungleich 0 (null) festgelegt ist, werden Dateien, die im Zielimage fehlen, vom Installationsprogramm ignoriert und während des Patchens unverändert gelassen. Dadurch können Patches erstellt werden, ohne dass das gesamte Image erforderlich ist. nur die geänderten Dateien des Produkts und die .msi Datei erforderlich sind. Dies kann die Zeit verkürzen, die zum Generieren des Patches erforderlich ist.

> [!Note]  
> Verwenden Sie den IgnoreMissingSrcFiles-Wert nicht, wenn TrustMsi in der [Eigenschaftentabelle](properties-table-patchwiz-dll-.md)auf 1 festgelegt ist.

 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle akzeptiert Umgebungsvariablen als Pfade ab Version 4.0 Patchwiz.dll.

 

 



