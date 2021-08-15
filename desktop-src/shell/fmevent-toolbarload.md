---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager seine Symbolleiste lädt. Diese Meldung ermöglicht einer Erweiterungs-DLL, der Symbolleiste des Datei-Managers eine Schaltfläche hinzuzufügen.
title: FMEVENT_TOOLBARLOAD-Nachricht (Wfext.h)
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
ms.openlocfilehash: a8aba636910735e9baa0bd3ebbcf846ecf69a2174b56372a387b541c92e59732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860392"
---
# <a name="fmevent_toolbarload-message"></a>FMEVENT \_ TOOLBARLOAD-Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager seine Symbolleiste lädt. Diese Meldung ermöglicht einer Erweiterungs-DLL, der Symbolleiste des Datei-Managers eine Schaltfläche hinzuzufügen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lpfmstbl* 
</dt> <dd>

Die Adresse einer [**FMS \_ TOOLBARLOAD-Struktur.**](fms-toolbarload.md) Wenn die Erweiterungs-DLL der Symbolleiste im Datei-Manager eine Schaltfläche hinzufügt, sollte die DLL die Struktur mit Informationen über die Schaltfläche füllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL muss **TRUE** zurückgeben, um die Schaltfläche zur Symbolleiste hinzuzufügen. Wenn die DLL **FALSE** zurückgibt, fügt der Datei-Manager die Schaltfläche nicht hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




