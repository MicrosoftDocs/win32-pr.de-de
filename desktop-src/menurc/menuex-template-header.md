---
title: MENUEX_TEMPLATE_HEADER-Struktur
description: Definiert den Header für eine erweiterte Menüvorlage. Diese Strukturdefinition wird nur zur Erklärung verwendet. sie ist in einer Standardheaderdatei nicht vorhanden.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER Strukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31e52661e04a036cf7a49791be96af002b801af0e0ed1c4b6ad3ddebf971c2c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226120"
---
# <a name="menuex_template_header-structure"></a>MENUEX \_ TEMPLATE \_ HEADER structure

Definiert den Header für eine erweiterte Menüvorlage. Diese Strukturdefinition wird nur zur Erklärung verwendet. sie ist in einer Standardheaderdatei nicht vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**wVersion**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Versionsnummer der Vorlage. Dieser Member muss für erweiterte Menüvorlagen 1 sein.

</dd> <dt>

**wOffset**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Der Offset zur ersten [**MENUEX \_ TEMPLATE \_ ITEM-Struktur**](menuex-template-item.md) relativ zum Ende dieses Strukturelements. Wenn die erste Elementdefinition unmittelbar auf das **dwHelpId-Element** folgt, sollte dieser Member 4 sein.

</dd> <dt>

**dwHelpId**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Hilfebezeichner der Menüleiste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine erweiterte Menüvorlage besteht aus einer **MENUEX \_ TEMPLATE \_ HEADER-Struktur,** gefolgt von einer oder mehreren zusammenhängenden [**MENUEX TEMPLATE \_ \_ ITEM-Strukturen.**](menuex-template-item.md) Die **MENUEX \_ TEMPLATE \_ ITEM-Strukturen,** die eine variable Länge haben, werden an **DWORD-Grenzen** ausgerichtet. Um ein Menü aus einer erweiterten Menüvorlage im Arbeitsspeicher zu erstellen, verwenden Sie die [**LoadMenuIndirect-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**\_MENUEX-VORLAGENELEMENT \_**](menuex-template-item.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

 





