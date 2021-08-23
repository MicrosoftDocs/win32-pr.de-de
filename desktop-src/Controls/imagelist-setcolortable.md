---
title: ImageList_SetColorTable-Funktion
description: Legt die Farbtabelle für eine Bildliste fest.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- ImageList_SetColorTable-Windows Steuerelemente
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de1acd8f14d9993bc75ea69b910b365e29156a6386933ccb95251a916c37244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412238"
---
# <a name="imagelist_setcolortable-function"></a>Funktion \_ "ImageList SetColorTable"

Legt die Farbtabelle für eine Bildliste fest.

## <a name="syntax"></a>Syntax


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*himl* \[ In\]
</dt> <dd>

Typ: **HIMAGELIST**

Ein Handle für die Bildliste.

</dd> <dt>

*Start* \[ In\]
</dt> <dd>

Typ: **int**

Ein nullbasierter Farbtabellenindex, der den ersten festgelegten Farbtabelleneintrag angibt.

</dd> <dt>

*len* \[ In\]
</dt> <dd>

Typ: **int**

Die Anzahl der festgelegten Farbtabelleneinträge.

</dd> <dt>

*prgb* \[ In\]
</dt> <dd>

Typ: **[ **RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\***

Ein Zeiger auf ein Array von *len* [**RGBQUAD-Strukturen,**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) die neue Farbinformationen für die Farbtabelle des DIB enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn die Funktion erfolgreich ist, gibt sie die Anzahl von Farbtabelleneinträgen zurück, die von der Funktion festgelegt wurden. Wenn die Funktion fehlschlägt, ist der Rückgabewert kleiner oder gleich 0 (null).

## <a name="remarks"></a>Hinweise

Nur Bildlisten, die mit dem [**ILC \_ COLOR4- oder**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) [**ILC \_ COLOR8-Flag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) erstellt wurden, verfügen über Farbtabellen. Die Farbtabelle einer solchen Bildliste wird in der Regel automatisch festgelegt, indem die Farbtabelle des ersten Bilds kopiert wird, das der Liste hinzugefügt wurde (z. B. über die [**Funktion ImageList \_ Add),**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) wenn es sich bei dem Bild um ein DIB handelt. Wenn das erste Der Bildliste hinzugefügte Bild kein DIB ist, wird die Farbtabelle der Halbtonpalette für **ILC \_ COLOR8-Bildlisten** und die VGA-Farbtabelle für **ILC \_ COLOR4 verwendet.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 3.51 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Farbtabelle](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

