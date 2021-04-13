---
title: /LCID-Schalter
description: Mit der/LCID-Compileroption können Sie internationale Zeichen in ihren Eingabedateien, Dateinamen und Verzeichnis Pfaden verwenden.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /LCID-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312948"
---
# <a name="lcid-switch"></a>/LCID-Schalter

Mit der **/LCID** -Compileroption können Sie internationale Zeichen in ihren Eingabedateien, Dateinamen und Verzeichnis Pfaden verwenden.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*LocaleID* 
</dt> <dd>

Gibt den 32-Bit-Gebiets Schema Bezeichner an, der in der Unterstützung von Windows- Der Gebiets Schema Bezeichner sollte in Dezimalzahlen angegeben werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In den Eingabedateien können Sie lokalisierte Kommentare, Zeichen folgen, helpstrings und Bezeichner verwenden. Der **/LCID** -Schalter bietet insbesondere vollständige DBCS-Unterstützung, um asiatische Sprachen wie Japanisch, Chinesisch und Koreanisch darzustellen.

> [!Note]  
> Der **/LCID** -Schalter ist mit der mittleren l-Version 3.01.75 und höher verfügbar.

 

## <a name="examples"></a>Beispiele

**Mittel l/LCID 1041 iface. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> </dl>

 

 




