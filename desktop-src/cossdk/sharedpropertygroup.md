---
description: Erstellt und greift auf die freigegebenen Eigenschaften in einer freigegebenen Eigenschaften Gruppe zu.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: SharedPropertyGroup-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748169"
---
# <a name="sharedpropertygroup-class"></a>SharedPropertyGroup-Klasse

Erstellt und greift auf die freigegebenen Eigenschaften in einer freigegebenen Eigenschaften Gruppe zu.

Weitere Informationen zum Verwenden der freigegebenen Eigenschaften-Manager in com+ finden Sie unter [com+ Shared Eigenschaften-Manager](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|------------------------------------------------------|
| Schnittstellen | [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)zuzugreifen.

## <a name="remarks"></a>Bemerkungen

Sie können ein **SharedPropertyGroup** -Objekt mithilfe der Methode " [**kreatepropertygroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) " von [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)erstellen.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu. Ein SharedPropertyGroup-Objekt wird erstellt, indem die [**createpropertygroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) -Methode des [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) -Objekts aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>"Comsvcs. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




