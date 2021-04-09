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
# <a name="registering-for-events"></a><span data-ttu-id="9bb39-103">Registrieren für Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9bb39-103">Registering for Events</span></span>

<span data-ttu-id="9bb39-104">Im folgenden Beispiel wird die Methode Windows-Abbild Beschaffung (WIA) 1,0 [**iwiadevmgr:: registereventcallbackclsid**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) verwendet, um eine Benachrichtigung zu registrieren, wenn ein Windows-Abbild Erfassungsgerät (WIA) mit dem System verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="9bb39-104">The following example uses the Windows Image Acquisition (WIA) 1.0 [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) method to register for notification when any Windows Image Acquisition (WIA) device is connected to the system.</span></span> <span data-ttu-id="9bb39-105">Anwendungen können auch WIA 1,0 [**iwiadevmgr:: registereventcallbackinterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) und WIA 1,0 [**iwiadevmgr:: registereventcallbackprogram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) verwenden, um sich für Ereignisse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="9bb39-105">Applications can also use WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) and WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register for events.</span></span> <span data-ttu-id="9bb39-106">Mit Windows Vista und höher können Sie die Methoden Windows Image Acquisition (WIA) 2,0 [**IWiaDevMgr2:: registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2:: registereventcallbackinterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)oder [**IWiaDevMgr2:: registereventcallbackprogram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) verwenden, um sich für Ereignisse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="9bb39-106">With Windows Vista and later, you can use the Windows Image Acquisition (WIA) 2.0 [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md), or [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) methods to register for events.</span></span>

<span data-ttu-id="9bb39-107">Es wird davon ausgegangen, dass das Beispiel aus einer Anwendung stammt, die als Component Object Model (com) out-of-Process-Server Objekt registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9bb39-107">It is assumed that the example is taken from an application that is registered as a Component Object Model (COM) out-of-process server object.</span></span>

<span data-ttu-id="9bb39-108">Der Aufruf von [**iwiadevmgr:: registereventcallbackclsid**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (oder [**IWiaDevMgr2:: registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9bb39-108">The call to [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) is as follows:</span></span>


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



<span data-ttu-id="9bb39-109">Im vorherigen Code ist **pwiadevmgr** ein gültiger Zeiger auf die Schnittstelle [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)). der WIA \_ - \_ Registrierungs \_ Ereignis Rückruf ist eine Konstante, die angibt, dass sich dieser Aufruf für das Ereignis registrieren soll, anstatt die Registrierung für das Ereignis aufzuheben, dass das WIA- \_ Ereignis \_ Gerät verbunden ist, das \_ angibt, dass die Anwendung für die Benachrichtigung registriert wird, wenn ein Gerät mit dem Computer des Benutzers verbunden ist. **pclsid** ist ein Zeiger auf die registrierte CLSID der Anwendung. **bstrinname** ist der Name der Anwendung, **bstraudescription** ist eine Textbeschreibung der Anwendung, und **bstricon** ist der Name einer Bilddatei, die für das Symbol für die Anwendung verwendet werden soll, die für das Ereignis registriert wird.</span><span class="sxs-lookup"><span data-stu-id="9bb39-109">In the previous code, **pWiaDevMgr** is a valid pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface, WIA\_REGISTER\_EVENT\_CALLBACK is a constant that specifies that this call is to register for the event as opposed to unregistering for the event, WIA\_EVENT\_DEVICE\_CONNECTED is a constant that specifies that the application is registering to be notified whenever a device is connected to the user's computer, **pCLSID** is a pointer to the registered CLSID of the application, **bstrName** is the name of the application, **bstrDescription** is a text description of the application, and **bstrIcon** is the name of an image file to be used for the icon for the application registering for the event.</span></span>

<span data-ttu-id="9bb39-110">Die Anwendung muss dann die [**iwiaeventcallback:: imageeventcallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) -Methode implementieren, die immer dann aufgerufen wird, wenn ein Ereignis auftritt, für das die Anwendung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9bb39-110">The application must then implement the [**IWiaEventCallback::ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method, which is called whenever an event occurs for which the application is registered.</span></span>

<span data-ttu-id="9bb39-111">Eine Anwendung kann die [**iwiaitem:: enumregistereventinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (oder [**IWiaItem2:: enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md))-Methode verwenden, um die Informationen zu Ereignissen aufzulisten, für die Sie registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9bb39-111">An application can use the [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) method to enumerate the information about events for which it is registered.</span></span>

 

 



