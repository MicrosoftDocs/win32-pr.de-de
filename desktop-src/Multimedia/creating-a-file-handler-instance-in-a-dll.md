---
title: Erstellen einer File-Handler-Instanz in einer DLL
description: Erstellen einer File-Handler-Instanz in einer DLL
ms.assetid: 0cf7ef72-c675-4a67-97b3-18cccfb7ddc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0023de28f660473a1747ff05528ec5360674754b5c0bcd34f5ae3a28cc39412f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144753"
---
# <a name="creating-a-file-handler-instance-in-a-dll"></a>Erstellen einer File-Handler-Instanz in einer DLL

Wenn eine Anwendung Die Dateihandler-DLL oder den Streamhandler angibt, sucht das System sie anhand ihres Klassenbezeichners in der Registrierung und wird geladen. Das System ruft dann die [**DllGetClassObject-Funktion**](/previous-versions//dd797891(v=vs.85)) der DLL auf, um eine Instanz der Datei oder des Streamhandlers zu erstellen. Das folgende (in C++geschriebene) Beispiel zeigt, wie ein Dateihandler eine -Instanz erstellt.


```C++
// Main DLL entry point. 
STDAPI DllGetClassObject(const CLSID FAR& rclsid, 
    const IID FAR& riid, void FAR* FAR* ppv) 
{ 
    HRESULT hresult; 
    hresult = CAVIFileCF::Create(rclsid, riid, ppv); 
    return hresult; 
} 
HRESULT CAVIFileCF::Create(const CLSID FAR&   rclsid, 
    const IID FAR& riid, void FAR* FAR*   ppv) 
{ 
// The following is the class factory creation and not an 
// actual PAVIFile. 
    CAVIFileCF FAR*   pAVIFileCF; 
    IUnknown FAR*   pUnknown; 
    HRESULT hresult; 
 
// Create the instance. 
    pAVIFileCF = new FAR CAVIFileCF(rclsid, &pUnknown); 
    if (pAVIFileCF == NULL) 
        return ResultFromScode(E_OUTOFMEMORY); 
 
// Set the interface pointer. 
    hresult = pUnknown->QueryInterface(riid, ppv); 
    if (FAILED(GetScode(hresult))) 
        delete pAVIFileCF; 
    return hresult; 
} 

```



 

 