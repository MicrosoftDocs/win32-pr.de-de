---
description: Bei der Verwendung der RegisterDLLs-INF-Direktive für die Selbstregistrierung von DLLs erhalten Aufrufer von setupinstallfrominfsection möglicherweise Benachrichtigungen zu jeder Datei, während Sie registriert oder deren Registrierung aufgehoben wird.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: SPFILENOTIFY_STARTREGISTRATION Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355310"
---
# <a name="spfilenotify_startregistration-message"></a>Spfilenotify- \_ startregitionsnachricht

Bei der Verwendung der **RegisterDLLs** -INF-Direktive für die Selbstregistrierung von DLLs erhalten Aufrufer von [**setupinstallfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) möglicherweise Benachrichtigungen zu jeder Datei, während Sie registriert oder deren Registrierung aufgehoben wird. Wenn Sie eine **spfilenotify- \_ startregitionsbenachrichtigung** an die Rückruf Routine senden möchten, bevor Sie eine Datei registrieren, schließen Sie spinst \_ registercallbackaware Plus spinst \_ REGSVR in den *Flags* -Parameter von **setupinstallfrominfsection** ein. Um eine Benachrichtigung über die Aufhebung der Registrierung zu senden, schließen Sie spinst \_ registercallbackaware Plus spinst \_ unregsvr in den *Flags* -Parameter ein.

Die Rückruf Routine, die vom *msghandler* -Parameter von [**setupinstallfrominfisection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) angegeben wird, muss der Datentyp " [PSP \_ file \_ Callback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)" sein. Legen Sie den *context* -Parameter auf denselben *Kontext* fest, der in **setupinstallfrominfsection** angegeben ist. Legen Sie den *Benachrichtigungs* Parameter auf **spfilenotify \_ startregistration** fest.


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**SP- \_ Register \_ Steuer \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) Element-Status Struktur, die Informationen über die Datei enthält, die registriert oder nicht registriert wird. Der Member **CBSIZE** sollte auf die Größe der Struktur festgelegt werden. Der **Dateiname** muss auf den voll qualifizierten Pfad der Datei festgelegt werden, die registriert wird. **Win32Error** wird nicht verwendet und sollte auf keinen Fehler festgelegt werden \_ . " **FailureCode** " wird nicht verwendet und sollte auf "auf der festgelegte Ausführung" festgelegt werden \_ .

</dd> <dt>

*Param2* 
</dt> <dd>

Wenn die Datei registriert wird, sollte *Param2* auf einen Zeiger auf einen Wert ungleich 0 (null) festgelegt werden. Wenn die Registrierung der Datei aufgehoben wird, muss *Param2* auf einen Zeiger auf NULL festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nach dem Empfang der Benachrichtigung kann die Rückruffunktion einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**fileOp- \_ Abbruch**</dt> </dl> | Registrieren oder heben Sie die Registrierung der Datei nicht auf, und deaktivieren Sie die Verarbeitung des INF-Abschnitts.<br/>             |
| <dl> <dt>**fileOp- \_ doit**</dt> </dl>  | Registrieren oder Aufheben der Registrierung der Datei und Fortsetzen der Verarbeitung des INF-Abschnitts.<br/>                |
| <dl> <dt>**Datei \_ übersprungen**</dt> </dl>    | Registrierung oder Aufhebung der Registrierung der Datei überspringen, die Verarbeitung des INF-Abschnitts fortsetzen<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**Setupinstallfrominf-Abschnitt**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[**spfilenotify- \_ endregistrierung**](spfilenotify-endregistration.md)
</dt> </dl>

 

