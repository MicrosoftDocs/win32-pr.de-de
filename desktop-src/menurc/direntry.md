---
title: DIRENTRY-Struktur
description: Enthält eine eindeutige Ordnungszahl, die eine einzelne Schriftart in der Ressourcengruppe der Schriftart identifiziert. Die hier bereitgestellte Strukturdefinition ist nur zur Erklärung vorgesehen. sie ist in einer Standardheaderdatei nicht vorhanden.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- DIRENTRY-Strukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 281ede8b2f87e73bf0600d985abd3194a83e8e8f186fa8f780f18f80985e0f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602110"
---
# <a name="direntry-structure"></a>DIRENTRY-Struktur

Enthält eine eindeutige Ordnungszahl, die eine einzelne Schriftart in der Ressourcengruppe der Schriftart identifiziert. Die hier bereitgestellte Strukturdefinition ist nur zur Erklärung vorgesehen. sie ist in einer Standardheaderdatei nicht vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**fontOrdinal**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Ein eindeutiger Ordinalbezeichner für eine einzelne Schriftart in einer Schriftartressourcengruppe.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**FONTDIRENTRY-Struktur**](fontdirentry.md) für die angegebene Schriftart folgt direkt der **DIRENTRY-Struktur** für diese Schriftart.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

 





