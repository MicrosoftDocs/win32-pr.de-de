---
title: EM_GETTYPOGRAPHYOPTIONS Meldung (RichEdit. h)
description: Gibt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuer Elements zurück.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- Windows-Steuerelemente für EM_GETTYPOGRAPHYOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105105"
---
# <a name="em_gettypographyoptions-message"></a>EM \_ gettypographyoptions-Meldung

Gibt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuer Elements zurück.

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

Gibt die aktuellen Typografieoptionen zurück. Eine Liste der Optionen finden Sie unter [**EM \_ settypographyoptions**](em-settypographyoptions.md).

## <a name="remarks"></a>Bemerkungen

Sie können den erweiterten Zeilenumbruch aktivieren, indem Sie die Nachricht " [**EM \_ settypographyoptions**](em-settypographyoptions.md) " senden. Erweiterte und normale Zeilenumbruch können auch automatisch durch das Rich Edit-Steuerelement aktiviert werden, wenn es für bestimmte Sprachen benötigt wird.

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

[**EM \_ settypographyoptions**](em-settypographyoptions.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Informationen zu Rich Edit-Steuerelementen](about-rich-edit-controls.md)
</dt> </dl>

 

 





