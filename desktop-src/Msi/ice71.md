---
description: ICE71 überprüft, ob die Media-Tabelle einen Eintrag mit diskId gleich 1 enthält.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1090eb8b1a36ed361ef763bfda3875a8fde052ed8643dceeb660c88ae954a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142514"
---
# <a name="ice71"></a>ICE71

ICE71 überprüft, ob die [Media-Tabelle](media-table.md) einen Eintrag mit diskId gleich 1 enthält. (Windows Installer geht davon aus, dass sich .msi Paket auf Datenträger 1 befindet.)

## <a name="result"></a>Ergebnis

ICE71 gibt einen Fehler zurück, wenn die Media-Tabelle keinen Eintrag mit diskId gleich 1 enthält.

## <a name="example"></a>Beispiel

ICE71 meldet den folgenden Fehler für das gezeigte Beispiel.

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 behebt diesen Fehler, und ändern Sie die DiskId des Eintrags, in dem das Paket gespeichert ist, in 1.

[Medientabelle](media-table.md) (partiell)



| DiskId |
|--------|
| 2      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



