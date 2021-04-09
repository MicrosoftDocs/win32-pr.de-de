---
description: ICE66 verwendet die Tabellen in der-Datenbank, um zu bestimmen, welches Schema von der Datenbank verwendet werden soll.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753016"
---
# <a name="ice66"></a>ICE66

ICE66 verwendet die Tabellen in der-Datenbank, um zu bestimmen, welches Schema von der Datenbank verwendet werden soll.

Einige Funktionen sind möglicherweise nur verfügbar, wenn das Paket auf einem System mit einer aktuellen Windows Installer Version installiert ist.

## <a name="result"></a>Ergebnis

ICE66 gibt eine Warnung aus, wenn die Datenbank das falsche Schema verwendet.

## <a name="example"></a>Beispiel

ICE66 meldet die folgende Warnung für das gezeigte Beispiel.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

Diese Warnung kann ignoriert werden, wenn das Paket mit einer aktuellen Windows Installer Version installiert werden soll. Wenn Sie z. b. möchten, dass das Paket nur in Version 2,0 oder höher installiert werden kann, ändern Sie das Paket Schema (PID \_ Page count) in 200.

[Isolatedcomponent-Tabelle](isolatedcomponent-table.md)



| Frei \_ gegebene Komponente | Komponenten \_ Anwendung |
|-------------------|------------------------|
| Component1        | Component2             |



 

[Zusammenfassungs Informationsdaten Strom](summary-information-stream.md)



| Pidt           | Wert |
|----------------|-------|
| PID- \_ PageCount | 100   |



 

## <a name="table-used-during-execution"></a>Während der Ausführung verwendete Tabelle:

[\_Columns-Tabelle](-columns-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



