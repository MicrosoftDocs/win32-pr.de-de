---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um den Typ des Datei-Manager-Fensters abzurufen, das den Eingabefokus besitzt.
title: FM_GETFOCUS (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841411"
---
# <a name="fm_getfocus-message"></a>FM \_ GETFOCUS-Nachricht

Wird von einer Datei-Manager-Erweiterung gesendet, um den Typ des Datei-Manager-Fensters abzurufen, das den Eingabefokus besitzt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Typ des Datei-Manager-Fensters zurück, das den Eingabefokus besitzt. Dieses Argument einen der folgenden Werte annehmen.



| Rückgabecode                                                                                    | Beschreibung                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**FMFOCUS \_ DIR**</dt> </dl>    | Verzeichnisteil eines Verzeichnisfensters.<br/> |
| <dl> <dt>**\_FMFOCUS-STRUKTUR**</dt> </dl>   | Strukturteil eines Verzeichnisfensters.<br/>      |
| <dl> <dt>**\_FMFOCUS-LAUFWERKE**</dt> </dl> | Die Laufwerkleiste eines Verzeichnisfensters.<br/>         |
| <dl> <dt>**\_FMFOCUS-SUCHE**</dt> </dl> | Suchergebnisfenster.<br/>                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



 

 




