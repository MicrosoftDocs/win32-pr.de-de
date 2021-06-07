---
description: Eine vom Client implementierte Schnittstelle, mit der Entwickler ihre eigenen Anmeldeinformationen dynamisch zur Laufzeit angeben können, um nicht in die Domäne beigetretene Container mit Active Directory zu authentifizieren.
title: ICcgDomainAuthCredentials-Schnittstelle (ccgplugins.h)
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
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387805"
---
# <a name="iccgdomainauthcredentials-interface"></a>ICcgDomainAuthCredentials-Schnittstelle

Eine vom Client implementierte Schnittstelle, mit der Entwickler ihre eigenen Anmeldeinformationen dynamisch zur Laufzeit angeben können, um nicht in die Domäne beigetretene Container mit Active Directory zu authentifizieren. 

## <a name="members"></a>Member

Die **ICcgDomainAuthCredentials-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ICcgDomainAuthCredentials** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ICcgDomainAuthCredentials-Schnittstelle** verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetPasswordCredentials**](iccgdomainauthcredentials-getpasswordcredentials.md)               | Gibt Anmeldeinformationen zurück, um einen nicht in die Domäne beigetretenen Container bei Active Directory zu authentifizieren.<br/>                                                              |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>ccgplugins.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>ccgplugins.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ccgplugins.dll</dt> </dl> |
| IID<br/>                      | 6ecda518-2010-4437-8bc3-46e752b7b172<br/>          |



 

