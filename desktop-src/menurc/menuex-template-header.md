---
title: MENUEX_TEMPLATE_HEADER Struktur
description: Definiert den Header für eine erweiterte Menüvorlage. Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341783"
---
# <a name="menuex_template_header-structure"></a>Menuex- \_ Vorlagen \_ Header Struktur

Definiert den Header für eine erweiterte Menüvorlage. Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

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

**wversion**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Versionsnummer der Vorlage. Dieser Member muss für erweiterte Menü Vorlagen 1 sein.

</dd> <dt>

**woffset**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Offset zur ersten [**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md) Struktur, relativ zum Ende dieses Strukturmembers. Wenn die erste Element Definition direkt auf den **dwhelpid** -Member folgt, sollte dieser Member 4 sein.

</dd> <dt>

**dwhelpid**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Hilfe Bezeichner der Menüleiste.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine erweiterte Menüvorlage besteht aus einer **menuex- \_ Vorlagen \_ Header** Struktur, gefolgt von einer oder mehreren zusammenhängenden [**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md) Strukturen. Die **menuex- \_ Vorlagen \_ Element** Strukturen, die eine Variable Länge haben, werden an den **DWORD** -Grenzen ausgerichtet. Verwenden Sie die [**loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) -Funktion, um ein Menü aus einer erweiterten Menüvorlage im Arbeitsspeicher zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

 





