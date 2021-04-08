---
title: ImageList_SetColorTable-Funktion
description: Legt die Farbtabelle für eine Bildliste fest.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- Windows-Steuerelemente ImageList_SetColorTable-Funktion
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
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957268"
---
# <a name="imagelist_setcolortable-function"></a>ImageList- \_ setcolortable-Funktion

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

*HIML* \[ in\]
</dt> <dd>

Typ: **HIMAGELIST**

Ein Handle für die Bildliste.

</dd> <dt>

*starten* \[ Sie in\]
</dt> <dd>

Typ: **int**

Ein NULL basierter Index der Farbtabelle, der den ersten festzulegenden Farb Tabelleneintrag angibt.

</dd> <dt>

*len* \[ in\]
</dt> <dd>

Typ: **int**

Die Anzahl der festzulegenden farbtabelleneinträge.

</dd> <dt>

*prgb* \[ in\]
</dt> <dd>

Typ: **[**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _

Ein Zeiger auf ein Array von _Len * [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Strukturen, das neue Farbinformationen für die Farbtabelle der DIB enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie die Anzahl der farbtabelleneinträge zurück, die von der Funktion festgelegt werden. Wenn die Funktion fehlschlägt, ist der Rückgabewert kleiner oder gleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Nur Bildlisten, die mit dem [**ILC- \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) -oder [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) -Flag erstellt wurden, haben Farbtabellen. Die Farbtabelle einer solchen Bildliste wird in der Regel automatisch festgelegt, indem die Farbtabelle des ersten Bilds kopiert wird, das der Liste hinzugefügt wird (z. b. über die Funktion " [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) "), wenn dieses Bild ein DIB ist. Wenn das erste der Bildliste hinzugefügte Bild kein DIB ist, dann wird die Farbtabelle der Halbton-Palette für **ILC- \_ COLOR8** -Bildlisten und die VGA-Farbtabelle für **ILC- \_ COLOR4** verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 3,51 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Farbtabelle](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

