---
description: Ermöglicht den Zugriff auf eine Auflistung von Sicherheitsinformationen, die die Identität eines Aufrufers darstellen. Mit dieser Klasse können Sie einen bestimmten Aufrufer in einer Kette von Aufrufern herausfinden, die Teil des Sicherheitsaufrufkontexts ist.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: SecurityIdentity-Klasse (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: d16139ccf60a22ebfb4cf609e734e0b8df3285ef9ddb1804657313900a3ea05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305476"
---
# <a name="securityidentity-class"></a>SecurityIdentity-Klasse

Ermöglicht den Zugriff auf eine Auflistung von Sicherheitsinformationen, die die Identität eines Aufrufers darstellen. Mit dieser Klasse können Sie einen bestimmten Aufrufer in einer Kette von Aufrufern herausfinden, die Teil des Sicherheitsaufrufkontexts ist. Weitere Informationen zum Zugriff auf Kontextinformationen für Sicherheitsaufrufe finden Sie unter Programmgesteuerte Komponentensicherheit.

Nur COM+-Anwendungen, die rollenbasierte Sicherheit verwenden, können auf die **SecurityIdentity-Klasse** zugreifen. Weitere Informationen zu Rollen finden Sie unter [Rollenbasierte Sicherheitsverwaltung.](role-based-security-administration.md)

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|--------------------------------------------------------|
| Schnittstellen | [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**ISecurityIdentityColl zu zugreifen.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)

## <a name="remarks"></a>Hinweise

Sie können ein **SecurityIdentity-Objekt nicht direkt** erstellen. Um die Methoden von [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)zu verwenden, müssen Sie einen Verweis auf seine Implementierung abrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)aufrufen und IID ISecurityCallContext für den \_ *riid-Parameter* angeben. Rufen Sie als Nächstes [**ISecurityCallContext::get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) auf, um ein Kontextelement für einen Sicherheitsaufruf anfordern, das eine Sicherheitsidentitätssammlung ist (z. B. "DirectCaller" oder "OriginalCaller"). Rufen Sie dann [**ISecurityIdentityColl::get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) auf, um ein Sicherheitsidentitätselement abzurufen (z. B. "Name" oder "AuthenticationService").

Um diese Klasse von Microsoft Visual Basic verwenden zu können, fügen Sie einen Verweis auf die COM+-Diensttypbibliothek hinzu. Sie können ein SecurityIdentity-Objekt nicht direkt erstellen. Um seine Eigenschaften verwenden zu können, müssen Sie mit [**getSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)eine Referenz auf die Implementierung abrufen. Rufen Sie als Nächstes die Item-Eigenschaft des -Objekts ab, und fordern Sie ein Kontextelement für einen Sicherheitsaufruf an, bei dem es sich um eine Sicherheitsidentitätssammlung handelt (z. B. "DirectCaller" oder "OriginalCaller"). Verwenden Sie dann die Item-Eigenschaft des SecurityIdentity-Objekts, um ein Sicherheitsidentitätselement abzurufen (z. B. "Name" oder "AuthenticationService").

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

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

[**SecurityCallers**](securitycallers.md)
</dt> </dl>

 

