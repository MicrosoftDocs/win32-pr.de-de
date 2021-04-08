---
description: ICE71 überprüft, ob die Medien Tabelle einen Eintrag mit einem DiskId-Wert gleich 1 enthält.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960482"
---
# <a name="ice71"></a>ICE71

ICE71 überprüft, ob die [Medien Tabelle](media-table.md) einen Eintrag mit einem DiskId-Wert gleich 1 enthält. (Windows Installer geht davon aus, dass sich das MSI-Paket auf Datenträger 1 befindet.)

## <a name="result"></a>Ergebnis

ICE71 gibt einen Fehler zurück, wenn die Medien Tabelle keinen Eintrag enthält, bei dem DiskId gleich 1 ist.

## <a name="example"></a>Beispiel

ICE71 meldet den folgenden Fehler für das gezeigte Beispiel.

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 beheben Sie diesen Fehler, und ändern Sie die DiskId des Eintrags, in dem das Paket gespeichert ist, auf 1.

[Medien Tabelle](media-table.md) (partiell)



| DiskId |
|--------|
| 2      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



