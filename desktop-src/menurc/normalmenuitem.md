---
title: NORMALMENUITEM-Struktur
description: Enthält Informationen zu jedem Element in einer Menüressource, die kein Menü oder Untermenü öffnet. Die hier bereitgestellte Strukturdefinition dient nur zur Erklärung. sie ist in keiner Standardheaderdatei vorhanden.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- NORMALMENUITEM-StrukturMenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f47fef5e1481d56671cd525061f1a5fcf88481213671bac45c923cfbae0ebbd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733690"
---
# <a name="normalmenuitem-structure"></a>NORMALMENUITEM-Struktur

Enthält Informationen zu jedem Element in einer Menüressource, die kein Menü oder Untermenü öffnet. Die hier bereitgestellte Strukturdefinition dient nur zur Erklärung. sie ist in keiner Standardheaderdatei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a>Member

<dl> <dt>

**Resinfo**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Der Typ des Menüelements. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**WIEDERERZ \_ END**</dt> <dt>0x80</dt> </dl>       | Das Menüelement ist das letzte in dieser Untermenü- oder Menüressource. Dieses Flag wird intern vom System verwendet.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**WIEDERERZ \_ POPUP-0x01**</dt> <dt></dt> </dl> | Das Menüelement öffnet ein Menü oder ein Untermenü. Das Flag wird intern vom System verwendet. <br/>                    |



 

</dd> <dt>

**menuText**
</dt> <dd>

Typ: **szOrOrd**

</dd> <dd>

Eine auf NULL endende Unicode-Zeichenfolge, die den Text für dieses Menüelement enthält. Es gibt keinen festen Grenzwert für die Größe dieser Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Es gibt eine **NORMALMENUITEM-Struktur** für jedes Menüelement, das kein Menü oder Untermenü öffnet. Geben Sie das letzte Menüelement in einem Menü an, indem Sie den **resInfo-Member** auf **DIE END-End-Einstellung \_** festlegen.

Ein Menütrennzeichen ist ein spezieller Typ von Menüelement, das inaktiv ist, aber als Trennleiste zwischen zwei aktiven Menüelementen angezeigt wird. Geben Sie ein Menütrennzeichen an, indem Sie das **menuText-Element** leer lassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

 





