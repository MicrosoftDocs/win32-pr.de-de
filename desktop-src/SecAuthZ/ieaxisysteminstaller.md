---
description: Installiert ein ActiveX Objekt.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: IeAxiSystemInstaller-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: fb462c4b4f8fc28d9d00de230dea1bbd3670c4fb6eaa962d59875b4fd9054c8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671010"
---
# <a name="ieaxisysteminstaller-interface"></a>IeAxiSystemInstaller-Schnittstelle

Die **IeAxiSystemInstaller-Schnittstelle** installiert ein ActiveX Objekt.

Diese Schnittstelle wird nicht in einem öffentlichen Header deklariert. Anwendungen müssen sie selbst definieren. Das folgende IDL-Fragment (Interface Definition Language) beschreibt diese Schnittstelle, einschließlich ihrer IID.

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a>Member

Die **IeAxiSystemInstaller-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiSystemInstaller** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IeAxiSystemInstaller-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                              | Beschreibung                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**InitializeSystemInstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | Installiert das angegebene ActiveX Objekt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller ist als a50ea6f8-4764-4299-b309-022b2a8b4d8d definiert.<br/>                   |



 

