---
title: v1_enum-Attribut
description: Das \v1 enum\-Attribut gibt an, dass der angegebene enumerierte Typ als \_ 32-Bit-Entität und nicht als 16-Bit-Standard übertragen wird.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum MIDL-Attribut
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
# <a name="v1_enum-attribute"></a>\_v1-Enum-Attribut

Das **\[ \_ \] v1-Enum-Attribut** gibt an, dass der angegebene aufzählte Typ als 32-Bit-Entität und nicht als 16-Bit-Standard übertragen wird.

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>Parameter

Dieses Attribut verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Die Verwendung des **\[ \_ \] v1-Enumerationsattributs** zum Übertragen eines enumerationsbasierten Typs als 32-Bit-Entität erhöht die Effizienz des Marshallings und Desmarshalings von Daten, wenn eine solche Enumeration in Strukturen oder Unions eingebettet ist.

Zur Verbesserung der Leistung wird empfohlen, das **\[ \_ \] Enumeratorattribut v1** auf Enumeratoren in 32-Bit-Anwendungen zu anwenden. Beachten Sie jedoch, dass der C-Compiler auf 16-Bit-Plattformen einen aufzählten Typ als 16-Bit-Int [**behandelt.**](int.md) Daher müssen 16-Bit-Clientanwendungen [**Enum-Typen**](enum.md) für die Remoteübertragung in long konvertieren, um zu vermeiden, dass Daten überschreiben oder falsche Werte senden. [](long.md)

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

 

 




