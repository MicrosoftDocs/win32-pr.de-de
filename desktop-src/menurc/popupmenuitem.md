---
title: Popupmenuitem-Struktur
description: Enthält Informationen zu den Menü Elementen in einer Menü Ressource, mit der ein Menü oder ein Untermenü geöffnet wird. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Popupmenuitem-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949552"
---
# <a name="popupmenuitem-structure"></a>Popupmenuitem-Struktur

Enthält Informationen zu den Menü Elementen in einer Menü Ressource, mit der ein Menü oder ein Untermenü geöffnet wird. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a>Member

<dl> <dt>

**type**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Beschreibt das Menü Element. Einige der Werte, die dieser Member enthalten kann, sind die in der folgenden Liste aufgeführten Werte.

Zusätzlich zu den angezeigten Werten kann dieser Member auch eine Kombination der Typwerte sein, die mit dem **ftype** -Member der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur aufgelistet sind. Die Typwerte sind diejenigen, die mit MFT beginnen \_ . Um diese vordefinierten MFT- \_ \* Typwerte zu verwenden, fügen Sie die folgende Anweisung in die RC-Datei ein:

`#include "winuser.h"`



| Wert                                                                                                                                                                                                    | Bedeutung                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_ Ende**</dt> <dt>0x80</dt> </dl>       | Das Menü Element ist das letzte im Menü. das-Flag wird intern vom System verwendet. <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ Popup**</dt> - <dt>0x01</dt> </dl> | Das Menü Element öffnet ein Menü oder ein Untermenü. das-Flag wird intern vom System verwendet. <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Beschreibt das Menü Element. Dieser Member kann eine Kombination der Zustands Werte sein, die mit dem **dwstate** -Member der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur aufgelistet werden. Die Statuswerte sind diejenigen, die mit MFS beginnen \_ . Um diese vordefinierten MFS- \_ \* Zustands Werte zu verwenden, fügen Sie die folgende Anweisung in die RC-Datei ein:

`#include "winuser.h"`

</dd> <dt>

**id**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein numerischer Ausdruck, der das Menü Element identifiziert, das in der [**WM- \_ Befehls**](wm-command.md) Meldung ausgegeben wird.

</dd> <dt>

**resInfo**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Ein Satz von Bitflags, die den Typ des Menü Elements angeben. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ Ende**</dt> <dt>0x80</dt> </dl>       | Das Menü Element ist das letzte in diesem Untermenü oder in der Menü Ressource. Dieses Flag wird intern vom System verwendet.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ Popup**</dt> - <dt>0x01</dt> </dl> | Das Menü Element öffnet ein Menü oder ein Untermenü. das-Flag wird intern vom System verwendet.<br/>                     |



 

</dd> <dt>

**MenuText**
</dt> <dd>

Typ: **szorord**

</dd> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die den Text für dieses Menü Element enthält. Es gibt keine Beschränkung für die Größe dieser Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es gibt eine **popupmenuitem** -Struktur für jedes Menü Element, das ein Menü oder ein Untermenü öffnet. Identifizieren Sie diesen Typ von Menü Element durch Festlegen des **Typmembers** auf das **MF- \_ Popup** und durch Festlegen des **MFR- \_ Popup** Bits im **ResInfo** -Member auf 0x0001. In diesem Fall handelt es sich bei den letzten Daten, die in die [**RT- \_ Menü**](/windows/desktop/menurc/resource-types) Ressource für das Menü oder Untermenü geschrieben werden, um die [**menuhelpid**](menuhelpid.md) -Struktur. **Menuhelpid** enthält einen numerischen Ausdruck, der das Menü während der [**WM- \_ Hilfe**](../shell/wm-help.md) Verarbeitung identifiziert.

Außerdem folgt jede **popupmenuitem** -Struktur, der das **MFR- \_ Popup** -Bit im **ResInfo** -Member festgelegt ist, eine [**menuhelpid**](menuhelpid.md) -Struktur plus eine zusätzliche Anzahl von **popupmenuitem** -Strukturen, eine für jedes Menü Element in diesem Untermenü. In der letzten **popupmenuitem** -Struktur im Untermenü wird das **MFR- \_ Endbit** im **ResInfo** -Member festgelegt. Um das Ende der Ressource zu ermitteln, suchen Sie nach einem passenden **MFR- \_ Ende** für jedes **MFR- \_ Popup** plus ein zusätzliches **MFR- \_ Ende** , das mit dem äußersten Satz von Menü Elementen übereinstimmt.

Geben Sie das letzte Menü Element an, indem Sie das **Typelement** auf das **\_ Ende von MF** festlegen. Da Untermenüs geschachtelt werden können, können mehrere Ebenen von **MF \_ enden**. In diesen Fällen sind die Menü Elemente sequenziell.

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

[**Menuhelpid**](menuhelpid.md)
</dt> <dt>

[**Menuiteminfo zuordnet**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**Normalmenuitem**](normalmenuitem.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

