---
title: EM_SETCUEBANNER Meldung (kommstrg. h)
description: Legt den Text Hinweis oder Tip fest, der vom Bearbeitungs Steuerelement angezeigt wird, um den Benutzer zur Eingabe von Informationen aufzufordern.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Windows-Steuerelemente für EM_SETCUEBANNER Meldung
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478576"
---
# <a name="em_setcuebanner-message"></a>EM \_ setcuebanner-Meldung

Legt den Text Hinweis oder Tip fest, der vom Bearbeitungs Steuerelement angezeigt wird, um den Benutzer zur Eingabe von Informationen aufzufordern.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

**True** , wenn das Hinweis Banner auch dann angezeigt werden soll, wenn das Bearbeitungs Steuerelement den Fokus besitzt. andernfalls **false**. **False** ist das Standardverhalten, das das Hinweis Banner verschwindet, wenn der Benutzer auf das-Steuerelement klickt.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Text enthält, der als Text Hinweis angezeigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ein Bearbeitungs Steuerelement, das verwendet wird, um eine Suche zu starten, kann in grauem Text als Text Hinweis den Text "hier suchen hier eingeben" anzeigen. Wenn der Benutzer auf den Text klickt, geht der Text Weg, und der Benutzer kann eingeben.

Sie können kein Hinweis Banner in einem mehrzeiligen Bearbeitungs Steuerelement oder in einem Rich-Edit-Steuerelement festlegen.

> [!Note]  
> Um diese API zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bearbeiten von \_ setcuebannertext**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





