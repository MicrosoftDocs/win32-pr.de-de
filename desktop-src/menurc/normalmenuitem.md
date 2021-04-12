---
title: Normalmenuitem-Struktur
description: Enthält Informationen zu jedem Element in einer Menü Ressource, die kein Menü oder Untermenü öffnet. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Normmenuitem-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340517"
---
# <a name="normalmenuitem-structure"></a>Normalmenuitem-Struktur

Enthält Informationen zu jedem Element in einer Menü Ressource, die kein Menü oder Untermenü öffnet. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a>Member

<dl> <dt>

**resInfo**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Typ des Menü Elements. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ Ende**</dt> <dt>0x80</dt> </dl>       | Das Menü Element ist das letzte in diesem Untermenü oder in der Menü Ressource. Dieses Flag wird intern vom System verwendet.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ Popup**</dt> - <dt>0x01</dt> </dl> | Das Menü Element öffnet ein Menü oder ein Untermenü. das-Flag wird intern vom System verwendet. <br/>                    |



 

</dd> <dt>

**MenuText**
</dt> <dd>

Typ: **szorord**

</dd> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die den Text für dieses Menü Element enthält. Es gibt keine Beschränkung für die Größe dieser Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es gibt eine **Normal MenuItem** -Struktur für jedes Menü Element, das kein Menü oder Untermenü öffnet. Geben Sie das letzte Menü Element in einem Menü an, indem Sie das **ResInfo** -Element auf **MFR- \_ Ende** festlegen.

Ein Menü Trennzeichen ist ein spezieller Typ von Menü Element, das inaktiv ist, aber als Trennleiste zwischen zwei aktiven Menü Elementen angezeigt wird. Geben Sie ein Menü Trennzeichen an, indem Sie den **MenuText** -Member leer gelassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Menuheader**](menuheader.md)
</dt> <dt>

[**Menuiteminfo zuordnet**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**Popupmenuitem**](popupmenuitem.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

 





