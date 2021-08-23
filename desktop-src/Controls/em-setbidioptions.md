---
title: EM_SETBIDIOPTIONS (Richedit.h)
description: Die MELDUNG EM \_ SETBIDIOPTIONS legt den aktuellen Status der bidirektionalen Optionen im Rich-Edit-Steuerelement fest.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS von Windows Steuerelementen
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f22d03e1738fc688d34f55a6823f7ae95c2dfc41724e827cd31a184ac7cbdfce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545020"
---
# <a name="em_setbidioptions-message"></a>EM \_ SETBIDIOPTIONS-Meldung

Die **MELDUNG EM \_ SETBIDIOPTIONS** legt den aktuellen Status der bidirektionalen Optionen im Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**BIDIOPTIONS-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) die angibt, wie der Status der bidirektionalen Optionen im Rich-Edit-Steuerelement festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Rich-Edit-Steuerelement muss sich im Nur-Text-Modus befinden, **oder EM \_ SETBIDIOPTIONS** kann nichts tun.

In Nur-Text-Steuerelementen bestimmt **EM \_ SETBIDIOPTIONS** automatisch die Absatzrichtung und/oder -ausrichtung basierend auf den Kontextregeln. Diese Regeln geben an, dass die Richtung und/oder Ausrichtung vom ersten starken Zeichen im Steuerelement abgeleitet wird. Ein starkes Zeichen ist ein Zeichen, aus dem die Textrichtung bestimmt werden kann (siehe Unicode Standard Version 2.0). Die Absatzrichtung und/oder -ausrichtung wird auf das Standardformat angewendet.

**EM \_ SETBIDIOPTIONS** schaltet das Standardformat des Absatzes nur dann in RTL (rechts nach links) um, wenn ein RTL-Zeichen gefunden wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ GETBIDIOPTIONS**](em-getbidioptions.md)
</dt> </dl>

 

 





