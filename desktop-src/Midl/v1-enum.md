---
title: v1_enum-Attribut
description: Das Attribut \v1 \_ enum\ weist an, dass der angegebene Enumerationstyp als 32-Bit-Entität und nicht als 16-Bit-Standard übertragen wird.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum-Attribut MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7afb814cde879f0ada5124b1a19d8ac8b8c851deafcda7e75295a6e5338f68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382784"
---
# <a name="v1_enum-attribute"></a>\_v1-Enumerationsattribut

Das **\[ v1-Enumerationsattribut \_ \]** weist an, dass der angegebene Enumerationstyp nicht als 16-Bit-Standard, sondern als 32-Bit-Entität übertragen wird.

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>Parameter

Dieses Attribut verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Die Verwendung des **\[ v1-Enumerationsattributs \_ \]** zum Übertragen eines aufzählenden Typs als 32-Bit-Entität erhöht die Effizienz des Marshallings und Desmarshalings von Daten, wenn eine solche Enumeration in Strukturen oder Unions eingebettet ist.

Zur Verbesserung der Leistung wird empfohlen, das **\[ v1-Enumerationsattribut \_ \]** auf Enumeratoren in 32-Bit-Anwendungen anzuwenden. Beachten Sie jedoch, dass der C-Compiler auf 16-Bit-Plattformen einen enumerierten Typ [](int.md)als 16-Bit-Int behandelt. Daher müssen 16-Bit-Clientanwendungen [**Enumerationstypen**](enum.md) für die Remoteübertragung in [**long**](long.md) konvertieren, um das Überschreiben von Daten oder das Senden falscher Werte zu vermeiden.

## <a name="examples"></a>Beispiele

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Enum**](enum.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> </dl>

 

 




