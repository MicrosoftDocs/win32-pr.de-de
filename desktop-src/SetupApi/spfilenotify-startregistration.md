---
description: 'SPFILENOTIFY_STARTREGISTRATION: Wenn Sie die RegisterDlls INF-Direktive verwenden, um DLLs selbst zu registrieren, erhalten Aufrufer von SetupInstallFromInfSection möglicherweise Benachrichtigungen zu jeder Datei, wenn sie registriert oder nicht registriert ist.'
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: SPFILENOTIFY_STARTREGISTRATION (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84f72c237480b2aeb583d9bd7b75fd8ea67f5effc1d51c5baeadc02c4948d3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964100"
---
# <a name="spfilenotify_startregistration-message"></a>SPFILENOTIFY \_ STARTREGISTRATION-Meldung

Wenn Sie die **RegisterDlls** INF-Direktive verwenden, um DLLs selbst zu registrieren, erhalten Aufrufer von [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) möglicherweise Benachrichtigungen zu jeder Datei, wenn sie registriert oder nicht registriert ist. Um eine **SPFILENOTIFY \_ STARTREGISTRATION-Benachrichtigung** einmal an die Rückrufroutine zu senden, bevor Sie eine Datei registrieren, schließen Sie SPINST \_ REGISTERCALLBACKAWARE plus SPINST \_ REGSVR in den *Flags-Parameter* von **SetupInstallFromInfSection** ein. Um eine Benachrichtigung über die Aufhebung der Registrierung zu senden, schließen Sie SPINST \_ REGISTERCALLBACKAWARE plus SPINST \_ UNREGSVR in den *Flags-Parameter* ein.

Die rückrufroutine, die durch den *MsgHandler-Parameter* von [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) angegeben wird, muss vom [Typ PSP \_ FILE \_ CALLBACK sein.](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a) Legen Sie *den Context-Parameter* auf denselben *Kontext fest,* der in **SetupInstallFromInfSection angegeben ist.** Legen Sie den *Notification-Parameter* **auf SPFILENOTIFY \_ STARTREGISTRATION fest.**


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**SP \_ REGISTER CONTROL \_ \_ STATUS-Struktur,**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) die Informationen zur registrierten oder nicht registrierten Datei enthält. Der Member **cbsize** sollte auf die Größe der -Struktur festgelegt werden. Das **FileName-Mitglied** sollte auf den vollqualifizierten Pfad der Datei festgelegt werden, die registriert wird. **Win32Error** wird nicht verwendet und sollte auf NO ERROR festgelegt \_ werden. **FailureCode** wird nicht verwendet und sollte auf SPREG SUCCESS festgelegt \_ werden.

</dd> <dt>

*Param2* 
</dt> <dd>

Wenn die Datei registriert wird, *sollte Param2* auf einen Zeiger auf einen Wert ungleich 0 (null) festgelegt werden. Wenn die Registrierung der Datei aufgehoben wird, sollte *Param2* auf einen Zeiger auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nach dem Empfang der Benachrichtigung gibt die Rückruffunktion möglicherweise einen der folgenden Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl> | Registrieren Oder aufheben Sie die Registrierung der Datei nicht, und beenden Sie die Verarbeitung des INF-Abschnitts.<br/>             |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Registrieren Oder aufheben Sie die Registrierung der Datei, und fahren Sie mit der Verarbeitung des INF-Abschnitts fort.<br/>                |
| <dl> <dt>**DATEI \_ ÜBERSPRINGEN**</dt> </dl>    | Überspringen der Registrierung oder Aufhebung der Registrierung der Datei, aber Fortsetzen der Verarbeitung des INF-Abschnitts<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)
</dt> </dl>

 

