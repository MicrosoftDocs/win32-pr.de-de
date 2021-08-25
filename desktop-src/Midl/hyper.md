---
title: hyper-Attribut
description: Das Schlüsselwort hyper gibt eine 64-Bit-Ganzzahl an, die als mit oder ohne Vorzeichen deklariert werden kann.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- Hyperattribut MIDL
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f202890d2d81dcd7916f29c0330bf8e7093a7cf189e7b76a8af64dd2f0d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895260"
---
# <a name="hyper-attribute"></a>hyper-Attribut

Das Schlüsselwort **hyper gibt** eine 64-Bit-Ganzzahl an, die als mit oder ohne Vorzeichen deklariert werden kann.

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*declarator-list* 
</dt> <dd>

Gibt einen oder mehrere C-Standarddeklaratoren an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren. (Funktionsdeklaratoren und Bitfelddeklarationen sind in Strukturen, die in Remoteprozeduraufrufen übertragen werden, nicht zulässig. Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der **Hypertyp** ist einer der Basistypen der Schnittstellendefinitionssprache (Interface Definition Language, IDL). Der **Hypertyp** kann als Typspezifizierer in const-Deklarationen, [**Typedef-Deklarationen,**](typedef.md) allgemeinen Deklarationen und Funktionsdeklaratoren (als Funktions-Rückgabetypspezifizierer und als Parametertypspezifizierer) angezeigt werden. [](const.md) Informationen zum Kontext, in dem Typspezifizierer angezeigt werden, finden Sie unter [Interface Definition (IDL)-Datei.](interface-definition-idl-file.md)

> [!Note]  
> Bei 16-Bit-Plattformen ersetzt der MIDL-Compiler ganzzahlige Hyperzahlen ohne Vorzeichen durch **\_ MIDL-Uhyper**. Dadurch können Schnittstellen mit ganzzahligen Hyperzahlen ohne Vorzeichen auf Plattformen definiert werden, die 64-Bit-Ganzzahlen nicht direkt unterstützen. **\_ MIDL-Uhyper** wird in den RPC-Headerdateien definiert.

 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




