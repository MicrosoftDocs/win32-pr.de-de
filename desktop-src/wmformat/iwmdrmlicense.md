---
title: IWMDRMLicense-Schnittstelle
description: Die IWMDRMLicense-Schnittstelle stellt eine Liste mit einer oder mehreren Lizenzen dar.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- IWMDRMLicense-Schnittstelle windows Medienformat
- IWMDRMLicense-Schnittstelle windows Media Format , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38aadbda7a0ab6e899e4100adb5ff03873a4dd683fcb8f5893c506033545d558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847127"
---
# <a name="iwmdrmlicense-interface"></a>IWMDRMLicense-Schnittstelle

Die **IWMDRMLicense-Schnittstelle** stellt eine Liste mit einer oder mehreren Lizenzen dar.

## <a name="members"></a>Member

Die **IWMDRMLicense-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMLicense** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMLicense-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                   | Beschreibung                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPersist**](iwmdrmlicense-canpersist.md)                                           | Fragt ab, ob die Lizenz in einem lokalen Lizenzspeicher beibehalten werden kann.<br/>                                                                                                                                               |
| [**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)                                 | Erstellt ein Entschlüsselungsobjekt mithilfe der Einstellungen der aktuellen Lizenz.<br/>                                                                                                                                                   |
| [**CreateEncryptor**](iwmdrmlicense-createencryptor.md)                                 | Erstellt ein Verschlüsselungsobjekt mithilfe der Einstellungen der aktuellen Lizenz.<br/>                                                                                                                                                  |
| [**CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md)                     | Erstellt ein sicheres Entschlüsselungsobjekt. Die sichere Entschlüsselung unterscheidet sich von der normalen Entschlüsselungsmethode darin, dass sie den Inhalt entschlüsselt und dann gemäß den in den Parametern dieser Methode angegebenen Einstellungen erneut verschlüsselt.<br/> |
| [**GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md) | Ruft alle analogen Videoeinschränkungen ab, die für die aktuelle Lizenz festgelegt sind.<br/>                                                                                                                                                     |
| [**GetInclusionList**](iwmdrmlicense-getinclusionlist.md)                               | Ruft die gesamte Aufnahmeliste für die aktuelle Lizenz oder Lizenzkette ab.<br/>                                                                                                                                           |
| [**GetLicense**](iwmdrmlicense-getlicense.md)                                           | Ruft die Lizenz als XML-Daten (Extensible Markup Language) oder XMR-Daten (Extensible Media Rights) ab.<br/>                                                                                                                        |
| [**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)                           | Ruft eine Eigenschaft aus der aktuellen Lizenz ab.<br/>                                                                                                                                                                          |
| [**GetNext**](iwmdrmlicense-getnext.md)                                                 | Lädt die Informationen zur nächsten Lizenz in der Liste.<br/>                                                                                                                                                               |
| [**GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md)             | Ruft Informationen zu allen Ausgabeschutzebenen (Output Protection Levels, OPLs) ab, die der Lizenz zugewiesen sind.<br/>                                                                                                                                |
| [**PersistLicense**](iwmdrmlicense-persistlicense.md)                                   | Speichert die aktuelle Lizenz aus dem temporären Speicher im permanenten lokalen Lizenzspeicher.<br/>                                                                                                                              |
| [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)                               | Setzt die Lizenzliste auf ihren ursprünglichen Zustand zurück.<br/>                                                                                                                                                                          |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> </dl>

 

