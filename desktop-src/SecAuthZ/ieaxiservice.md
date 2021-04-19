---
description: Initialisiert ein-Systemdienst Objekt, um ein ActiveX-Objekt zu installieren, wenn der aktuelle Benutzer nicht über die Berechtigung zum Installieren des-Objekts verfügt.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Ieaxiservice-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363258"
---
# <a name="ieaxiservice-interface"></a>Ieaxiservice-Schnittstelle

Die **iaxiservice** -Schnittstelle initialisiert ein-Systemdienst Objekt, um ein ActiveX-Objekt zu installieren, wenn der aktuelle Benutzer nicht über die Berechtigung zum Installieren des-Objekts verfügt.

Diese Schnittstelle wird von der [**cieaxiinstallerservice**](cieaxiinstallerservice.md) -Klasse implementiert.

Diese Schnittstelle ist nicht in einem öffentlichen Header deklariert. Anwendungen müssen es selbst definieren. Das folgende IDL-Fragment (Interface Definition Language) beschreibt diese Schnittstelle, einschließlich ihrer IID.

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a>Member

Die **ieaxiservice** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ieaxiservice** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ieaxiservice** -Schnittstelle verfügt über diese Methoden.



| Methode                                        | BESCHREIBUNG                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [**Cleanup**](ieaxiservice-cleanup.md)       | Gibt die von der **ieaxiservice** -Schnittstelle verwendeten Ressourcen frei.<br/> |
| [**Initialisieren**](ieaxiservice-initialize.md) | Hiermit wird ein ActiveX-Objekt überprüft und heruntergeladen.<br/>                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ ieaxiservice ist definiert als E9E92380-9ecd-4982-A0EB-6815a56ccb27<br/>                           |



 

