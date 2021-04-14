---
description: Bindet ein verwaltetes Objekt an eine Anwendungsdomäne. Hierbei handelt es sich um eine isolierte Umgebung, in der Anwendungen ausgeführt werden.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: AppDomainHelper-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523443"
---
# <a name="appdomainhelper-class"></a>AppDomainHelper-Klasse

Bindet ein verwaltetes Objekt an eine Anwendungsdomäne. Hierbei handelt es sich um eine isolierte Umgebung, in der Anwendungen ausgeführt werden.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ AppDomainHelper                                 |
| ProgID     | L "System. EnterpriseServices. Internal. AppDomainHelper" |
| Schnittstellen | [**Iappdomainhelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**iappdomainhelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)zuzugreifen.

## <a name="remarks"></a>Bemerkungen

Um dieses Objekt zu erstellen, rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)auf.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu. Ein AppDomainHelper-Objekt kann mithilfe von "COMSVCSLIB. AppDomainHelper" als Klassenname deklariert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>"Comsvcs. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iappdomainhelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

