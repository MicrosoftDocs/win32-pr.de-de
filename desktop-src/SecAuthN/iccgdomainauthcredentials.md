---
description: Eine vom Client implementierte Schnittstelle, mit der Entwickler ihre eigenen Anmelde Informationen zur Laufzeit dynamisch bereitstellen können, um nicht mit der Domäne verbundene Container mit Active Directory zu authentifizieren.
title: Iccgdomainauth-Anmelde Informationen-Schnittstelle (ccgplugins. h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106366564"
---
# <a name="iccgdomainauthcredentials-interface"></a>Iccgdomainauth-Anmelde Informationen (Schnittstelle)

Eine vom Client implementierte Schnittstelle, mit der Entwickler ihre eigenen Anmelde Informationen zur Laufzeit dynamisch bereitstellen können, um nicht mit der Domäne verbundene Container mit Active Directory zu authentifizieren. 

## <a name="members"></a>Member

Die **iccgdomainauthanmelde** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iccgdomainauthanmeldeinformationen** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iccgdomainauthanmelde** -Schnittstelle verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Getpasswordanmelde Informationen**](iccgdomainauthcredentials-getpasswordcredentials.md)               | Gibt Anmelde Informationen zurück, um einen nicht in die Domäne eingebundenen Container mit Active Directory zu authentifizieren.<br/>                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>ccgplugins. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>ccgplugins. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ccgplugins.dll</dt> </dl> |
| IID<br/>                      | 6ecda518-2010-4437-8bc3-46e752b7b172<br/>          |



 

