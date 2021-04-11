---
description: Registriert eine laufende Anwendung für die Windows-Image Erfassung (WIA) 2,0-Ereignis Benachrichtigung.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'IWiaDevMgr2:: registereventcallbackinterface-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216049"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>IWiaDevMgr2:: registereventcallbackinterface-Methode

Registriert eine laufende Anwendung für die Windows-Image Erfassung (WIA) 2,0-Ereignis Benachrichtigung.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den eindeutigen Bezeichner eines WIA 2,0-Geräts an. Legen Sie diesen Parameter auf **null** fest, um für das Ereignis auf allen WIA 2,0-Geräten zu registrieren.

</dd> <dt>

" *Peer-GUID* \[ " in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *GUID \** _

Gibt einen Zeiger auf den Ereignis Bezeichner an, für den die Anwendung registriert wird. Weitere Informationen finden Sie unter [WIA-Ereignis](-wia-wia-event-identifiers.md) Bezeichner für Standard Ereignis Bezeichner.

</dd> <dt>

_pIWiaEventCallback * \[ in\]
</dt> <dd>

Typ: **[**iwiaeventcallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _

Gibt einen Zeiger auf die [_ *iwiaeventcallback* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) -Schnittstelle an, die von WIA 2,0 zum Senden der Ereignis Benachrichtigung verwendet wird.

</dd> <dt>

" *Peer-Object* \[ " vorgenommen\]
</dt> <dd>

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Empfängt die Adresse eines Zeigers auf die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt die Standard-COM-Fehlercodes oder die folgenden zurück.



| Rückgabecode                                                                               | Beschreibung                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ notimpl**</dt> </dl> | Die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle kann nicht zurückgegeben werden. <br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!WARNING]
> Das Verwenden der [**iwiadevmgr:: registereventcallbackinterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface)-Methode, der **IWiaDevMgr2:: registereventcallbackinterface**-Methode und der [**DeviceManager. registerevent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) -Methode aus demselben Prozess, nachdem der weiterhin Image Dienst neu gestartet wurde, kann zu einer Zugriffsverletzung führen, wenn die Funktionen vor dem Beenden des Dienstes verwendet wurden.

 

Wenn WIA 2,0-Anwendungen mit der Ausführung beginnen, wird diese Methode verwendet, um sich für den Empfang von Hardware Geräte Ereignissen zu registrieren. Dadurch wird verhindert, dass die Anwendung neu gestartet wird, wenn ein anderes Ereignis registriert wird. Sobald eine Anwendung **IWiaDevMgr2:: registereventcallbackinterface** aufruft, um sich für das Empfangen von WIA 2,0-Ereignissen von einem Gerät zu registrieren, werden die registrierten Ereignisse von WIA 2,0 an das Programm weitergeleitet.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den Parameter " *Peer-Object* " empfangen.

> [!Note]  
> In einer Multithreadanwendung kann der Ereignis Benachrichtigungs Rückruf in einem anderen Thread als dem auftreten, der den Rückruf registriert hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
