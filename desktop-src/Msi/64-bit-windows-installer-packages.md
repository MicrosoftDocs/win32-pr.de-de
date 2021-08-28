---
description: Ein 64-Bit-Paket besteht teilweise oder vollständig aus 64-Bit-Windows Installer-Komponenten.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: 64-Bit-Windows Installerpakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540ef7afc5c70eeba2bb24eb376eae8e52b8e55cec2c8622ccdcf18a804b6f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559540"
---
# <a name="64-bit-windows-installer-packages"></a>64-Bit-Windows Installerpakete

Ein 64-Bit-Paket besteht teilweise oder vollständig aus 64-Bit-Windows [Installer-Komponenten.](windows-installer-components.md) In der folgenden Liste sind die Anforderungen für jedes 64-Bit-Windows Installer-Paket aufgeführt:

-   Der Wert "Intel64" muss nur dann in das Plattformfeld der [**Eigenschaft Vorlagenzusammenfassung**](template-summary.md) eingegeben werden, wenn das Paket auf einem Intel64-Prozessor (Itanium) ausgeführt wird.
-   Der Wert "x64" muss nur dann in das Plattformfeld der Eigenschaft [**Vorlagenzusammenfassung**](template-summary.md) eingegeben werden, wenn das Paket auf einem x64-Prozessor ausgeführt wird.
-   Der Wert "Arm64" muss nur dann in das Plattformfeld der Eigenschaft [**Vorlagenzusammenfassung**](template-summary.md) eingegeben werden, wenn das Paket auf einem Arm64-Prozessor ausgeführt wird.
-   Die [](page-count-summary.md) Eigenschaft Zusammenfassung der Seitenanzahl muss auf die ganze Zahl 200 oder höher festgelegt werden, da Windows Installer 2.0 die Mindestversion ist, die 64-Bit-Komponenten installieren kann. Pakete für die Arm64-Plattform erfordern einen Wert von 500 oder höher.
-   Jede 64-Bit-Windows Installer-Komponente im Paket muss das **msidbComponentAttributes64bit-Bit** in der Spalte Attribute der [Komponententabelle enthalten.](component-table.md)

Weitere Informationen finden Sie unter [Windows Installer unter 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md) und [32-Bit-Windows Installer-Pakete](32-bit-windows-installer-packages.md).

 

 



