---
title: Language-Anweisung
description: Definiert die Sprache für alle Ressourcen bis zur nächsten sprach Anweisung oder bis zum Ende der Datei.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Sprach Anweisungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516781"
---
# <a name="language-statement"></a>Language-Anweisung

Definiert die Sprache für alle Ressourcen bis zur nächsten **sprach** Anweisung oder bis zum Ende der Datei.

Wenn die **Language** -Anweisung vor dem Anfang des Texts einer Schnellansicht [**,**](accelerators-resource.md) [**DIALOGEX**](dialogex-resource.md), [**Menü**](menu-resource.md), [**RCDATA**](rcdata-resource.md)oder [**STRINGTABLE**](stringtable-resource.md) -Ressourcendefinition angezeigt wird, gilt die angegebene Sprache nur für diese Ressource.

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span id="language"></span><span id="LANGUAGE"></span>*Kurse*
</dt> <dd>

Der Sprachen Bezeichner.

</dd> <dt>

<span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*unter Sprachen*
</dt> <dd>

Unter Sprachen-ID.

</dd> </dl>

Weitere Informationen finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Accelerators**](accelerators-resource.md)
</dt> <dt>

[**Charakteristik**](characteristics-statement.md)
</dt> <dt>

[**Stehen**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 