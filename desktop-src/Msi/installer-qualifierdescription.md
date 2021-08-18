---
description: Die schreibgeschützte QualifierDescription-Eigenschaft gibt eine Textzeichenfolge zurück, die die qualifizierte Komponente beschreibt.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Installer.QualifierDescription-Eigenschaft
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
ms.openlocfilehash: c226f00d7f95b4585fa4a0713fb281011079cdc35c4e421254beec75db84d7db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763580"
---
# <a name="installerqualifierdescription-property"></a>Installer.QualifierDescription-Eigenschaft

Die schreibgeschützte **QualifierDescription-Eigenschaft** gibt eine Textzeichenfolge zurück, die die qualifizierte Komponente beschreibt. Diese lokalisierbare Zeichenfolge wird in der Spalte AppData der [PublishComponent-Tabelle](publishcomponent-table.md) erstellt und kann dem Benutzer angezeigt werden. Der Qualifizierer unterscheidet mehrere Formen derselben Komponente, z. B. eine Komponente, die in mehreren Sprachen implementiert ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Qualifizierte Komponenten](qualified-components.md)
</dt> </dl>

 

 




