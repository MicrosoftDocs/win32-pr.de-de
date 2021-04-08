---
title: v1_enum-Attribut
description: Das Attribut \ v1 \_ enum \ leitet, dass der angegebene enumerierte Typ als 32-Bit-Entität und nicht als 16-Bit-Standardwert übertragen wird.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum Attribut-Mittel l
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857439"
---
# <a name="v1_enum-attribute"></a>v1-Aufzählungs \_ Attribut

Das Attribut **\[ v1 \_ Enumeration \]** leitet, dass der angegebene enumerierte Typ als 32-Bit-Entität und nicht als 16-Bit-Standardwert übertragen wird.

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>Parameter

Dieses Attribut hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Die Verwendung des **\[ v1 \_ \]** -Enumerationsattributs, um einen enumerierten Typ als 32-Bit-Entität zu übertragen, erhöht die Effizienz des Marshalling und entmarshalling von Daten, wenn eine solche Enumeration in Strukturen oder Unions eingebettet ist.

Um die Leistung zu verbessern, wird empfohlen, das **\[ v1- \_ \] Enumeration** -Attribut auf Enumeratoren in 32-Bit-Anwendungen anzuwenden. Beachten Sie jedoch, dass der C-Compiler auf 16-Bit-Plattformen einen enumerierten Typ als 16-Bit- [**int**](int.md)behandelt. Daher müssen für 16-Bit-Client Anwendungen [](enum.md) Enumerationstypen für die Remote Übertragung in [**Long**](long.md) konvertiert werden, um das Überschreiben von Daten oder das Senden falscher Werte zu vermeiden.

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

[**Enumeration**](enum.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lange**](long.md)
</dt> </dl>

 

 




