---
title: BCM_GETNOTE Nachricht (Commctrl.h)
description: Ruft den Text der Notiz ab, die einer Befehlslinkschaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das \_ Schaltflächenmakro GetNote verwenden.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b552f79e1d6c7bda2808b99701ff11e45deb169232b8bb52c4ecf231cdcbfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921700"
---
# <a name="bcm_getnote-message"></a>BCM \_ GETNOTE-Nachricht

Ruft den Text der Notiz ab, die einer Befehlslinkschaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das [**\_ Schaltflächenmakro GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in, out\]
</dt> <dd>

Ein **DWORD,** das die Größe des Puffers angibt, auf den *von lParam* in Zeichen gezeigt wird.

</dd> <dt>

*lParam* \[ out\]
</dt> <dd>

Der Zeichenfolgenpuffer, der den Text empfangen soll. Der Puffer muss groß genug sein, um das abschließende NULL-Zeichen aufzunehmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, wird **TRUE** zurückgegeben. Andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die **BCM \_ GETNOTE-Nachricht** funktioniert nur mit Schaltflächen, die den [**BS \_ COMMANDLINK-**](button-styles.md) oder [**BS \_ DEFCOMMANDLINK-Schaltflächenstil**](button-styles.md) aufweisen.

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) enthält Folgendes:

-   FEHLER \_ NICHT \_ UNTERSTÜTZT, wenn die Schaltfläche nicht den Stil [**"BS \_ DEFCOMMANDLINK"**](button-styles.md) oder [**"BS \_ COMMANDLINK"**](button-styles.md) aufweist.
-   ERROR \_ INSUFFICIENT \_ BUFFER, wenn der *lParam-Puffer* zu klein ist. Der *wParam-Parameter* enthält die erforderliche Puffergröße in Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

