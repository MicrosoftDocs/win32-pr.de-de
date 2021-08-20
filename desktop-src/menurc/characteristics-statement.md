---
title: CHARACTERISTICS-Anweisung
description: Definiert Informationen zu einer Ressource, die von Tools verwendet werden können, die Ressourcendefinitionsdateien lesen und schreiben.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- CHARACTERISTICS-Anweisung Menus and Other Resources
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9910a86263d14dd928fb01347dfea4fd6c796c23b4e5d42d69cdba4bc40e14c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034313"
---
# <a name="characteristics-statement"></a>CHARACTERISTICS-Anweisung

Definiert Informationen zu einer Ressource, die von Tools verwendet werden können, die Ressourcendefinitionsdateien lesen und schreiben. Der angegebene **DWORD-Wert** wird mit der Ressource in der kompilierten RES-Datei angezeigt. Der Wert wird jedoch nicht in der ausführbaren Datei gespeichert und hat keine Bedeutung für das System.

Die **CHARACTERISTICS-Anweisung** wird vor dem Anfang des Textkörpers einer [**ACCELERATORS-,**](accelerators-resource.md) [**DIALOG-,**](dialog-resource.md) [**MENU-,**](menu-resource.md) [**RCDATA-**](rcdata-resource.md)oder [**STRINGTABLE-Ressourcendefinition**](stringtable-resource.md) angezeigt. Der angegebene Wert gilt nur für diese Ressource.

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*Dword*
</dt> <dd>

Benutzerdefinierter **DWORD-Wert.**

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Beschleuniger**](accelerators-resource.md)
</dt> <dt>

[**DIALOG**](dialog-resource.md)
</dt> <dt>

[**Sprache**](language-statement.md)
</dt> <dt>

[**Menü**](menu-resource.md)
</dt> <dt>

[**Rcdata**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> </dl>

 

 




