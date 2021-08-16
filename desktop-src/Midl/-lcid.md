---
title: Schalter "/lcid"
description: Mit der Compileroption /lcid MIDL können Sie internationale Zeichen in Ihren Eingabedateien, Dateinamen und Verzeichnispfaden verwenden.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /lcid switch MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ceff1f9a4ef2f6c95a8dac12ff689995efe4fdd3619cf48e11043967fec053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385513"
---
# <a name="lcid-switch"></a>Schalter "/lcid"

Mit **der Compileroption /lcid** MIDL können Sie internationale Zeichen in Ihren Eingabedateien, Dateinamen und Verzeichnispfaden verwenden.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

*Localeid* 
</dt> <dd>

Gibt den 32-Bit-Locale Identifier an, der in Windows National Language Support verwendet wird. Der Locale Identifier muss in decimal angegeben werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Innerhalb der Eingabedateien können Sie lokalisierte Kommentare, Zeichenfolgen, Hilfezeichenfolgen und Bezeichner verwenden. Insbesondere der Schalter **/lcid** bietet vollständige DBCS-Unterstützung für die Darstellung von chinesischen Sprachen wie Japanisch, Chinesisch und Koreanisch.

> [!Note]  
> Der **Schalter /lcid** ist ab MIDL-Version 3.01.75 verfügbar.

 

## <a name="examples"></a>Beispiele

**midl /lcid 1041 iface.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> </dl>

 

 




