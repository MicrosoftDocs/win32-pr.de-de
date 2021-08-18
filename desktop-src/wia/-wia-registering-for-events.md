---
description: Im folgenden Beispiel wird die methode Windows Image Acquisition (WIA) 1.0 IWiaDevMgr::RegisterEventCallbackCLSID verwendet, um sich für die Benachrichtigung zu registrieren, wenn ein Windows WIA-Gerät (Image Acquisition) mit dem System verbunden ist.
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Registrieren für Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7a72614533ccc7c2f72bb4f2cf105107cc88ef8030cf306d31d6d9ffa5b4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965549"
---
# <a name="registering-for-events"></a>Registrieren für Ereignisse

Im folgenden Beispiel wird die methode Windows Image Acquisition (WIA) 1.0 [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) verwendet, um sich für die Benachrichtigung zu registrieren, wenn ein Windows WIA-Gerät (Image Acquisition) mit dem System verbunden ist. Anwendungen können auch WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) und WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) verwenden, um sich für Ereignisse zu registrieren. Mit Windows Vista und höher können Sie die methoden Windows Image Acquisition (WIA) 2.0 [**IWiaDevMgr2::RegisterEventCallbackCLSID,**](-wia-iwiadevmgr2-registereventcallbackclsid.md) [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)oder [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) verwenden, um sich für Ereignisse zu registrieren.

Es wird davon ausgegangen, dass das Beispiel aus einer Anwendung stammt, die als out-of-process-Serverobjekt Component Object Model (COM) registriert ist.

Der Aufruf von [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (oder [**IWiaDevMgr2::RegisterEventCallbackCLSID)**](-wia-iwiadevmgr2-registereventcallbackclsid.md)lautet wie folgt:


```
    pWiaDevMgr->RegisterEventCallbackCLSID( WIA_REGISTER_EVENT_CALLBACK,
                                            NULL,
                                            WIA_EVENT_DEVICE_CONNECTED,
                                            pCLSID,
                                            bstrName,
                                            bstrDescription,
                                            bstrIcon
                                            );
```



Im vorherigen Code ist **pWiaDevMgr** ein gültiger Zeiger auf die [**Schnittstelle IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (oder [**IWiaDevMgr2).**](-wia-iwiadevmgr2.md)WIA \_ REGISTER EVENT \_ \_ CALLBACK ist eine Konstante, die angibt, dass dieser Aufruf für das Ereignis registriert werden soll, anstatt die Registrierung für das Ereignis aufheben zu müssen. WIA \_ EVENT DEVICE CONNECTED ist eine \_ \_ Konstante, die angibt, dass die Anwendung registriert wird, um benachrichtigt zu werden, wenn ein Gerät mit dem Computer des Benutzers verbunden ist, **pCLSID** ein Zeiger auf die registrierte CLSID der Anwendung, **bstrName** ist der Name der Anwendung, **bstrDescription** ist eine Textbeschreibung der Anwendung, und **bstrIcon** ist der Name einer Bilddatei, die für das Symbol für die Anwendung verwendet werden soll, die sich für das Ereignis registriert.

Die Anwendung muss dann die [**IWiaEventCallback::ImageEventCallback-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) implementieren, die immer dann aufgerufen wird, wenn ein Ereignis auftritt, für das die Anwendung registriert ist.

Eine Anwendung kann die [**IWiaItem::EnumRegisterEventInfo-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (oder [**IWiaItem2::EnumRegisterEventInfo)**](-wia-iwiaitem2-enumregistereventinfo.md)verwenden, um die Informationen zu Ereignissen aufzulisten, für die sie registriert ist.

 

 



