---
title: byte-Attribut
description: Das byte-Schlüsselwort gibt ein 8-Bit-Datenelement an.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- Byteattribut MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a271cc81fe97fb25850bfe4dcb7d2edb55ba3c69805dab17d013bc646768e87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384724"
---
# <a name="byte-attribute"></a>byte-Attribut

Das **byte-Schlüsselwort** gibt ein 8-Bit-Datenelement an.

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen MIDL-Bezeichner an. Gültige MIDL-Bezeichner bestehen aus bis zu 31 alphanumerischen und/oder Unterstrichen und müssen mit einem alphabetischen oder Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein **Bytedatenelement** wird für die Übertragung im Netzwerk nicht wie ein [**char-Typ konvertiert.**](char-idl.md)

Der **Bytetyp** ist einer der Basistypen der Schnittstellendefinitionssprache (Interface Definition Language, IDL). Der **Bytetyp** kann als Typspezifizierer in const-Deklarationen, [](const.md) [**TypeDef-Deklarationen,**](typedef.md) allgemeinen Deklarationen und Funktionsdeklaratoren (als Funktions-Rückgabetypspezifizierer und als Parametertypspezifizierer) angezeigt werden. Informationen zum Kontext, in dem Typspezifizierer angezeigt werden, finden Sie unter [Interface Definition (IDL)-Datei.](interface-definition-idl-file.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




