---
description: Registriert eine ausgeführte Anwendung für Windows WIA 2.0-Ereignisbenachrichtigung (Image Acquisition).
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: IWiaDevMgr2::RegisterEventCallbackInterface-Methode (Wia.h)
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
ms.openlocfilehash: e2658654254257c707d12f4e676aee3371f0ad491dfedeb0637508ca3f33a057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965640"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>IWiaDevMgr2::RegisterEventCallbackInterface-Methode

Registriert eine ausgeführte Anwendung für Windows WIA 2.0-Ereignisbenachrichtigung (Image Acquisition).

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

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstrDeviceID* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den eindeutigen Bezeichner eines WIA 2.0-Geräts an. Legen Sie diesen Parameter auf **NULL fest,** um sich auf allen WIA 2.0-Geräten für das Ereignis zu registrieren.

</dd> <dt>

*pEventGUID* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Gibt einen Zeiger auf den Ereignisbezeichner an, für den die Anwendung registriert wird. Standardereignisbezeichner finden Sie unter [WIA-Ereignisbezeichner.](-wia-wia-event-identifiers.md)

</dd> <dt>

*pIWiaEventCallback* \[ In\]
</dt> <dd>

Typ: **[ **IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\***

Gibt einen Zeiger auf die [**IWiaEventCallback-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) an, die wia 2.0 zum Senden von Ereignisbenachrichtigungen verwendet.

</dd> <dt>

*pEventObject* \[ out\]
</dt> <dd>

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Empfängt die Adresse eines Zeigers auf die [IUnknown-Schnittstelle.](/windows/win32/api/unknwn/nn-unknwn-iunknown)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt die STANDARDMÄßIGEN COM-Fehlercodes oder die folgenden zurück.



| Rückgabecode                                                                               | Beschreibung                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Die [IUnknown-Schnittstelle](/windows/win32/api/unknwn/nn-unknwn-iunknown) kann nicht zurückgegeben werden. <br/> |



 

## <a name="remarks"></a>Hinweise

> [!WARNING]
> Die Verwendung der [**Methoden IWiaDevMgr::RegisterEventCallbackInterface,**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) **IWiaDevMgr2::RegisterEventCallbackInterface** und [**DeviceManager.RegisterEvent aus**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) demselben Prozess nach dem Neustart des Still Image Service kann zu einer Zugriffsverletzung führen, wenn die Funktionen vor dem Abbruch des Diensts verwendet wurden.

 

Wenn WIA 2.0-Anwendungen mit der Ausführung beginnen, verwenden sie diese Methode, um sich für den Empfang von Hardwaregeräteereignissen zu registrieren. Dadurch wird verhindert, dass die Anwendung neu gestartet wird, wenn ein anderes Ereignis auftritt, für das sie registriert ist. Sobald eine Anwendung **IWiaDevMgr2::RegisterEventCallbackInterface** aufruft, um sich selbst für den Empfang von WIA 2.0-Ereignissen von einem Gerät zu registrieren, werden die registrierten Ereignisse von WIA 2.0 an das Programm geroutet.

Anwendungen müssen die [IUnknown::Release-Methode für](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) die Schnittstellenze0er aufrufen, die sie über den *pEventObject-Parameter* empfangen.

> [!Note]  
> In einer Multithreadanwendung kann der Ereignisbenachrichtigungsrückruf in einem anderen Thread als dem kommen, der den Rückruf registriert hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
