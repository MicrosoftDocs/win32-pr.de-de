---
description: Initialisiert ein Systemdienstobjekt, um ein ActiveX-Objekt zu installieren, wenn der aktuelle Benutzer nicht über die Berechtigung zum Installieren des Objekts verfügt.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: IeAxiService-Schnittstelle
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
ms.openlocfilehash: f799b0b306d10e8246afbef83e4677729f6a735a52e5e4ed4954b873ec5b6201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414720"
---
# <a name="ieaxiservice-interface"></a>IeAxiService-Schnittstelle

Die **IAxiService-Schnittstelle** initialisiert ein Systemdienstobjekt, um ein ActiveX-Objekt zu installieren, wenn der aktuelle Benutzer nicht über die Berechtigung zum Installieren des Objekts verfügt.

Die [**CIeAxiInstallerService-Klasse**](cieaxiinstallerservice.md) implementiert diese Schnittstelle.

Diese Schnittstelle wird nicht in einem öffentlichen Header deklariert. Anwendungen müssen sie selbst definieren. Das folgende IDL-Fragment (Interface Definition Language) beschreibt diese Schnittstelle, einschließlich ihrer IID.

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

Die **IeAxiService-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiService** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IeAxiService-Schnittstelle** verfügt über diese Methoden.



| Methode                                        | Beschreibung                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [**Bereinigen**](ieaxiservice-cleanup.md)       | Gibt die von der **IeAxiService-Schnittstelle** verwendeten Ressourcen frei.<br/> |
| [**Initialisieren**](ieaxiservice-initialize.md) | Überprüft ein ActiveX-Objekt und lädt es herunter.<br/>                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService ist als E9E92380-9ECD-4982-A0EB-6815A56CCF27 definiert.<br/>                           |



 

