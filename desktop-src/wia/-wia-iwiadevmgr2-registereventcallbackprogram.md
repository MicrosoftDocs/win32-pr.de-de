---
description: 'Die IWiaDevMgr2:: registereventcallbackprogram-Methode registriert eine Anwendung, um Geräte Ereignisse zu empfangen. Es wird hauptsächlich aus Gründen der Abwärtskompatibilität mit Anwendungen bereitgestellt, die nicht für die Windows-Abbild Beschaffung (WIA) 2,0 geschrieben wurden.'
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'IWiaDevMgr2:: registereventcallbackprogram-Methode (WIA. h)'
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
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353134"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a>IWiaDevMgr2:: registereventcallbackprogram-Methode

Die **IWiaDevMgr2:: registereventcallbackprogram** -Methode registriert eine Anwendung, um Geräte Ereignisse zu empfangen. Es wird hauptsächlich aus Gründen der Abwärtskompatibilität mit Anwendungen bereitgestellt, die nicht für die Windows-Abbild Beschaffung (WIA) 2,0 geschrieben wurden.

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

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Die Registrierungsflags. Kann auf die folgenden Werte festgelegt werden.



| Wert                                                                                                                                                                                                           | Bedeutung                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <dt>**WIA- \_ Register \_ Ereignis \_ Rückruf**</dt> </dl>       | Registrieren Sie sich für das-Ereignis.<br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <dt>**\_ \_ Ereignis Rückruf für die Aufhebung der Registrierung \_**</dt> </dl> | Löschen Sie die Registrierung für das Ereignis.<br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <dt>**WIA \_ - \_ Standard \_ Handler festlegen**</dt> </dl>                   | Legen Sie die Anwendung als Standard Ereignishandler fest.<br/> |



 

</dd> <dt>

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Ein Geräte Bezeichner. Übergeben Sie **null** , um für das Ereignis auf allen WIA 2,0-Geräten zu registrieren.

</dd> <dt>

" *Peer-GUID* \[ " in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *GUID \** _

Das Ereignis, für das die Anwendung registriert wird. Eine Liste gültiger Ereignis-GUIDs finden Sie unter [WIA-Ereignis](-wia-wia-event-identifiers.md)Bezeichner.

</dd> <dt>

_bstrFullAppName * \[ in\]
</dt> <dd>

Typ: **BSTR**

Der vollständige Pfadname der Anwendung.

</dd> <dt>

*bstraucommandlinearg* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die entsprechenden Befehlszeilenargumente für die Anwendung.

</dd> <dt>

*bstrinname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Der Namen der Anwendung. Der Name wird dem Benutzer angezeigt, wenn sich mehrere Anwendungen für dasselbe Ereignis registrieren.

</dd> <dt>

*bstraudescription* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die Beschreibung der Anwendung. Die Beschreibung wird dem Benutzer angezeigt, wenn sich mehrere Anwendungen für dasselbe Ereignis registrieren.

</dd> <dt>

*bstricon* \[ in\]
</dt> <dd>

Typ: **BSTR**

Das Symbol, das die Anwendung darstellt. Das Symbol wird dem Benutzer angezeigt, wenn sich mehrere Anwendungen für dasselbe Ereignis registrieren. Die Zeichenfolge enthält den Namen der Anwendung und den NULL basierten Index des Symbols, getrennt durch ein Komma, z. b. "MyApp, 0". Möglicherweise gibt es mehrere Symbole, die eine Anwendung darstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **IWiaDevMgr2:: registereventcallbackprogram** , um sich für Hardware Geräte Ereignisse zu registrieren. Wenn ein Ereignis auftritt, bei dem eine Anwendung für registriert ist, wird die Anwendung gestartet, und die Ereignis Informationen werden an die Anwendung übertragen.

Verwenden Sie die [**enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md) -Methode, um einen Zeiger auf ein Enumeratorobjekt für Ereignis Registrierungs Eigenschaften abzurufen.

Verwenden Sie die **IWiaDevMgr2:: registereventcallbackprogram** -Methode nur für die Abwärtskompatibilität mit Anwendungen, die nicht für die WIA 2,0-Architektur geschrieben wurden. Verwenden Sie die von der WIA 2,0-Architektur bereitgestellten Component Object Model (com)-Schnittstellen für neue Anwendungen. Rufen Sie insbesondere [**IWiaDevMgr2:: registereventcallbackinterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) oder [**IWiaDevMgr2:: registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md) auf, um eine neue Anwendung für Geräte Ereignisse zu registrieren.

In der Regel wird diese Methode von einem Installationsprogramm oder einem Skript aufgerufen. Das Installationsprogramm oder Skript registriert die Anwendung, um WIA 2,0-Geräte Ereignisse zu empfangen. Wenn das Ereignis auftritt, wird die Anwendung vom WIA 2,0-Laufzeitsystem gestartet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




