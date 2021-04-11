---
description: Legt den Wert einer freigegebenen Eigenschaft fest oder ruft ihn ab.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: SharedProperty-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126578"
---
# <a name="sharedproperty-class"></a>SharedProperty-Klasse

Legt den Wert einer freigegebenen Eigenschaft fest oder ruft ihn ab.

Allgemeine Informationen zum Verwenden der freigegebenen Eigenschaften-Manager in com+ finden Sie unter [com+ Shared Eigenschaften-Manager](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|--------------------------------------------|
| Schnittstellen | [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)zuzugreifen.

## <a name="remarks"></a>Bemerkungen

Sie können ein **SharedProperty** -Objekt erstellen, indem Sie die Methoden " [**kreateproperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) " oder " [**kreatepropertybyposition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) " von " [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)" verwenden.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu. Ein SharedProperty-Objekt wird erstellt, indem die [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) -Methode oder die [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) -Methode des [**SharedPropertyGroup**](sharedpropertygroup.md) -Objekts aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>"Comsvcs. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> <dt>

[**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




