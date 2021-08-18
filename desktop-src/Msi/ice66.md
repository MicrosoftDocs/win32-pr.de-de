---
description: ICE66 verwendet die Tabellen in der Datenbank, um zu bestimmen, welches Schema Ihre Datenbank verwenden soll.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023450a451a412c47c21904ab96a13e4513c71f8327966dffa5b657b1b65bb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787400"
---
# <a name="ice66"></a>ICE66

ICE66 verwendet die Tabellen in der Datenbank, um zu bestimmen, welches Schema Ihre Datenbank verwenden soll.

Einige Funktionen sind möglicherweise nur verfügbar, wenn das Paket auf einem System mit einer aktuellen Version Windows Installer installiert ist.

## <a name="result"></a>Ergebnis

ICE66 gibt eine Warnung aus, wenn Ihre Datenbank das falsche Schema verwendet.

## <a name="example"></a>Beispiel

ICE66 meldet die folgende Warnung für das gezeigte Beispiel.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

Diese Warnung kann ignoriert werden, wenn Sie möchten, dass Ihr Paket mithilfe einer aktuellen Version Windows Installer installiert wird. Wenn Ihr Paket beispielsweise nur ab Version 2.0 installiert werden kann, ändern Sie das Paketschema (PID \_ PAGECOUNT) in 200.

[IsolatedComponent-Tabelle](isolatedcomponent-table.md)



| Freigegebene \_ Komponente | \_Komponentenanwendung |
|-------------------|------------------------|
| Komponente1        | Component2             |



 

[Zusammenfassungsinformationsstream](summary-information-stream.md)



| PIDt           | Wert |
|----------------|-------|
| PID \_ PAGECOUNT | 100   |



 

## <a name="table-used-during-execution"></a>Während der Ausführung verwendete Tabelle:

[\_Spaltentabelle](-columns-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



