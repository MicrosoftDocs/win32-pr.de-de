---
title: Versions Anweisung
description: Definiert Versionsinformationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menüs der Versions Anweisung und andere Ressourcen
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718510"
---
# <a name="version-statement"></a>Versions Anweisung

Definiert Versionsinformationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben. Der angegebene *DWORD* -Wert wird mit der Ressource in der kompilierten angezeigt. RES-Datei. Der Wert wird jedoch nicht in der ausführbaren Datei gespeichert und hat keine Bedeutung für das System.

Die **Version** -Anweisung wird vor dem Anfang des Texts der Ressourcendefinition " [**Accelerators**](accelerators-resource.md)", " [**DIALOGEX**](dialogex-resource.md)", " [**Menu**](menu-resource.md)", " [**RCDATA**](rcdata-resource.md)" oder " [**STRINGTABLE**](stringtable-resource.md) " angezeigt. Der angegebene Wert gilt nur für diese Ressource.

``` syntax
VERSION dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*DWORD*
</dt> <dd>

Ein benutzerdefinierter **DWORD** -Wert.

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Accelerators**](accelerators-resource.md)
</dt> <dt>

[**Charakteristik**](characteristics-statement.md)
</dt> <dt>

[**Kurse**](language-statement.md)
</dt> <dt>

[**Stehen**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




