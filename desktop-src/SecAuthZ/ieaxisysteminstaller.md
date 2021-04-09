---
description: Installiert ein ActiveX-Objekt.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Ieaxisysteminstaller-Schnittstelle
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
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050383"
---
# <a name="ieaxisysteminstaller-interface"></a>Ieaxisysteminstaller-Schnittstelle

Die **ieaxisysteminstaller** -Schnittstelle installiert ein ActiveX-Objekt.

Diese Schnittstelle ist nicht in einem öffentlichen Header deklariert. Anwendungen müssen es selbst definieren. Das folgende IDL-Fragment (Interface Definition Language) beschreibt diese Schnittstelle, einschließlich ihrer IID.

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

Die **ieaxisysteminstaller** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ieaxisysteminstaller** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ieaxisysteminstaller** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**Initializesysteminstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | Installiert das angegebene ActiveX-Objekt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ ieaxisysteminstaller ist als a50ea6f8-4764-4299-b309-022b2a8b4d8d definiert.<br/>                   |



 

