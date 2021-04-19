---
title: Verb
description: Gibt die Verben an, die für eine Anwendung registriert werden sollen.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Verb Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339101"
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

## <a name="remarks"></a>Bemerkungen

Jedes Verb ist ein **reg \_ SZ** -Wert im Format "*Name*, *Menü \_* Kennzeichen, *Verb \_ Flag*". Verben müssen nacheinander nummeriert werden.

Der *Name* beschreibt, wie das Verb durch einen [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) -Funktions aufrufangefügt wird. Beispiel: "&Play".

Der Wert für das *\_ menüflag* gibt an, wie das Verb im Menü angezeigt werden soll. Alle Flags, die von [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) unterstützt werden, werden unterstützt, mit Ausnahme von MF- \_ Bitmap, MF \_ -Besitzer zeichnen und MF- \_ Popup.

Der *Verb \_ Flagwert* beschreibt die Attribute der Verben. Verwenden Sie einen der Werte aus [**oleverbatbinb**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)oder 0.

Weitere Informationen finden Sie unter [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)und [**IOleObject:: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**Oleverbatbinb**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 