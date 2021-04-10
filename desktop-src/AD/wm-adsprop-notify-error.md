---
title: WM_ADSPROP_NOTIFY_ERROR Meldung (adsprop. h)
description: Die "WM \_ adsprop \_ Notify Error"- \_ Meldung fügt eine Fehlermeldung zu einer Liste von Fehlermeldungen hinzu, die durch Aufrufen der adspropshowerrordialog-Funktion angezeigt werden.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_ERROR Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103791"
---
# <a name="wm_adsprop_notify_error-message"></a>WM \_ adsprop- \_ Benachrichtigungs \_ Fehlermeldung

Die " **WM \_ adsprop \_ Notify \_ Error** "-Meldung fügt eine Fehlermeldung zu einer Liste von Fehlermeldungen hinzu, die durch Aufrufen der [**adspropshowerrordialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) -Funktion angezeigt werden.


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Handle des Benachrichtigungs Objekts. Dies ist der *hnotifyobject* -Parameter, der von [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)abgerufen wird.

</dd> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**adsproperror**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) -Struktur, die Fehlermeldungs Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Die [**adspropsenderrormessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) -Funktion ist die bevorzugte Methode zum Senden dieser Nachricht.

Die von der " **WM \_ adsprop \_ Notify \_ Error** "-Meldung hinzugefügten Fehlermeldungen werden gesammelt, bis " [**adspropshowerrordialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) " aufgerufen wird. **Adspropshowerrordialog** kombiniert die gesammelten Fehlermeldungen und zeigt diese an. Wenn das Fehler Dialogfeld verworfen wird, werden die gesammelten Fehlermeldungen gelöscht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Nachrichten in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**Adsproperror**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[**Adspropsenderrormessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[**Adspropshowerrordialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





