---
description: Die schreibgeschützte qualifierdescription-Eigenschaft gibt eine Text Zeichenfolge zurück, in der die qualifizierte Komponente beschrieben wird.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Installer. qualifierdescription (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365626"
---
# <a name="installerqualifierdescription-property"></a>Installer. qualifierdescription (Eigenschaft)

Die schreibgeschützte **qualifierdescription** -Eigenschaft gibt eine Text Zeichenfolge zurück, in der die qualifizierte Komponente beschrieben wird. Diese lokalisierbare Zeichenfolge wird in der APPDATA-Spalte der [PublishComponent-Tabelle](publishcomponent-table.md) erstellt und kann für den Benutzer angezeigt werden. Der Qualifizierer unterscheidet mehrere Formen derselben Komponente, z. b. eine Komponente, die in mehreren Sprachen implementiert ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msienumschlag componentqualifizierer**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Qualifizierte Komponenten](qualified-components.md)
</dt> </dl>

 

 




