---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um den Typ des Datei-Manager-Fensters abzurufen, das den Eingabefokus besitzt.
title: FM_GETFOCUS Nachricht (Wfext.h)
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
ms.openlocfilehash: 7512595008ad79d33bf1ac9b381b63831977282b83a8ce595c3d2689087c869c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459110"
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
| <dl> <dt>**\_FMFOCUS-LAUFWERKE**</dt> </dl> | Laufwerksleiste eines Verzeichnisfensters.<br/>         |
| <dl> <dt>**\_FMFOCUS-SUCHE**</dt> </dl> | Fenster "Suchergebnisse".<br/>                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



 

 




