---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager Ihre Symbolleiste lädt. Diese Meldung ermöglicht der Erweiterungs-DLL, der Datei-Manager-Symbolleiste eine Schaltfläche hinzuzufügen.
title: FMEVENT_TOOLBARLOAD Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215954"
---
# <a name="fmevent_toolbarload-message"></a>Meldung für das Meldung "f" \_

Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager Ihre Symbolleiste lädt. Diese Meldung ermöglicht der Erweiterungs-DLL, der Datei-Manager-Symbolleiste eine Schaltfläche hinzuzufügen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lpfmstbl* 
</dt> <dd>

Die Adresse einer [**f- \_ Load**](fms-toolbarload.md) -Struktur. Wenn die Erweiterungs-DLL der Symbolleiste im Datei-Manager eine Schaltfläche hinzufügt, sollte die dll die Struktur mit Informationen über die Schaltfläche Auffüllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL muss **true** zurückgeben, um der Symbolleiste die Schaltfläche hinzuzufügen. Wenn die DLL **false** zurückgibt, fügt der Datei-Manager die Schaltfläche nicht hinzu.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> </dl>

 

 




