---
description: 'SPFILENOTIFY_ENDREGISTRATION: Wenn Sie die RegisterDlls INF-Direktive verwenden, um DLLs selbst zu registrieren, erhalten Aufrufer von SetupInstallFromInfSection möglicherweise Benachrichtigungen zu jeder Datei, wenn sie registriert oder nicht registriert ist.'
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: SPFILENOTIFY_ENDREGISTRATION (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec341c26f9f88390ff1b807e6e932b3b381cd57
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094508"
---
# <a name="spfilenotify_endregistration-message"></a>SPFILENOTIFY \_ ENDREGISTRATION-Meldung

Wenn Sie die **RegisterDlls** INF-Direktive verwenden, um DLLs selbst zu registrieren, erhalten Aufrufer von [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) möglicherweise Benachrichtigungen zu jeder Datei, wenn sie registriert oder nicht registriert ist. Um eine **SPFILENOTIFY \_ ENDREGISTRATION-Benachrichtigung** einmal nach dem Registrieren oder Aufheben der Registrierung einer Datei an eine Rückrufroutine zu senden, schließen Sie SPINST \_ REGISTERCALLBACKAWARE plus SPINST \_ REGSVR in den *Flags-Parameter* von **SetupInstallFromInfSection** ein. Um eine Benachrichtigung über die Aufhebung der Registrierung zu senden, schließen Sie SPINST \_ REGISTERCALLBACKAWARE plus SPINST \_ UNREGSVR in den *Flags-Parameter* ein.

Die rückrufroutine, die durch den *MsgHandler-Parameter* von [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) angegeben wird, muss vom [Typ PSP \_ FILE \_ CALLBACK sein.](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a) Legen Sie *den Context-Parameter* auf denselben *Kontext fest,* der in **SetupInstallFromInfSection angegeben ist.** Legen Sie den *Notification-Parameter* **auf SPFILENOTIFY \_ ENDREGISTRATION fest.**


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**SP \_ REGISTER CONTROL \_ \_ STATUS-Struktur,**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) die Informationen zur registrierten oder nicht registrierten Datei enthält. Der Member **cbsize** sollte auf die Größe der -Struktur festgelegt werden. **FileName** sollte auf den vollqualifizierten Pfad der Datei festgelegt werden, die registriert wird. **Win32Error** sollte auf einen Systemfehlercode [festgelegt werden,](/windows/desktop/Debug/system-error-codes) der einen erweiterten Fehlercode angibt. **FailureCode** sollte auf einen der gültigen Fehlercodes festgelegt werden, die das Ergebnis der Registrierung angeben. Gültige Fehlercodes finden Sie unter [**SP \_ REGISTER CONTROL \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).

</dd> <dt>

*Param2* 
</dt> <dd>

Wenn die Datei registriert wird, sollte *Param2* auf einen Zeiger auf einen Wert ungleich 0 (null) festgelegt werden. Wenn die Registrierung der Datei aufgehoben wird, sollte *Param2* auf einen Zeiger auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nach dem Empfang der Benachrichtigung gibt die Rückruffunktion möglicherweise einen der folgenden Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl> | Beenden Sie die Verarbeitung des INF-Abschnitts.<br/>     |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Fahren Sie mit der Verarbeitung des Abschnitts INF fort.<br/> |
| <dl> <dt>**FILE \_ SKIP**</dt> </dl>    | Fortsetzen der Verarbeitung des INF-Abschnitts<br/>  |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)
</dt> </dl>

 

