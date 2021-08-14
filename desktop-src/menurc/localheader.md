---
title: LOCALHEADER-Struktur
description: Enthält die x- und y-Koordinaten eines Hotspots, die dem cursor zugeordnet sind, der durch eine RESDIR-Struktur identifiziert wird. Die hier bereitgestellte Strukturdefinition dient nur zur Erklärung. sie ist in keiner Standardheaderdatei vorhanden.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- LOCALHEADER-StrukturMenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52ec46b802b847b73c99cc81939531d8f9ec1a6a2e0addb4c928d5610ac5b80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870318"
---
# <a name="localheader-structure"></a>LOCALHEADER-Struktur

Enthält die x- und y-Koordinaten eines Hotspots, die dem cursor zugeordnet sind, der durch eine [**RESDIR-Struktur**](resdir.md) identifiziert wird. Die hier bereitgestellte Strukturdefinition dient nur zur Erklärung. sie ist in keiner Standardheaderdatei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**xHotSpot**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die x-Koordinate des Cursor-Hotspots in Pixel.

</dd> <dt>

**yHotSpot**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die y-Koordinate des Cursor-Hotspots in Pixel.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **LOCALHEADER-Struktur** ist die erste In die [RT \_ CURSOR-Ressource](/windows/desktop/menurc/resource-types) geschriebene Daten, wenn eine [**RESDIR-Struktur**](resdir.md) Informationen zu einem Cursor enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CURSORDIR**](cursordir.md)
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

