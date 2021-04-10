---
title: readonly-Attribut
description: Das Attribut \ schreibgeschützt \ untersagt die Zuweisung zu einer Variablen.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- Schreib geschütztes Attribut, Mittel l
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948692"
---
# <a name="readonly-attribute"></a>readonly-Attribut

Das **Schreib \[ geschützte Attribut verhindert die Zuweisung zu einer Variablen. \]**

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optionale Attribute* 
</dt> <dd>

NULL oder mehr mittlere Attribute.

</dd> <dt>

*Datentyp* 
</dt> <dd>

Der Typ der Daten, die im *Bezeichner* enthalten sind.

</dd> <dt>

*identifier* 
</dt> <dd>

Ein Name, mit dem die Software auf den Daten Speicherort verweisen kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **Schreib \[ geschützte Attribut verhindert die Zuweisung zu einer Variablen. \]** "schreibgeschützt" wird nur auf Parameter Ebene, nicht auf Methoden Ebene unterstützt. **\[ \]**

### <a name="flags"></a>Flags

varflag \_ freadonly

## <a name="examples"></a>Beispiele

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 