---
description: Legt den Wert einer freigegebenen Eigenschaft fest oder ruft sie ab.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: SharedProperty-Klasse (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: 9b0daa74c7329f8dc9f2566852d863715d22fd556ce3d4674dfaf246c17504b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915770"
---
# <a name="sharedproperty-class"></a>SharedProperty-Klasse

Legt den Wert einer freigegebenen Eigenschaft fest oder ruft sie ab.

Allgemeine Informationen zur Verwendung von Shared Eigenschaften-Manager in COM+ finden Sie unter [COM+ Shared Eigenschaften-Manager](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|--------------------------------------------|
| Schnittstellen | [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**ISharedProperty zu zugreifen.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)

## <a name="remarks"></a>Hinweise

Sie können ein **SharedProperty-Objekt** erstellen, indem Sie die [**Methoden CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) oder [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) von [**ISharedPropertyGroup verwenden.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)

Um diese Klasse aus Microsoft Visual Basic, fügen Sie einen Verweis auf die COM+-Diensttypbibliothek hinzu. Ein SharedProperty-Objekt wird durch Aufrufen der [**Methoden CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) oder [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) des [**SharedPropertyGroup-Objekts**](sharedpropertygroup.md) erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> <dt>

[**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




