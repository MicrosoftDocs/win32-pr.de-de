---
title: EM_SETBIDIOPTIONS Meldung (RichEdit. h)
description: Die \_ Meldung "gesetbidioptions" legt den aktuellen Status der bidirektionalen Optionen im Rich Edit-Steuerelement fest.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- Windows-Steuerelemente für EM_SETBIDIOPTIONS Meldung
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
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105591"
---
# <a name="em_setbidioptions-message"></a>EM \_ setbidioptions-Meldung

Die Meldung " **\_ gesetbidioptions** " legt den aktuellen Status der bidirektionalen Optionen im Rich Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) -Struktur, die angibt, wie der Zustand der bidirektionalen Optionen im Rich Edit-Steuerelement festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Rich Edit-Steuerelement muss sich im nur-Text-Modus befinden, oder **EM \_ setbidioptions** führt nichts aus.

Bei nur-Text-Steuerelementen bestimmt **EM \_ setbidioptions** automatisch die Absatz Richtung und/oder die Ausrichtung basierend auf den Kontextregeln. Diese Regeln geben an, dass die Richtung und/oder Ausrichtung vom ersten starken Zeichen im Steuerelement abgeleitet wird. Ein starkes Zeichen ist ein Zeichen, von dem die Textrichtung bestimmt werden kann (siehe Unicode-Standard Version 2,0). Die Absatz Richtung und/oder Ausrichtung wird auf das Standardformat angewendet.

**EM \_ Setbidioptions** schaltet nur das Standard Absatzformat zu RTL (von rechts nach links), wenn ein RTL-Zeichen gefunden wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ getbidioptions**](em-getbidioptions.md)
</dt> </dl>

 

 





