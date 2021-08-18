---
description: Die IWiaDevMgr2::RegisterEventCallbackCLSID-Methode registriert eine Anwendung, um Ereignisse zu empfangen, auch wenn die Anwendung nicht ausgeführt wird.
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: IWiaDevMgr2::RegisterEventCallbackCLSID-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9137fdd33f59eb841a54e84a6d12bb0b08968ac29c8737afbf56f66c57176c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965648"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a>IWiaDevMgr2::RegisterEventCallbackCLSID-Methode

Die **IWiaDevMgr2::RegisterEventCallbackCLSID-Methode** registriert eine Anwendung, um Ereignisse zu empfangen, auch wenn die Anwendung nicht ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt Registrierungsflags an. Kann auf die folgenden Werte festgelegt werden:



| Registrierungsflag                | Bedeutung                                           |
|----------------------------------|---------------------------------------------------|
| WIA \_ \_ REGISTER-EREIGNISRÜCKRUF \_   | Registrieren Sie sich für das Ereignis.                           |
| WIA \_ UNREGISTER \_ EVENT \_ CALLBACK | Löschen Sie die Registrierung für das Ereignis.            |
| WIA \_ \_ SET-STANDARDHANDLER \_       | Legen Sie die Anwendung als Standardereignishandler fest. |



 

</dd> <dt>

*bstrDeviceID* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt einen Gerätebezeichner an. Übergeben Sie **NULL,** um sich für das Ereignis auf allen WIA 2.0-Geräten zu registrieren.

</dd> <dt>

*pEventGUID* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Gibt das Ereignis an, für das die Anwendung registriert wird. Eine Liste der Standardereignisse finden Sie unter [WIA-Ereignisbezeichner.](-wia-wia-event-identifiers.md)

</dd> <dt>

*pClsID* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Zeiger auf die Anwendungsklassen-ID (**CLSID**). Das WIA 2.0-Laufzeitsystem verwendet die **Anwendungs-CLSID,** um die Anwendung zu starten, wenn ein Ereignis auftritt, für das es registriert ist.

</dd> <dt>

*bstrName* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Anwendung an, die für das Ereignis registriert wird.

</dd> <dt>

*bstrDescription* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt eine Textbeschreibung der Anwendung an, die für das Ereignis registriert wird.

</dd> <dt>

*bstrIcon* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen einer Bilddatei an, die für das Symbol für die Anwendung verwendet werden soll, die für das Ereignis registriert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

WIA 2.0-Anwendungen verwenden diese Methode, um sich für den Empfang von Hardwaregeräteereignissen zu registrieren. Nachdem **IWiaDevMgr2::RegisterEventCallbackCLSID** aufgerufen wurde, wird die Anwendung für den Empfang von WIA 2.0-Geräteereignissen registriert, auch wenn sie nicht ausgeführt wird.

Wenn das Ereignis auftritt, bestimmt das WIA 2.0-System, welche Anwendung für den Empfang des Ereignisses registriert ist. Sie verwendet die [CoCreateInstance-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) und die im *pClsID-Parameter* angegebene CLSID, um eine Instanz der Anwendung zu erstellen, und ruft dann die [**ImageEventCallback-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) auf, um die Ereignisinformationen an die Anwendung zu übertragen.

Eine Anwendung kann die [**EnumRegisterEventInfo-Methode**](-wia-iwiaitem2-enumregistereventinfo.md) aufrufen, um Ereignisregistrierungsinformationen aufzuzählen.

Wenn die Anwendung keine registrierte com-Komponente (Component Object Model) ist und nicht mit der WIA 2.0-Architektur kompatibel ist, verwenden Sie die [**IWiaDevMgr2::RegisterEventCallbackProgram-Methode,**](-wia-iwiadevmgr2-registereventcallbackprogram.md) um eine Anwendung für Geräteereignisse zu registrieren.

> [!Note]  
> In einer Multithreadanwendung gibt es keine Garantie dafür, dass der Ereignisbenachrichtigungsrückruf für denselben Thread zurückgegeben wird, der den Rückruf registriert hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 
