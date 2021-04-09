---
description: Ein 64-Bit-Paket besteht teilweise oder vollständig aus 64-Bit-Windows Installer Komponenten.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: 64-Bit-Windows Installer Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864540"
---
# <a name="64-bit-windows-installer-packages"></a>64-Bit-Windows Installer Pakete

Ein 64-Bit-Paket besteht teilweise oder vollständig aus 64-Bit- [Windows Installer](windows-installer-components.md) Komponenten. In der folgenden Liste sind die Anforderungen für alle 64-Bit-Windows Installer Pakets aufgeführt:

-   Der Wert "Intel64" muss im Feld Platform der [**Template Summary**](template-summary.md) -Eigenschaft nur dann eingegeben werden, wenn das Paket auf einem Intel64-Prozessor (Itanium) ausgeführt wird.
-   Der Wert "x64" muss in das Feld "Platform" der [**Template Summary**](template-summary.md) -Eigenschaft eingegeben werden, wenn das Paket auf einem x64-Prozessor ausgeführt wird.
-   Der Wert "Arm64" muss in das Feld Platform der [**Template Summary**](template-summary.md) -Eigenschaft eingegeben werden, wenn das Paket auf einem Arm64-Prozessor ausgeführt wird.
-   Die [**Seitenanzahl-Zusammenfassungs**](page-count-summary.md) Eigenschaft muss auf die ganze Zahl 200 oder höher festgelegt werden, da Windows Installer 2,0 die Mindestversion ist, die die Installation von 64-Bit-Komponenten unterstützt. Für Pakete für die Arm64-Plattform ist der Wert 500 oder höher erforderlich.
-   Jede 64-Bit-Windows Installer Komponente im Paket muss das **msidbComponentAttributes64bit** -Bit in der Spalte Attribute der [Komponenten Tabelle](component-table.md)enthalten.

Weitere Informationen finden Sie unter [Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md) und [32-Bit-Windows Installer Paketen](32-bit-windows-installer-packages.md).

 

 



