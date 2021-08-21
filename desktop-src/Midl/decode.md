---
title: Decodierungsattribut
description: Das ACF-Attribut \decode\ gibt an, dass eine Prozedur oder ein Typ Deserialisierungsunterstützung benötigt.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- Decodierungsattribut MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30c70c821906bcfa4dedb8dbe87aab882866a4f21b7d561b16d3613f9041e0f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384725"
---
# <a name="decode-attribute"></a>Decodierungsattribut

Das **\[ Decodieren \]** des ACF-Attributs gibt an, dass eine Prozedur oder ein Typ Deserialisierungsunterstützung benötigt.

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

*interface-attribute-list* 
</dt> <dd>

Gibt andere Attribute an, die für die gesamte Schnittstelle gelten.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Schnittstellendefinition* 
</dt> <dd>

Gibt IDL-Anweisungen an, die die Definition der Schnittstelle bilden.

</dd> <dt>

*op-attribute-list* 
</dt> <dd>

Gibt andere betriebsbereite Attribute an, die für die Prozedur gelten, z. B. **\[** [**codieren.**](encode.md) **\]**

</dd> <dt>

*proc-name* 
</dt> <dd>

Gibt den Namen der Prozedur an.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Gibt andere Attribute an, z. B. **\[** [**codieren**](encode.md) **\]** und **\[** [**zuordnen.**](allocate.md) **\]**

</dd> <dt>

*type-name* 
</dt> <dd>

Gibt einen in der IDL-Datei definierten Typ an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ \] Decodierungsattribut** bewirkt, dass der MIDL-Compiler Code generiert, mit dem eine Anwendung serialisierte Daten aus einem Puffer abrufen kann. Das **\[** [](encode.md) **\]** Codierungsattribut bietet Serialisierungsunterstützung und generiert den Code zum Serialisieren von Daten in einen Puffer.

Verwenden Sie die **\[** [**Codierungs-**](encode.md) **\]** und **\[ \] Decodierungsattribute** in einem ACF, um Serialisierungscode für Prozeduren oder Typen zu generieren, die in der IDL-Datei einer Schnittstelle definiert sind. Bei Verwendung als Schnittstellenattribut gilt **\[ die Decodierung \]** für alle Typen und Prozeduren, die in der IDL-Datei definiert sind. Bei Verwendung als Typattribut gilt **\[ die Decodierung \]** nur für den angegebenen Typ. Bei Verwendung als operatives Attribut gilt **\[ die Decodierung \]** nur für diese Prozedur.

Weitere Informationen zur Verwendung dieser Serialisierungsunterstützung finden Sie unter [Serialisierungsdienste](/windows/desktop/Rpc/serialization-services) und **\[** [**Codieren**](encode.md) **\]** von .

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Codieren**](encode.md)
</dt> </dl>

 

 