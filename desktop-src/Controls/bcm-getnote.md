---
title: BCM_GETNOTE Meldung (kommstrg. h)
description: Ruft den Text des Notiz Texts ab, der einer Befehls Link Schaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das Schaltfläche \_ GetNote-Makro verwenden.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- Windows-Steuerelemente für BCM_GETNOTE Meldung
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
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345297"
---
# <a name="bcm_getnote-message"></a>BCM \_ GetNote-Meldung

Ruft den Text des Notiz Texts ab, der einer Befehls Link Schaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das [**Schaltfläche \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in, out\]
</dt> <dd>

Ein **DWORD** , das die Größe des Puffers angibt, auf den *LPARAM* zeigt, in Zeichen.

</dd> <dt>

*LPARAM* \[ vorgenommen\]
</dt> <dd>

Der Zeichen folgen Puffer, der den Text empfangen soll. Der Puffer muss groß genug sein, um das abschließende Null-Zeichen aufnehmen zu können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die **BCM \_ GetNote** -Nachricht funktioniert nur mit Schaltflächen, die den Schaltflächen Stil " [**SB \_ CommandLink**](button-styles.md) " oder " [**b" \_ defcommandlink**](button-styles.md) aufweisen.

" [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " enthält Folgendes:

-   Ein Fehler wird \_ nicht \_ unterstützt, wenn die Schaltfläche nicht den Typ "bin [**\_ defcommandlink**](button-styles.md) " oder " [**SB \_ CommandLink**](button-styles.md) " hat.
-   Fehler \_ unzureichender \_ Puffer, wenn der *LPARAM* -Puffer zu klein ist. Der *wParam* -Parameter enthält die erforderliche Puffergröße in Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

