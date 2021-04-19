---
title: declare_guid-Schlüsselwort
description: Das DECLARE \_ GUID-Schlüsselwort weist die Mitte an, eine GUID-Variable in der generierten Header Datei auszugeben.
keywords:
- declare_guid-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106355096"
---
# <a name="declare_guid-keyword"></a>DECLARE \_ GUID-Schlüsselwort

Das **Declare \_ GUID** -Schlüsselwort weist die Mitte an, eine GUID-Variable in der generierten Header Datei auszugeben.

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Variablenname* 
</dt> <dd>

Gibt einen Variablennamen für den Bezeichner in der generierten Header Datei an.

</dd> <dt>

*guid*
</dt> <dd>

Gibt die [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) an, die auf den Variablennamen in der generierten Header Datei angewendet wird.

</dd> </dl>

## <a name="examples"></a>Beispiele

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a>Bemerkungen

`declare_guid` `cpp_quote` Die Verwendung von entspricht der Verwendung von, um einen Aufruf des `EXTERN_GUID` Makros zu generieren.

Im obigen Beispiel wird die folgende Ausgabe angezeigt:

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

Die- `declare_guid` Anweisung wird als praktische Hilfe bereitgestellt. Es hat den Vorteil, dass die gleiche GUID-Syntax wie das- [ `uuid` Attribut](uuid.md)verwendet wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**cpp_quote**](cpp-quote.md)
</dt> <dt>

[**uuid-Attribut**](uuid.md)
</dt> <dt>

[**GUID-Struktur**](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
