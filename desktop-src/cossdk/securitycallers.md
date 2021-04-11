---
description: Bietet Zugriff auf Informationen zu einzelnen Aufrufern in einer Auflistung von Aufrufern. Die Auflistung stellt die Kette der Aufrufe dar, die mit dem aktuellen aufrufenden, und jeder Aufrufer in der Auflistung stellt die Identität eines Aufrufers dar.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: SecurityCaller-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: c757b11bba6a30e8951915e1eace0811b6b6f732
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342189"
---
# <a name="securitycallers-class"></a>SecurityCaller-Klasse

Bietet Zugriff auf Informationen zu einzelnen Aufrufern in einer Auflistung von Aufrufern. Die Auflistung stellt die Kette der Aufrufe dar, die mit dem aktuellen aufrufenden, und jeder Aufrufer in der Auflistung stellt die Identität eines Aufrufers dar. Nur Aufrufer, die eine Grenze überschreiten, in der die Sicherheit geprüft wird, sind in der Kette der Aufru (In der com+-Umgebung wird die Sicherheit an den Anwendungsgrenzen geprüft.) Der Zugriff auf Informationen über die Identität eines bestimmten Aufrufers wird über die [**SecurityIdentity**](securityidentity.md) -Klasse, eine Identitäts Sammlung, bereitgestellt.

Nur com+-Anwendungen, die rollenbasierte Sicherheit verwenden, können auf die **SecurityCaller** -Klasse zugreifen. Weitere Informationen zu Rollen finden Sie unter Rollen [basierte Sicherheitsverwaltung](role-based-security-administration.md).

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|------------------------------------------------------|
| Schnittstellen | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)zuzugreifen.

## <a name="remarks"></a>Bemerkungen

Ein **SecurityCaller** -Objekt kann nicht direkt erstellt werden. Um die Methoden von [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)verwenden zu können, müssen Sie einen Verweis auf seine Implementierung abrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)aufrufen und IID \_ ISecurityCallContext für den *riid* -Parameter angeben. Rufen Sie als nächstes [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) auf, um ein Kontext Element für den Sicherheits Aufruf anzufordern, das eine Sammlung von Sicherheits Identitäten ist (z. b. "DirectCaller" oder "OriginalCaller").

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu. Ein SecurityCaller-Objekt kann nicht direkt erstellt werden. Um die zugehörigen Eigenschaften verwenden zu können, müssen Sie mithilfe von [**getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)eine referenzce zu ihrer Implementierung abrufen. Anschließend erhalten Sie die Item-Eigenschaft des-Objekts, das ein Kontext Element für den Sicherheits Aufruf anfordert, bei dem es sich um eine Sammlung von Sicherheits Identitäten handelt (z.b. "DirectCaller" oder "OriginalCaller").

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

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

