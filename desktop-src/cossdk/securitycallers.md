---
description: Bietet Zugriff auf Informationen zu einzelnen Aufrufern in einer Auflistung von Aufrufern. Die Auflistung stellt die Kette der Aufrufe dar, die mit dem aktuellen Aufruf enden, und jeder Aufrufer in der Auflistung stellt die Identität eines Aufrufers dar.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: SecurityCallers-Klasse (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: a494e1421e443d2a6c3663bd7fa7c15eda898079477592e8df9958a2d5b87990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915894"
---
# <a name="securitycallers-class"></a>SecurityCallers-Klasse

Bietet Zugriff auf Informationen zu einzelnen Aufrufern in einer Auflistung von Aufrufern. Die Auflistung stellt die Kette der Aufrufe dar, die mit dem aktuellen Aufruf enden, und jeder Aufrufer in der Auflistung stellt die Identität eines Aufrufers dar. Nur Aufrufer, die eine Grenze überschreiten, an der die Sicherheit überprüft wird, sind in der Kette der Aufrufer enthalten. (In der COM+-Umgebung wird die Sicherheit an Anwendungsgrenzen überprüft.) Der Zugriff auf Informationen über die Identität eines bestimmten Aufrufers wird über die [**SecurityIdentity-Klasse,**](securityidentity.md) eine Identitätssammlung, bereitgestellt.

Nur COM+-Anwendungen, die rollenbasierte Sicherheit verwenden, können auf die **SecurityCallers-Klasse** zugreifen. Weitere Informationen zu Rollen finden Sie unter [Rollenbasierte Sicherheitsverwaltung.](role-based-security-administration.md)

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|------------------------------------------------------|
| Schnittstellen | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**ISecurityCallersColl zu zugreifen.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)

## <a name="remarks"></a>Hinweise

Sie können kein **SecurityCallers-Objekt direkt** erstellen. Um die Methoden von [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)zu verwenden, müssen Sie einen Verweis auf seine Implementierung abrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)aufrufen und IID ISecurityCallContext für den \_ *riid-Parameter* angeben. Rufen Sie als Nächstes [**ISecurityCallContext::get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) auf, um ein Kontextelement für einen Sicherheitsaufruf anfordern, das eine Sicherheitsidentitätssammlung ist (z. B. "DirectCaller" oder "OriginalCaller").

Um diese Klasse von Microsoft Visual Basic verwenden zu können, fügen Sie einen Verweis auf die COM+-Diensttypbibliothek hinzu. Sie können kein SecurityCallers-Objekt direkt erstellen. Um seine Eigenschaften verwenden zu können, müssen Sie mit [**getSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)eine Referenz auf die Implementierung abrufen. Rufen Sie als Nächstes die Item-Eigenschaft des -Objekts ab, und fordern Sie ein Kontextelement für einen Sicherheitsaufruf an, bei dem es sich um eine Sicherheitsidentitätssammlung handelt (z. B. "DirectCaller" oder "OriginalCaller").

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

[**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[Programmgesteuerte Komponentensicherheit](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallContext**](securitycallcontext.md)
</dt> <dt>

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

