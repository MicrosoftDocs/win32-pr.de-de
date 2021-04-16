---
title: Iwmdrmlicense-Schnittstelle
description: Die iwmdrmlicense-Schnittstelle stellt eine Liste mit mindestens einer Lizenz dar.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Iwmdrmlicense-Schnittstelle Windows Media-Format
- Iwmdrmlicense-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473580"
---
# <a name="iwmdrmlicense-interface"></a>Iwmdrmlicense-Schnittstelle

Die **iwmdrmlicense** -Schnittstelle stellt eine Liste mit mindestens einer Lizenz dar.

## <a name="members"></a>Member

Die **iwmdrmlicense** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmdrmlicense** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmlicense** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Canpersistent**](iwmdrmlicense-canpersist.md)                                           | Fragt ab, ob die Lizenz in einem lokalen Lizenz Speicher persistent gespeichert werden kann.<br/>                                                                                                                                               |
| [**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)                                 | Erstellt ein Entschlüsselungsobjekt mit den Einstellungen der aktuellen Lizenz.<br/>                                                                                                                                                   |
| [**CreateEncryptor**](iwmdrmlicense-createencryptor.md)                                 | Erstellt ein Verschlüsselungs Objekt mit den Einstellungen der aktuellen Lizenz.<br/>                                                                                                                                                  |
| [**"Kreatesecuredecryptor"**](iwmdrmlicense-createsecuredecryptor.md)                     | Erstellt ein sicheres Entschlüsselungs-Objekt. Der sichere entschlüsselungstyp unterscheidet sich vom normalen entschlüsselungstyp darin, dass er den Inhalt entschlüsselt und dann gemäß den in den Parametern dieser Methode angegebenen Einstellungen erneut verschlüsselt.<br/> |
| [**Getanalogvideorestrictionlevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md) | Ruft alle analogen Video Einschränkungen ab, die für die aktuelle Lizenz festgelegt sind.<br/>                                                                                                                                                     |
| [**Getinclusionlist**](iwmdrmlicense-getinclusionlist.md)                               | Ruft die gesamte Inklusions Liste für die aktuelle Lizenz oder Lizenz Kette ab.<br/>                                                                                                                                           |
| [**GetLicense**](iwmdrmlicense-getlicense.md)                                           | Ruft die Lizenz als Extensible Markup Language (XML) oder XMR-Daten (Extensible Media Rights) ab.<br/>                                                                                                                        |
| [**Getliceneinproperty**](iwmdrmlicense-getlicenseproperty.md)                           | Ruft eine Eigenschaft aus der aktuellen Lizenz ab.<br/>                                                                                                                                                                          |
| [**GetNext**](iwmdrmlicense-getnext.md)                                                 | Lädt die Informationen über die nächste Lizenz in der Liste.<br/>                                                                                                                                                               |
| [**Getoutputschutzlevels**](iwmdrmlicense-getoutputprotectionlevels.md)             | Ruft Informationen zu allen Ausgabe Schutz Ebenen (opls) ab, die der Lizenz zugewiesen sind.<br/>                                                                                                                                |
| [**Persistlicense**](iwmdrmlicense-persistlicense.md)                                   | Speichert die aktuelle Lizenz aus dem temporären Speicher im permanenten lokalen Lizenz Speicher.<br/>                                                                                                                              |
| [**Retenumeration**](iwmdrmlicense-resetenumeration.md)                               | Setzt die Lizenz Liste auf den ursprünglichen Zustand zurück.<br/>                                                                                                                                                                          |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> </dl>

 

