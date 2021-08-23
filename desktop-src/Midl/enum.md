---
title: enum-Attribut
description: Die Schlüsselwortenumerum identifiziert einen aufzählten Typ.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- enum-Attribut MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1519e6208e8bccae0288d6e0b31d7897faba4e1c9c7add8987f5dd493f4f5f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384489"
---
# <a name="enum-attribute"></a>enum-Attribut

Die **Schlüsselwortenumerum** identifiziert einen aufzählten Typ.

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Etikett* 
</dt> <dd>

Gibt ein optionales Tag für den aufzählten Typ an.

</dd> <dt>

*identifier* 
</dt> <dd>

Gibt die bestimmte Enumeration an.

</dd> <dt>

*integer-value* 
</dt> <dd>

Gibt einen konstanten ganzzahligen Wert an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**Enum-Typen** können als Typspezifizierer in Typedef-Deklarationen, allgemeinen Deklarationen und Funktionsdeklaratoren (entweder als Funktions-Rückgabetyp oder als Parametertypspezifizierer) angezeigt werden. [](typedef.md) Informationen zum Kontext, in dem Typspezifizierer angezeigt werden, finden Sie unter [Interface Definition (IDL)-Datei.](interface-definition-idl-file.md)

Im Standardmodus des MIDL-Compilers können Sie Enumeratoren ganzzahlige Werte zuweisen. (Dieses Feature ist nicht verfügbar, wenn Sie mit dem [**Schalter /osf kompilieren.)**](-osf.md) Wie bei C-Enumeratoren müssen Enumeratornamen eindeutig sein, aber die Enumeratorwerte müssen nicht sein.

Wenn keine Zuweisungsoperatoren bereitgestellt werden, werden Bezeichner aufeinanderfolgenden ganzen Zahlen von links nach rechts zugeordnet, beginnend mit null. Wenn Zuweisungsoperatoren bereitgestellt werden, beginnen zugewiesene Werte mit dem zuletzt zugewiesenen Wert.

Die maximale Anzahl von Bezeichnern beträgt 65.535.

Objekte vom Typ **enum** sind [**int-Typen,**](int.md) und ihre Größe ist systemabhängig. Standardmäßig werden Objekte von **Enum-Typen** als 16-Bit-Objekte vom Typ [**unsigned**](unsigned.md) [**short**](short.md) behandelt, wenn sie über ein Netzwerk übertragen werden. Werte außerhalb des Bereichs von 0 bis 32.767 verursachen die Laufzeitausnahme RPC \_ X \_ ENUM \_ VALUE OUT OF \_ \_ \_ RANGE. Um Objekte als 32-Bit-Entitäten zu übertragen, wenden Sie das **\[** [**\_ v1-enum-Attribut**](v1-enum.md) auf die **\]** **enum** typedef an.

## <a name="examples"></a>Beispiele

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**\_v1-Aufzählen**](v1-enum.md)
</dt> </dl>

 

 




