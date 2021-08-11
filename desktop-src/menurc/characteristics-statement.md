---
title: Merkmale-Anweisung
description: Definiert Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Definitions Dateien lesen und schreiben.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Merkmale von Anweisungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037968"
---
# <a name="characteristics-statement"></a>Merkmale-Anweisung

Definiert Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Definitions Dateien lesen und schreiben. Der angegebene **DWORD** -Wert wird mit der Ressource in der kompilierten res-Datei angezeigt. Der Wert wird jedoch nicht in der ausführbaren Datei gespeichert und hat keine Bedeutung für das System.

Die **Characteristics** -Anweisung wird vor dem Anfang des Texts der Ressourcendefinition " [**Accelerators**](accelerators-resource.md)", " [**Dialog**](dialog-resource.md)", " [**Menü**](menu-resource.md)", " [**RCDATA**](rcdata-resource.md)" oder " [**STRINGTABLE**](stringtable-resource.md) " angezeigt. Der angegebene Wert gilt nur für diese Ressource.

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*DWORD*
</dt> <dd>

Benutzerdefinierter **DWORD** -Wert.

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Accelerators**](accelerators-resource.md)
</dt> <dt>

[**Dialog**](dialog-resource.md)
</dt> <dt>

[**Kurse**](language-statement.md)
</dt> <dt>

[**Stehen**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




