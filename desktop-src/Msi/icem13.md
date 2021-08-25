---
description: ICEM13 überprüft, ob das Mergemodul keine Herausgeberrichtlinien- und Konfigurationsassemblys enthält.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678b89e14cb699bb6207be5c2e14473de2a743494b47ff5ae5e0ccda2a9cc9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894280"
---
# <a name="icem13"></a>ICEM13

ICEM13 überprüft, ob das Mergemodul keine Herausgeberrichtlinien- und Konfigurationsassemblys enthält. Publisher Richtlinien- und Konfigurationsassemblys sollten nicht in merge-Modulen enthalten sein, die für die Neuverteilung vorgesehen sind, da sich dies auf andere Anwendungen auf dem Computer eines Benutzers auswirken kann.

Dieses ICEM ist in der Datei Mergemod.cub verfügbar, die im Windows Installer 2.0 SDK und höher bereitgestellt wird. Weitere Informationen finden Sie [unter Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Ergebnis

ICEM13 gibt eine Warnmeldung aus, wenn eine Komponente gefunden wird, die im Feld Komponente der [MsiAssembly-Tabelle](msiassembly-table.md) des Mergemoduls angegeben ist, die eine Herausgeberrichtlinie oder Konfigurationsassembly ist.

## <a name="example"></a>Beispiel

ICEM13 gibt die folgende Warnmeldung aus, wenn eine Zeile in der [MsiAssembly-Tabelle](msiassembly-table.md) mit der Komponente "1" gefunden wird, die im Feld Komponente angegeben ist und eine Herausgeberrichtlinie oder Konfigurationsassembly ist, die im Mergemodul enthalten \[ \] ist.

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

Es ist möglich, Herausgeberrichtlinien- und Konfigurationsassemblys mithilfe des Windows Installers zu installieren. Es wird nicht empfohlen, diese Assemblys in Mergemodulen neu zu verteilen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Merge Module ICE Reference](merge-module-ice-reference.md)
</dt> </dl>

 

 



