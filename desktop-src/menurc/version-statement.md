---
title: VERSION-Anweisung
description: Definiert Versionsinformationen zu einer Ressource, die von Tools verwendet werden können, die Ressourcendateien lesen und schreiben.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- VERSIONS-Anweisungsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c95f2af63d5c7bdb499d371892d0c2fa6ddb875fda5daf5b19fd0d188a478fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776660"
---
# <a name="version-statement"></a>VERSION-Anweisung

Definiert Versionsinformationen zu einer Ressource, die von Tools verwendet werden können, die Ressourcendateien lesen und schreiben. Der angegebene *DWORD-Wert* wird mit der Ressource im kompilierten angezeigt. RES-Datei. Der Wert wird jedoch nicht in der ausführbaren Datei gespeichert und hat keine Bedeutung für das System.

Die **VERSION-Anweisung** wird vor dem Anfang des Textkörpers einer [**ACCELERATORS-,**](accelerators-resource.md) [**DIALOGEX-,**](dialogex-resource.md) [**MENU-,**](menu-resource.md) [**RCDATA-**](rcdata-resource.md)oder [**STRINGTABLE-Ressourcendefinition**](stringtable-resource.md) angezeigt. Der angegebene Wert gilt nur für diese Ressource.

``` syntax
VERSION dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*Dword*
</dt> <dd>

Ein benutzerdefinierter **DWORD-Wert.**

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beschleuniger**](accelerators-resource.md)
</dt> <dt>

[**Merkmale**](characteristics-statement.md)
</dt> <dt>

[**Sprache**](language-statement.md)
</dt> <dt>

[**Menü**](menu-resource.md)
</dt> <dt>

[**Rcdata**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> </dl>

 

 




