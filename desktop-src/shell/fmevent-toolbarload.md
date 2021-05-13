---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager seine Symbolleiste lädt. Diese Meldung ermöglicht einer Erweiterungs-DLL, der Symbolleiste des Datei-Managers eine Schaltfläche hinzuzufügen.
title: FMEVENT_TOOLBARLOAD Nachricht (Wfext.h)
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
ms.openlocfilehash: c4195acedbd696679a2deea2f4d6e268717566d1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841271"
---
# <a name="fmevent_toolbarload-message"></a>FMEVENT \_ TOOLBARLOAD-Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager seine Symbolleiste lädt. Diese Meldung ermöglicht einer Erweiterungs-DLL, der Symbolleiste des Datei-Managers eine Schaltfläche hinzuzufügen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lpfmstbl* 
</dt> <dd>

Die Adresse einer [**FMS \_ TOOLBARLOAD-Struktur.**](fms-toolbarload.md) Wenn die Erweiterungs-DLL der Symbolleiste im Datei-Manager eine Schaltfläche hinzufügt, sollte die DLL die Struktur mit Informationen zur Schaltfläche füllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL muss **TRUE** zurückgeben, um die Schaltfläche zur Symbolleiste hinzuzufügen. Wenn die DLL **FALSE** zurückgibt, fügt der Datei-Manager die Schaltfläche nicht hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




