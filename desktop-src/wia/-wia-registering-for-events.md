---
description: 'Im folgenden Beispiel wird die Methode Windows-Abbild Beschaffung (WIA) 1,0 iwiadevmgr:: registereventcallbackclsid verwendet, um eine Benachrichtigung zu registrieren, wenn ein Windows-Abbild Erfassungsgerät (WIA) mit dem System verbunden ist.'
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Registrieren für Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40fe29be23bda4a3094ff8bcf90ae1ca677e858d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129400"
---
# <a name="registering-for-events"></a>Registrieren für Ereignisse

Im folgenden Beispiel wird die Methode Windows-Abbild Beschaffung (WIA) 1,0 [**iwiadevmgr:: registereventcallbackclsid**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) verwendet, um eine Benachrichtigung zu registrieren, wenn ein Windows-Abbild Erfassungsgerät (WIA) mit dem System verbunden ist. Anwendungen können auch WIA 1,0 [**iwiadevmgr:: registereventcallbackinterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) und WIA 1,0 [**iwiadevmgr:: registereventcallbackprogram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) verwenden, um sich für Ereignisse zu registrieren. Mit Windows Vista und höher können Sie die Methoden Windows Image Acquisition (WIA) 2,0 [**IWiaDevMgr2:: registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2:: registereventcallbackinterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)oder [**IWiaDevMgr2:: registereventcallbackprogram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) verwenden, um sich für Ereignisse zu registrieren.

Es wird davon ausgegangen, dass das Beispiel aus einer Anwendung stammt, die als Component Object Model (com) out-of-Process-Server Objekt registriert ist.

Der Aufruf von [**iwiadevmgr:: registereventcallbackclsid**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (oder [**IWiaDevMgr2:: registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) lautet wie folgt:


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



Im vorherigen Code ist **pwiadevmgr** ein gültiger Zeiger auf die Schnittstelle [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)). der WIA \_ - \_ Registrierungs \_ Ereignis Rückruf ist eine Konstante, die angibt, dass sich dieser Aufruf für das Ereignis registrieren soll, anstatt die Registrierung für das Ereignis aufzuheben, dass das WIA- \_ Ereignis \_ Gerät verbunden ist, das \_ angibt, dass die Anwendung für die Benachrichtigung registriert wird, wenn ein Gerät mit dem Computer des Benutzers verbunden ist. **pclsid** ist ein Zeiger auf die registrierte CLSID der Anwendung. **bstrinname** ist der Name der Anwendung, **bstraudescription** ist eine Textbeschreibung der Anwendung, und **bstricon** ist der Name einer Bilddatei, die für das Symbol für die Anwendung verwendet werden soll, die für das Ereignis registriert wird.

Die Anwendung muss dann die [**iwiaeventcallback:: imageeventcallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) -Methode implementieren, die immer dann aufgerufen wird, wenn ein Ereignis auftritt, für das die Anwendung registriert ist.

Eine Anwendung kann die [**iwiaitem:: enumregistereventinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (oder [**IWiaItem2:: enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md))-Methode verwenden, um die Informationen zu Ereignissen aufzulisten, für die Sie registriert ist.

 

 



