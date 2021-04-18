---
title: Byte-Attribut
description: Das Byte-Schlüsselwort gibt ein 8-Bit-Datenelement an.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- Byte-Attribut-Mittell
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340468"
---
# <a name="byte-attribute"></a>Byte-Attribut

Das **Byte** -Schlüsselwort gibt ein 8-Bit-Datenelement an.

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen Mittell-Bezeichner an. Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein **Byte** -Datenelement wird bei der Übertragung im Netzwerk nicht als [**char**](char-idl.md) -Typ konvertiert.

Der **Bytetyp** ist einer der Basis Typen der IDL (Interface Definition Language). Der **Bytetyp** kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




