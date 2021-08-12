---
description: Die IWiaDevMgr2::RegisterEventCallbackProgram-Methode registriert eine Anwendung zum Empfangen von Geräteereignissen. Es wird in erster Linie aus Gründen der Abwärtskompatibilität mit Anwendungen bereitgestellt, die nicht für Windows Image Acquisition (WIA) 2.0 geschrieben wurden.
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: IWiaDevMgr2::RegisterEventCallbackProgram-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ebc99e61bf038c8db2ea537a1f8a5933ad512d21ec05cf51f6f8b7af5ede2b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441298"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a>IWiaDevMgr2::RegisterEventCallbackProgram-Methode

Die **IWiaDevMgr2::RegisterEventCallbackProgram-Methode** registriert eine Anwendung zum Empfangen von Geräteereignissen. Es wird in erster Linie aus Gründen der Abwärtskompatibilität mit Anwendungen bereitgestellt, die nicht für Windows Image Acquisition (WIA) 2.0 geschrieben wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Die Registrierungsflags. Kann auf die folgenden Werte festgelegt werden.



| Wert                                                                                                                                                                                                           | Bedeutung                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <dt>**WIA \_ \_ REGISTER-EREIGNISRÜCKRUF \_**</dt> </dl>       | Registrieren Sie sich für das Ereignis.<br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <dt>**WIA \_ UNREGISTER \_ EVENT \_ CALLBACK**</dt> </dl> | Löschen Sie die Registrierung für das Ereignis.<br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <dt>**WIA \_ \_ SET-STANDARDHANDLER \_**</dt> </dl>                   | Legen Sie die Anwendung als Standardereignishandler fest.<br/> |



 

</dd> <dt>

*bstrDeviceID* \[ In\]
</dt> <dd>

Typ: **BSTR**

Ein Gerätebezeichner. Übergeben Sie **NULL,** um sich für das Ereignis auf allen WIA 2.0-Geräten zu registrieren.

</dd> <dt>

*pEventGUID* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Das Ereignis, für das die Anwendung registriert wird. Eine Liste gültiger Ereignis-GUIDs finden Sie unter [WIA-Ereignisbezeichner.](-wia-wia-event-identifiers.md)

</dd> <dt>

*bstrFullAppName* \[ In\]
</dt> <dd>

Typ: **BSTR**

Der vollständige Pfadname der Anwendung.

</dd> <dt>

*bstrCommandlineArg* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die entsprechenden Befehlszeilenargumente für die Anwendung.

</dd> <dt>

*bstrName* \[ In\]
</dt> <dd>

Typ: **BSTR**

Der Namen der Anwendung. Der Name wird dem Benutzer angezeigt, wenn sich mehrere Anwendungen für dasselbe Ereignis registrieren.

</dd> <dt>

*bstrDescription* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die Beschreibung der Anwendung. Die Beschreibung wird dem Benutzer angezeigt, wenn sich mehrere Anwendungen für dasselbe Ereignis registrieren.

</dd> <dt>

*bstrIcon* \[ In\]
</dt> <dd>

Typ: **BSTR**

Das Symbol, das die Anwendung darstellt. Das Symbol wird dem Benutzer angezeigt, wenn sich mehrere Anwendungen für dasselbe Ereignis registrieren. Die Zeichenfolge enthält den Namen der Anwendung und den nullbasierten Index des Symbols, getrennt durch ein Komma, z.B. "MyApp, 0". Möglicherweise gibt es mehrere Symbole, die eine Anwendung darstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie **IWiaDevMgr2::RegisterEventCallbackProgram,** um sich für Hardwaregeräteereignisse zu registrieren. Wenn ein Ereignis auftritt, für das eine Anwendung registriert ist, wird die Anwendung gestartet, und die Ereignisinformationen werden an die Anwendung übertragen.

Verwenden Sie die [**EnumRegisterEventInfo-Methode,**](-wia-iwiaitem2-enumregistereventinfo.md) um einen Zeiger auf ein Enumeratorobjekt für Ereignisregistrierungseigenschaften abzurufen.

Verwenden Sie nur die **IWiaDevMgr2::RegisterEventCallbackProgram-Methode** für Abwärtskompatibilität mit Anwendungen, die nicht für die WIA 2.0-Architektur geschrieben wurden. Verwenden Sie die com-Schnittstellen (Component Object Model), die von der WIA 2.0-Architektur bereitgestellt werden, für neue Anwendungen. Rufen Sie insbesondere [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) oder [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) auf, um eine neue Anwendung für Geräteereignisse zu registrieren.

In der Regel wird diese Methode von einem Installationsprogramm oder Skript aufgerufen. Das Installationsprogramm oder Skript registriert die Anwendung zum Empfangen von WIA 2.0-Geräteereignissen. Wenn das Ereignis auftritt, wird die Anwendung vom WIA 2.0-Laufzeitsystem gestartet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 




