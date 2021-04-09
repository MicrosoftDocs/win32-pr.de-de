---
description: Erstellt freigegebene Eigenschaften Gruppen und, um Zugriff auf vorhandene freigegebene Eigenschaften Gruppen zu erhalten.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: SharedPropertyGroupManager-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860976"
---
# <a name="sharedpropertygroupmanager-class"></a>SharedPropertyGroupManager-Klasse

Erstellt freigegebene Eigenschaften Gruppen und, um Zugriff auf vorhandene freigegebene Eigenschaften Gruppen zu erhalten.

Weitere Informationen zum Verwenden der freigegebenen Eigenschaften-Manager in com+ finden Sie unter [com+ Shared Eigenschaften-Manager](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|--------------------------------------------------------------------|
| CLSID      | CLSID \_ SharedPropertyGroupManager                                  |
| ProgID     | L "mtxspm. SharedPropertyGroupManager"                               |
| Schnittstellen | [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)zuzugreifen.

## <a name="remarks"></a>Bemerkungen

Um dieses Objekt zu erstellen, rufen Sie [**IObjectContext:: kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)auf.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu. Ein SharedPropertyGroupManager-Objekt kann mithilfe von "COMSVCSLIB. SharedPropertyGroupManager" als Klassenname deklariert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>"Comsvcs. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> </dl>

 

 




