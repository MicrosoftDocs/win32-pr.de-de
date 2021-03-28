---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die dll lädt.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: FMEVENT_LOAD Meldung (WF. h)
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
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979705"
---
# <a name="fmevent_load-message"></a>Meldung zum Laden des Ereignisses \_

Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die dll lädt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lpfmsld* 
</dt> <dd>

Die Adresse einer [**Lom- \_ Lade**](fms-load.md) Struktur, die den Delta Wert für das Menü Element angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL muss **true** zurückgeben, um das Laden der dll fortzusetzen. Wenn die DLL **false** zurückgibt, ruft der Datei-Manager die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion auf und beendet jegliche Kommunikation mit der Erweiterungs-DLL.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte die Member " **dwSize**", " **szmenuname**" und " **HMENU** " in der [**FMS- \_ Lade**](fms-load.md) Struktur ausfüllen. Außerdem sollte Sie den Wert des **wmenudelta** -Members speichern und verwenden, um Menü Elemente bei der Menü Änderung zu identifizieren.

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

 

 
