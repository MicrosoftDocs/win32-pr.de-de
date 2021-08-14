---
title: UI_ALL_COMMANDS (Uiribbon.h)
description: Gibt eine Konstante an, die die Auflistung von Befehlen identifiziert, die in der Markupressourcendatei deklariert sind.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24767f2d3839b94ee83c6a9a527b2e80dcf8c1960e877f65a0e7e96fff4e3ec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705959"
---
# <a name="ui_all_commands"></a>BEFEHLE \_ DER BENUTZEROBERFLÄCHE "ALLE" \_

Gibt eine Konstante an, die die Auflistung von Befehlen identifiziert, die in der Markupressourcendatei deklariert sind.

## <a name="remarks"></a>Hinweise

**Benutzeroberfläche \_ ALL \_ COMMANDS** ist nützlich, wenn sie für alle Befehle auf ähnliche Eigenschaften zugreifen müssen. Beispielsweise können **UI \_ ALL \_ COMMANDS** an [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) übergeben werden, um alle Menübandbefehle ungültig zu machen und zu aktualisieren, indem die Hostanwendung nach neuen Eigenschaftswerten abfragt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Windows Vista mit SP2 und Plattformupdate nur für Windows \[ Vista-Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate nur für Windows Server 2008-Desktop-Apps \[\]<br/> |
| Header<br/>                   | <dl> <dt>Uiribbon.h</dt> </dl>                                             |
| Idl<br/>                      | <dl> <dt>Uiribbon.idl</dt> </dl>                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Konstanten und Enumerationen](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

