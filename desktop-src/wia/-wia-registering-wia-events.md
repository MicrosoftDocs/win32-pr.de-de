---
description: 'Anwendungen können sich registrieren, um über Windows WIA-Hardwaregeräteereignisse (Image Acquisition) benachrichtigt zu werden, indem sie eine der folgenden Schnittstellenmethoden IWiaDevMgr oder IWiaDevMgr2 aufrufen: IWiaDevMgr::RegisterEventCallbackCLSID oder IWiaDevMgr2::: RegisterEventCallbackCLSIDIWiaDevMgr::RegisterEventCallbackInterface oder IWiaDevMgr2::RegisterEventCallbackInterfaceIWiaDevMgr::RegisterEventCallbackProgram oder IWiaDevMgr2::RegisterEventCallbackProgram'
ms.assetid: 0c142083-835f-4bbd-ab32-eb6130f99c59
title: Registrieren von WIA-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e5f6409c8ac6af6f7bd82e43c34bef683a966fbd38d3ed35959ee9a4bc9c73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057030"
---
# <a name="registering-wia-events"></a>Registrieren von WIA-Ereignissen

Anwendungen können sich registrieren, um über Windows WIA-Hardwaregeräteereignisse (Image Acquisition) benachrichtigt zu werden, indem sie eine der folgenden [**IWiaDevMgr-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) oder [**IWiaDevMgr2-Schnittstellenmethoden**](-wia-iwiadevmgr2.md) aufrufen:

-   [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) oder [ **IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)
-   [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) oder [ **IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)
-   [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) oder [ **IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)

Alle diese Methoden verwenden Parameter, die das Ereignis und das Hardwaregerät angeben, für das die Anwendung benachrichtigt werden soll. Anwendungen registrieren sich, um ein Ereignis für alle WIA-Geräte zu empfangen, indem sie einen **NULL-Wert** für den Parameter übergeben, der das Hardwaregerät angibt.

Die **RegisterEventCallbackInterface-Methode** registriert eine Anwendung, um ein WIA-Hardwaregeräteereignis zu empfangen, wenn die Anwendung zum Zeitpunkt des Auftretens des Ereignisses ausgeführt wird. Wenn das Ereignis auftritt, für das die Anwendung registriert ist, ruft WIA die [**IWiaEventCallback::ImageEventCallback-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) des von der Anwendung bereitgestellten Objekts auf, um die Ereignisinformationen zu übertragen.

Die **RegisterEventCallbackCLSID-Methode** registriert eine Anwendung, die eine registrierte com-Komponente (Component Object Model) ist, um ein WIA-Hardwaregeräteereignis zu empfangen, auch wenn die Anwendung nicht ausgeführt wird. Zusätzlich zu den zuvor erwähnten Parametern verwendet diese Methode einen Parameter, *pClsID,* der die Klassen-ID der Anwendung angibt. Wenn das angegebene Ereignis auftritt, verwendet das WIA-System die [CoCreateInstance-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) und die von *pClsID* angegebene Klassen-ID, um eine neue Instanz der Anwendung zu erstellen, und ruft die [**IWiaEventCallback::ImageEventCallback-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) dieser Anwendung auf, um die Ereignisinformationen zu übertragen.

Die **RegisterEventCallbackProgram-Methode** registriert eine Anwendung, um ein WIA-Hardwaregeräteereignis zu empfangen, auch wenn die Anwendung beim Auftreten des Ereignisses nicht ausgeführt wird. Die Anwendung muss keine registrierte COM-Komponente sein. WIA startet die Anwendung mit einer Befehlszeilen-Anweisung. **RegisterEventCallbackProgram** verwendet den Parameter *bstrCommandline,* der den vollständigen Pfad und Dateinamen der ausführbaren Anwendung angibt. **RegisterEventCallbackProgram** ist aus Gründen der Abwärtskompatibilität mit Anwendungen vorhanden, die nicht für WIA geschrieben wurden und vermieden werden sollten. Verwenden Sie stattdessen **RegisterEventCallbackInterface** oder **RegisterEventCallbackCLSID.**

Um zu bestimmen, welche Handler für Ereignisse auf einem bestimmten WIA-Gerät registriert sind, ruft eine Anwendung die [**IWiaItem::EnumRegisterEventInfo-**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) oder [**IWiaItem2::EnumRegisterEventInfo-Methode**](-wia-iwiaitem2-enumregistereventinfo.md) eines Stammelements auf. Diese Methode erstellt ein Enumerationsobjekt für die Registrierungsinformationen. Die Anwendung kann dann die [**IEnumWIA \_ DEV \_ CAPS-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) dieses Objekts verwenden, um Informationen zu den Handlern aufzulisten, die zum Empfangen von Ereignissen für dieses Gerät registriert sind.

Wenn ein Ereignis auftritt, für das eine ausgeführte Anwendung über **RegisterEventCallbackInterface** und entweder **RegisterEventCallbackCLSID** oder **RegisterEventCallbackProgram** registriert wird, benachrichtigt WIA die ausgeführte Anwendung und versucht nicht, eine neue Instanz der Anwendung zu starten, da die Ereignisregistrierung über **RegisterEventCallbackInterface** Vorrang vor **RegisterEventCallbackCLSID** und **RegisterEventCallbackProgram** hat.

> [!Note]  
> In einer Multithreadanwendung gibt es keine Garantie dafür, dass der Thread, für den der Ereignisbenachrichtigungsrückruf zurückgegeben wird, derselbe Thread ist, der den Rückruf registriert hat.

 

 

 
