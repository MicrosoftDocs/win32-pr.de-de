---
title: Attribut decodieren
description: Das Attribut \ Decode \ ACF gibt an, dass eine Prozedur oder ein Typ die deserialisierungsunterstützung benötigt.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- Decodieren von attributmittell
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314906"
---
# <a name="decode-attribute"></a>Attribut decodieren

Das Attribut "ACF **\[ decodieren \]** " gibt an, dass eine Prozedur oder ein Typ die deserialisierungsunterstützung benötigt.

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Gibt andere Attribute an, die auf die gesamte Schnittstelle angewendet werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Schnittstellen Definition* 
</dt> <dd>

Gibt IDL-Anweisungen an, die die Definition der-Schnittstelle bilden.

</dd> <dt>

*OP-Attribute-List* 
</dt> <dd>

Gibt andere operative Attribute an, die für die Prozedur gelten, z **\[** . b. [**Codieren**](encode.md) **\]** .

</dd> <dt>

*proc-Name* 
</dt> <dd>

Gibt den Namen der Prozedur an.

</dd> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt andere Attribute an, z **\[** . b. [**Codieren**](encode.md) **\]** und **\[** [**zuordnen**](allocate.md) **\]** .

</dd> <dt>

*Typname* 
</dt> <dd>

Gibt einen Typ an, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Attribut " **\[ decodieren \]** " bewirkt, dass der Mittell-Compiler Code generiert, mit dem eine Anwendung serialisierte Daten aus einem Puffer abrufen kann. Das **\[** [**Codieren**](encode.md) - **\]** Attribut bietet Serialisierungsunterstützung und erzeugt den Code zum Serialisieren von Daten in einen Puffer.

Verwenden **\[** Sie die Attribute [**Codieren**](encode.md) **\]** und **\[ decodieren \]** in einer ACF, um Serialisierungscode für Prozeduren oder Typen zu generieren, die in der IDL-Datei einer Schnittstelle definiert sind. Wenn die **\[ Decodierung \]** als Schnittstellen Attribut verwendet wird, gilt sie für alle Typen und Prozeduren, die in der IDL-Datei definiert sind. Wenn die **\[ Decodierung \]** als Type-Attribut verwendet wird, gilt sie nur für den angegebenen Typ. Wenn die **\[ Decodierung \]** als Betriebs Attribut verwendet wird, gilt sie nur für diese Prozedur.

Weitere Informationen zur Verwendung dieser Serialisierungsunterstützung finden Sie unter [Serialisierung Services](/windows/desktop/Rpc/serialization-services) und **\[** [**Codieren**](encode.md) **\]** .

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Codieren**](encode.md)
</dt> </dl>

 

 