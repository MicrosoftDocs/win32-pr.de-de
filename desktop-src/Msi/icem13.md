---
description: ICEM13 überprüft, ob das Mergemodul keine Herausgeber Richtlinie und keine konfigurationsassemblys enthält.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864404"
---
# <a name="icem13"></a>ICEM13

ICEM13 überprüft, ob das Mergemodul keine Herausgeber Richtlinie und keine konfigurationsassemblys enthält. Herausgeber Richtlinien und konfigurationsassemblys sollten nicht in Mergemodulen enthalten sein, die für die Weiterverteilung vorgesehen sind, da dies Auswirkungen auf andere Anwendungen auf dem Computer

Dieses ICEM ist in der Datei "Mergemod. Cub" verfügbar, die im SDK für Windows Installer 2,0 und höher bereitgestellt wird. Weitere Informationen finden Sie unter [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Ergebnis

ICEM13 gibt eine Warnmeldung aus, wenn Sie eine im Komponenten Feld der [MsiAssembly-Tabelle](msiassembly-table.md) des Mergemoduls angegebene Komponente findet, bei der es sich um eine Herausgeber Richtlinie oder eine Konfigurationsassembly handelt.

## <a name="example"></a>Beispiel

ICEM13 gibt die folgende Warnmeldung aus, wenn eine Zeile in der [MsiAssembly-Tabelle](msiassembly-table.md) gefunden wird, in der die Komponente " \[ 1 \] " im Komponenten Feld angegeben ist, bei der es sich um eine Herausgeber Richtlinie oder eine Konfigurationsassembly handelt, die im Mergemodul enthalten ist

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

Es ist möglich, Herausgeber Richtlinien und konfigurationsassemblys mithilfe der Windows Installer zu installieren. es wird jedoch nicht empfohlen, diese Assemblys in Mergemodulen neu zu verteilen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



