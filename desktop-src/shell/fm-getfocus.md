---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um den Typ des Datei-Manager-Fensters abzurufen, das den Eingabefokus besitzt.
title: FM_GETFOCUS Meldung (WF. h)
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
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979736"
---
# <a name="fm_getfocus-message"></a>FM \_ GetFocus-Nachricht

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
| <dl> <dt>**fmfocus- \_ dir**</dt> </dl>    | Verzeichnis Teil eines Verzeichnis Fensters.<br/> |
| <dl> <dt>**fmfocus \_ -Struktur**</dt> </dl>   | Struktur Teil eines Verzeichnis Fensters.<br/>      |
| <dl> <dt>**fmfocus- \_ Laufwerke**</dt> </dl> | Laufwerk Leiste eines Verzeichnis Fensters.<br/>         |
| <dl> <dt>**fmfocus- \_ Suche**</dt> </dl> | Fenster "Suchergebnisse".<br/>                   |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



 

 




