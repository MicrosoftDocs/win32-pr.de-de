---
description: Erstellt freigegebene Eigenschaftengruppen und , um Zugriff auf vorhandene freigegebene Eigenschaftengruppen zu erhalten.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: SharedPropertyGroupManager-Klasse (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: ac05dcc813192a9ea1bf1f1f4e5ad63ed72eca6874de855ac3f4582af51680f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120360"
---
# <a name="sharedpropertygroupmanager-class"></a>SharedPropertyGroupManager-Klasse

Erstellt freigegebene Eigenschaftengruppen und , um Zugriff auf vorhandene freigegebene Eigenschaftengruppen zu erhalten.

Weitere Informationen zur Verwendung von Shared Eigenschaften-Manager in COM+ finden Sie unter [COM+ Shared Eigenschaften-Manager](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|--------------------------------------------------------------------|
| CLSID      | CLSID \_ SharedPropertyGroupManager                                  |
| ProgID     | L"MTxSpm.SharedPropertyGroupManager"                               |
| Schnittstellen | [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**ISharedPropertyGroupManager zu zugreifen.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)

## <a name="remarks"></a>Hinweise

Rufen Sie zum Erstellen dieses Objekts [**IObjectContext::CreateInstance auf.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)

Um diese Klasse aus Microsoft Visual Basic, fügen Sie einen Verweis auf die COM+-Diensttypbibliothek hinzu. Ein SharedPropertyGroupManager-Objekt kann mit "COMSVCSLib.SharedPropertyGroupManager" als Klassenname deklariert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> </dl>

 

 




