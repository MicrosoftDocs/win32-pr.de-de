---
title: readonly-Attribut
description: Das \readonly\-Attribut verhindert die Zuweisung zu einer Variablen.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- readonly-Attribut MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d0d534efe8df1f4d05cd0b536a78094f903870d896114ee8b614511e067025b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013678"
---
# <a name="readonly-attribute"></a>readonly-Attribut

Das **\[ schreibgeschützte Attribut \]** verhindert die Zuweisung zu einer Variablen.

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optional-attributes* 
</dt> <dd>

Null oder mehr MIDL-Attribute.

</dd> <dt>

*-Datentyp* 
</dt> <dd>

Der Typ der im Bezeichner enthaltenen *Daten.*

</dd> <dt>

*identifier* 
</dt> <dd>

Ein Name, mit dem die Software auf den Speicherort der Daten verweisen kann.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ schreibgeschützte Attribut \]** verhindert die Zuweisung zu einer Variablen. **\[ readonly \]** wird nur auf Parameterebene unterstützt, nicht auf Methodenebene.

### <a name="flags"></a>Flags

VARFLAG \_ FREADONLY

## <a name="examples"></a>Beispiele

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 