---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL lädt.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: FMEVENT_LOAD Nachricht (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 8001ca861b77755ea7f5ee829a9af490c2f426dcd6179f2fe84831c624bb4ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860655"
---
# <a name="fmevent_load-message"></a>FMEVENT \_ LOAD-Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL lädt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lpfmsld* 
</dt> <dd>

Die Adresse einer [**FMS \_ LOAD-Struktur,**](fms-load.md) die den Änderungswert des Menüelements angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL muss **TRUE** zurückgeben, um das Laden der DLL fortzusetzen. Wenn die DLL **FALSE** zurückgibt, ruft der Datei-Manager die [**FreeLibrary-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) auf und beendet jegliche Kommunikation mit der Erweiterungs-DLL.

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte die Member **dwSize,** **szMenuName** und **hMenu** in der [**FMS \_ LOAD-Struktur ausfüllen.**](fms-load.md) Außerdem sollte der Wert des **wMenuDelta-Elements** gespeichert und zum Identifizieren von Menüelementen beim Ändern des Menüs verwendet werden.

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

 

 
