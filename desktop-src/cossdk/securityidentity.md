---
description: Bietet Zugriff auf eine Auflistung von Sicherheitsinformationen, die die Identität eines Aufrufers darstellen. Mit dieser Klasse können Sie einen bestimmten Aufrufer in einer Kette von Aufrufern ermitteln, die Teil des Sicherheits Aufruf Kontexts ist.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: SecurityIdentity-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761556"
---
# <a name="securityidentity-class"></a>SecurityIdentity-Klasse

Bietet Zugriff auf eine Auflistung von Sicherheitsinformationen, die die Identität eines Aufrufers darstellen. Mit dieser Klasse können Sie einen bestimmten Aufrufer in einer Kette von Aufrufern ermitteln, die Teil des Sicherheits Aufruf Kontexts ist. Weitere Informationen zum Zugriff auf die Kontextinformationen von Sicherheits aufrufen finden Sie Unterprogramm gesteuerte Komponentensicherheit.

Nur com+-Anwendungen, die rollenbasierte Sicherheit verwenden, können auf die **SecurityIdentity** -Klasse zugreifen. Weitere Informationen zu Rollen finden Sie unter Rollen [basierte Sicherheitsverwaltung](role-based-security-administration.md).

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|--------------------------------------------------------|
| Schnittstellen | [**Isecurityidentitycoll**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**isecurityidentitycoll**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)zuzugreifen.

## <a name="remarks"></a>Bemerkungen

Sie können ein **SecurityIdentity** -Objekt nicht direkt erstellen. Um die Methoden von [**isecurityidentitycoll**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)verwenden zu können, müssen Sie einen Verweis auf seine Implementierung abrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)aufrufen und IID \_ ISecurityCallContext für den *riid* -Parameter angeben. Rufen Sie als nächstes [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) auf, um ein Kontext Element für den Sicherheits Aufruf anzufordern, das eine Sammlung von Sicherheits Identitäten ist (z. b. "DirectCaller" oder "OriginalCaller"). Rufen Sie dann [**isecurityidentitycoll:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) auf, um ein Sicherheits Identitätselement abzurufen (z. b. "Name" oder "AuthenticationService").

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu. Sie können ein SecurityIdentity-Objekt nicht direkt erstellen. Um die zugehörigen Eigenschaften verwenden zu können, müssen Sie mithilfe von [**getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)eine referenzce zu ihrer Implementierung abrufen. Anschließend erhalten Sie die Item-Eigenschaft des-Objekts, das ein Kontext Element für den Sicherheits Aufruf anfordert, bei dem es sich um eine Sammlung von Sicherheits Identitäten handelt (z.b. "DirectCaller" oder "OriginalCaller"). Verwenden Sie dann die Item-Eigenschaft des SecurityIdentity-Objekts, um ein Sicherheits Identitätselement abzurufen (z. b. "Name" oder "AuthenticationService").

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>"Comsvcs. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallContext**](securitycallcontext.md)
</dt> <dt>

[**SecurityCaller**](securitycallers.md)
</dt> </dl>

 

