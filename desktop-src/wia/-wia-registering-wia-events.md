---
description: 'Anwendungen können sich registrieren, um über die Windows-Abbild Erfassung (WIA) Hardware Geräte Ereignisse benachrichtigt zu werden, indem Sie eine der folgenden iwiadevmgr-oder IWiaDevMgr2-Schnittstellen Methoden aufrufen: iwiadevmgr:: registereventcallbackclsid oder IWiaDevMgr2:: registereventcallbackclsidiwiadevmgr:: registereventcallbackinterface oder IWiaDevMgr2:: registereventcallbackinterfakeiwiadevmgr:: registereventcallbackprogram oder IWiaDevMgr2:: registereventcallbackprogram'
ms.assetid: 0c142083-835f-4bbd-ab32-eb6130f99c59
title: Registrieren von WIA-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9fc36540a64211428579bc13b84902490ea103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958964"
---
# <a name="registering-wia-events"></a>Registrieren von WIA-Ereignissen

Anwendungen können sich registrieren, um über die Windows-Abbild Erfassung (WIA) Hardware Geräte Ereignisse benachrichtigt zu werden, indem Sie eine der folgenden [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) -Schnittstellen Methoden aufrufen:

-   [**Iwiadevmgr:: registereventcallbackclsid**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) oder [ **IWiaDevMgr2:: registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md)
-   [**Iwiadevmgr:: registereventcallbackinterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) oder [ **IWiaDevMgr2:: registereventcallbackinterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)
-   [**Iwiadevmgr:: registereventcallbackprogram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) oder [ **IWiaDevMgr2:: registereventcallbackprogram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)

Alle diese Methoden akzeptieren Parameter, mit denen das Ereignis und das Hardware Gerät angegeben werden, für das die Anwendung benachrichtigt werden soll. Anwendungen registrieren sich für den Empfang eines Ereignisses für alle WIA-Geräte, indem Sie einen **null** -Wert für den Parameter übergeben, der das Hardware Gerät angibt.

Mit der **registereventcallbackinterface** -Methode wird eine Anwendung zum Empfangen eines WIA-Hardware Geräte Ereignisses registriert, wenn die Anwendung zum Zeitpunkt des Ereignisses ausgeführt wird. Wenn das Ereignis, für das die Anwendung registriert ist, auftritt, ruft WIA die [**iwiaeventcallback:: imageeventcallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) -Methode des von der Anwendung bereitgestellten Objekts auf, um die Ereignis Informationen zu übertragen.

Mit der **registereventcallbackclsid** -Methode wird eine Anwendung registriert, bei der es sich um eine registrierte Component Object Model COM-Komponente handelt, um ein WIA-Hardware Geräte Ereignis zu empfangen, auch wenn die Anwendung nicht ausgeführt wird. Zusätzlich zu den zuvor erwähnten Parametern nimmt diese Methode den Parameter *pclsid* an, der die Klassen-ID der Anwendung angibt. Wenn das angegebene Ereignis auftritt, verwendet das WIA-System die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion und die von *pclsid* angegebene Klassen-ID, um eine neue Instanz der Anwendung zu erstellen, und ruft die [**iwiaeventcallback:: imageeventcallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) -Methode dieser Anwendung auf, um die Ereignis Informationen zu übertragen.

Mit der **registereventcallbackprogram** -Methode wird eine Anwendung zum Empfangen eines WIA-Hardware Geräte Ereignisses registriert, auch wenn die Anwendung nicht ausgeführt wird, wenn das Ereignis eintritt. Die Anwendung muss keine registrierte COM-Komponente sein. WIA wird die Anwendung mit einer Befehlszeilen Anweisung gestartet. **Registereventcallbackprogram** übernimmt den Parameter *bstrincommandline*, der den vollständigen Pfad und den Dateinamen der ausführbaren Anwendung angibt. **Registereventcallbackprogram** ist für die Abwärtskompatibilität mit Anwendungen vorhanden, die nicht für WIA geschrieben wurden, und sollte vermieden werden. Verwenden Sie stattdessen **registereventcallbackinterface** oder **registereventcallbackclsid** .

Um zu ermitteln, welche Handler für Ereignisse auf einem bestimmten WIA-Gerät registriert sind, ruft eine Anwendung eine [**iwiaitem:: enumregistereventinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) -Methode oder [**IWiaItem2:: enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md) -Methode eines Stamm Elements auf. Diese Methode erstellt ein Enumerationsobjekt für die Registrierungsinformationen. Die Anwendung kann dann die [**ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) -Schnittstelle dieses Objekts verwenden, um Informationen zu den Handlern aufzuzählen, die für den Empfang von Ereignissen für dieses Gerät registriert sind.

Wenn ein Ereignis auftritt, für das eine laufende Anwendung über **registereventcallbackinterface** und entweder **registereventcallbackclsid** oder **registereventcallbackprogram** registriert wird, WIA benachrichtigt die laufende Anwendung und versucht nicht, eine neue Instanz der Anwendung zu starten, da die Ereignis Registrierung über **registereventcallbackinterface** Vorrang vor " **registereventcallbackclsid** " und " **registereventcallbackprogram**" hat.

> [!Note]  
> In einer Multithreadanwendung gibt es keine Garantie dafür, dass der Thread, den der Ereignis Benachrichtigungs Rückruf zurückgibt, derselbe Thread ist, der den Rückruf registriert hat.

 

 

 
