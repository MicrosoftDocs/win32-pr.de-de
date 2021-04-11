---
description: Gibt die Mesh-Daten abzüglich der Positionsdaten an.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: "\"F\"-Daten"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52af6096357c4855d2dc34442c6cd4814b6713b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123854"
---
# <a name="fvfdata"></a>"F"-Daten

Gibt die Mesh-Daten abzüglich der Positionsdaten an.

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

Hierbei gilt:

-   DWF VF: ein f-Code.
-   ndwords: Binärdaten. Die Anzahl der DWORDs.
-   Data \[ ndwords \] : Array von DWords, die die Daten in jedem Scheitelpunkt Element enthalten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



