---
title: Iwmdrmlicensequery-Schnittstelle
description: Die iwmdrmlicensequery-Schnittstelle ermöglicht es Anwendungen, die Rechte und den Lizenzstatus für eine geschützte Datei abzufragen.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Iwmdrmlicensequery-Schnittstelle Windows Media-Format
- Iwmdrmlicensequery Interface Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728713"
---
# <a name="iwmdrmlicensequery-interface"></a>Iwmdrmlicensequery-Schnittstelle

Die **iwmdrmlicensequery** -Schnittstelle ermöglicht es Anwendungen, die Rechte und den Lizenzstatus für eine geschützte Datei abzufragen. Diese Schnittstelle verwendet die Schlüssel-ID, um Abfragen für den lokalen Lizenz Speicher auszuführen.

Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf. Übergeben Sie **IID \_ iwmdrmlicensequery** als *riid* -Parameter.

## <a name="members"></a>Member

Die **iwmdrmlicensequery** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmdrmlicensequery** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmlicensequery** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                | BESCHREIBUNG                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Queryaktionallowed**](iwmdrmlicensequery-queryactionallowed.md)                   | Fragt den lokalen Lizenz Speicher nach Berechtigungen zum Ausführen von Aktionen anhand der Schlüssel-ID ab.<br/>         |
| [**Querylicenenstate**](iwmdrmlicensequery-querylicensestate.md)                     | Fragt den lokalen Lizenz Speicher nach den Lizenz Zustandsdaten anhand der Schlüssel-ID und spezifischer Rechte ab.<br/> |
| [**"Mentactionzugewiesene wedqueryparams"**](iwmdrmlicensequery-setactionallowedqueryparams.md) | Legt Umgebungsparameter fest, um die Genauigkeit von Lizenz Abfragen zu verbessern.<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Die Methoden von **iwmdrmlicensequery** bieten keine Informationen zu einzelnen Lizenzen. Stattdessen werden die Lizenzdaten durch das DRM-Subsystem aggregiert, bevor die Abfrageergebnisse zurückgegeben werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> </dl>

 

