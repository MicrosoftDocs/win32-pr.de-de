---
title: POPUPMENUITEM-Struktur
description: Enthält Informationen zu den Menüelementen in einer Menüressource, die ein Menü oder ein Untermenü öffnen. Die hier bereitgestellte Strukturdefinition ist nur zur Erklärung vorgesehen. sie ist in einer Standardheaderdatei nicht vorhanden.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- POPUPMENUITEM-Strukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62d769e9756f0d15e7377a79f9aa94802a469746807e3a32b5ba329f76484b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011700"
---
# <a name="popupmenuitem-structure"></a>POPUPMENUITEM-Struktur

Enthält Informationen zu den Menüelementen in einer Menüressource, die ein Menü oder ein Untermenü öffnen. Die hier bereitgestellte Strukturdefinition ist nur zur Erklärung vorgesehen. sie ist in einer Standardheaderdatei nicht vorhanden.

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

Beschreibt das Menüelement. Einige der Werte, die dieses Member haben kann, enthalten die werte, die in der folgenden Liste angezeigt werden.

Zusätzlich zu den angezeigten Werten kann dieser Member auch eine Kombination der Typwerte sein, die mit dem **fType-Member** der [**MENUITEMINFO-Struktur aufgelistet**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) sind. Die Typwerte beginnen mit \_ MFT. Um diese vordefinierten \_ \* MFT-Typwerte zu verwenden, schließen Sie die folgende Anweisung in ihre RC-Datei ein:

`#include "winuser.h"`



| Wert                                                                                                                                                                                                    | Bedeutung                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_ END**</dt> <dt>0x80</dt> </dl>       | Das Menüelement ist das letzte im Menü. das Flag wird intern vom System verwendet. <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x01</dt> </dl> | Das Menüelement öffnet ein Menü oder ein Untermenü. das Flag wird intern vom System verwendet. <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Beschreibt das Menüelement. Dieser Member kann eine Kombination der Zustandswerte sein, die mit dem **dwState-Element** der [**MENUITEMINFO-Struktur aufgelistet**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) sind. Bei den Zustandswerten handelt es sich um die Werte, die mit MFS \_ beginnen. Um diese vordefinierten MFS-Zustandswerte \_ \* zu verwenden, schließen Sie die folgende Anweisung in ihre RC-Datei ein:

`#include "winuser.h"`

</dd> <dt>

**id**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein numerischer Ausdruck, der das Menüelement identifiziert, das in der [**WM \_ COMMAND-Meldung übergeben**](wm-command.md) wird.

</dd> <dt>

**Resinfo**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Ein Satz von Bitflags, die den Typ des Menüelements angeben. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**BESEN \_ END**</dt> <dt>0x80</dt> </dl>       | Das Menüelement ist das letzte in diesem Untermenü oder dieser Menüressource. dieses Flag wird intern vom System verwendet.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**BESEN \_ POPUP**</dt> <dt>0x01</dt> </dl> | Das Menüelement öffnet ein Menü oder ein Untermenü. das Flag wird intern vom System verwendet.<br/>                     |



 

</dd> <dt>

**menuText**
</dt> <dd>

Typ: **szOrOrd**

</dd> <dd>

Eine mit NULL beendete Unicode-Zeichenfolge, die den Text für dieses Menüelement enthält. Es gibt keine feste Beschränkung für die Größe dieser Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Es gibt eine **POPUPMENUITEM-Struktur** für jedes Menüelement, das ein Menü oder ein Untermenü öffnet. Identifizieren Sie diese Art von  Menüelement, indem Sie das Typelement auf **MF \_ POPUP** und das **POPUP-Bit im \_** **resInfo-Element** auf 0x0001. In diesem Fall sind die endgültigen Daten, die in die [**RESSOURCE RT \_ MENU**](/windows/desktop/menurc/resource-types) für das Menü oder Untermenü geschrieben werden, die [**MENUHELPID-Struktur.**](menuhelpid.md) **MENUHELPID enthält** einen numerischen Ausdruck, der das Menü während der [**WM \_ HELP-Verarbeitung**](../shell/wm-help.md) identifiziert.

Darüber hinaus folgt auf jede **POPUPMENUITEM-Struktur,** für die **das POPUP \_ POPUP-Bit** im **resInfo-Element** festgelegt ist, eine [**MENUHELPID-Struktur**](menuhelpid.md) sowie eine zusätzliche Anzahl von **POPUPMENUITEM-Strukturen,** eine für jedes Menüelement in diesem Untermenü. Für die **letzte POPUPMENUITEM-Struktur** im Untermenü wird im resInfo-Member **das BIT DES \_ ENDES** **festgelegt.** Um das Ende der Ressource zu finden, suchen Sie nach einem passenden BEENDEN für jedes **\_ POPUP-Popup** und nach einem zusätzlichen **DANN \_ END,** das mit dem äußersten Satz von Menüelementen übereinstimmen. **\_**

Geben Sie das letzte Menüelement an, indem Sie **das Typelement** auf **MF \_ END festlegen.** Da Sie Untermenüs schachteln können, kann es mehrere Ebenen von **MF \_ END geben.** In diesen Fällen sind die Menüelemente sequenziell.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**MENUHELPID**](menuhelpid.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

