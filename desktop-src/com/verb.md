---
title: Verb
description: Gibt die Verben an, die für eine Anwendung registriert werden sollen.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Verbregistrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef70e4a3f748b1f00a364f25755d60a3adfd9091cd2df3032e347f53f55519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047718"
---
# <a name="verb"></a>Verb

Gibt die Verben an, die für eine Anwendung registriert werden sollen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a>Hinweise

Jedes Verb ist ein **REG \_ SZ-Wert** der Form "*Name*, *\_ Menüflag*, *\_ Verbflag*". Verben müssen fortlaufend nummeriert werden.

Der *Name* beschreibt, wie das Verb durch einen [**AppendMenu-Funktionsaufruf**](/windows/win32/api/winuser/nf-winuser-appendmenua) angefügt wird. Beispiel: "&Play".

Der *\_ Menüflagwert* gibt an, wie das Verb im Menü angezeigt werden soll. Alle von [**AppendMenu unterstützten**](/windows/win32/api/winuser/nf-winuser-appendmenua) Flags werden unterstützt, mit Ausnahme von MF \_ BITMAP, MF \_ OWNERDRAW und MF \_ POPUP.

Der *\_ Verbflagwert* beschreibt Attribute der Verben. Verwenden Sie einen der Werte aus [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)oder 0.

Weitere Informationen finden Sie unter [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D oVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)und [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 