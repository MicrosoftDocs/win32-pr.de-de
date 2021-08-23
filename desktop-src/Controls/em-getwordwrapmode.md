---
title: EM_GETWORDWRAPMODE (Richedit.h)
description: Ruft die aktuellen Optionen für Zeilenumbruch und Wörterumbruch für das Rich-Edit-Steuerelement ab.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- EM_GETWORDWRAPMODE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef3127e5ce3652e9103dfa0e030d66ec7b1b085bc4b60d0cf0bb3f03a30d3fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437950"
---
# <a name="em_getwordwrapmode-message"></a>EM \_ GETWORDWRAPMODE-Nachricht

Ruft die aktuellen Optionen für Zeilenumbruch und Wörterumbruch für das Rich-Edit-Steuerelement ab.

> [!Note]  
> Diese Meldung wird nur in asiatisch-sprachbasierten Versionen von Microsoft Rich Edit 1.0 unterstützt. Sie wird in späteren Versionen von Rich Edit nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Meldung gibt die aktuellen Optionen für Zeilenumbruch und Wörterumbruch zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung darf nicht von der anwendungsdefinierten Prozedur mit Wörterbruch gesendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





