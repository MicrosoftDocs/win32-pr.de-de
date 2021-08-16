---
description: Ermöglicht den Zugriff auf den Sicherheitskontext des aktuellen Aufrufs, der Informationen zu den Aufrufern eines Objekts enthält.
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: SecurityCallContext-Klasse (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: f0efa73ef704d77cc68b5a1193ccdc3de71b1ed0a5b8c730a2ea67474600bf5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546264"
---
# <a name="securitycallcontext-class"></a>SecurityCallContext-Klasse

Ermöglicht den Zugriff auf den Sicherheitskontext des aktuellen Aufrufs, der Informationen zu den Aufrufern eines Objekts enthält. Mit dieser Klasse können Sie auch herausfinden, ob der direkte Aufrufer eines Objekts Mitglied einer bestimmten Rolle ist und ob die Sicherheit für das Objekt aktiviert ist.

Nur COM+-Anwendungen, die rollenbasierte Sicherheit verwenden, können auf die **SecurityCallContext-Klasse** zugreifen. Weitere Informationen zu Rollen finden Sie unter [Rollenbasierte Sicherheitsverwaltung.](role-based-security-administration.md)

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|------------------------------------------------------|
| Schnittstellen | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)zuzugreifen.

## <a name="remarks"></a>Hinweise

Sie können kein **SecurityCallContext-Objekt** direkt erstellen. Um die Methoden von [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)zu verwenden, müssen Sie einen Verweis auf seine Implementierung abrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)aufrufen und IID \_ ISecurityCallContext für den *riid-Parameter* angeben.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die COM+-Diensttypbibliothek hinzu. Ein SecurityCallContext-Objekt kann mit "COMSVCSLib.SecurityCallContext" als Klassenname deklariert werden. Sie wird durch Aufrufen von [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[Programmgesteuerte Komponentensicherheit](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> <dt>

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

