---
title: IWMDRMLicenseManagement-Schnittstelle
description: Die IWMDRMLicenseManagement-Schnittstelle stellt Methoden bereit, die allgemeine Vorgänge im Zusammenhang mit dem lokalen Lizenzspeicher ausführen. Rufen Sie IWMDRMProvider CreateObject auf, um eine Instanz dieser Schnittstelle abzurufen. Übergeben Sie IID \_ IWMDRMLicenseManagement als riid-Parameter.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- IWMDRMLicenseManagement-Schnittstelle windows Media Format
- IWMDRMLicenseManagement-Schnittstelle Windows Media Format , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63baeeb46baa877ccc294d1136351ec123d6c4661ee73d548b62d8cb4db05734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027548"
---
# <a name="iwmdrmlicensemanagement-interface"></a>IWMDRMLicenseManagement-Schnittstelle

Die **IWMDRMLicenseManagement-Schnittstelle** stellt Methoden bereit, die allgemeine Vorgänge im Zusammenhang mit dem lokalen Lizenzspeicher ausführen.

Rufen Sie [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md)auf, um eine Instanz dieser Schnittstelle abzurufen. Übergeben Sie **IID \_ IWMDRMLicenseManagement** als *riid-Parameter.*

## <a name="members"></a>Member

Die **IWMDRMLicenseManagement-Schnittstelle** erbt von [**IWMDRMEventGenerator.**](iwmdrmeventgenerator.md) **IWMDRMLicenseManagement** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMLicenseManagement-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                               | BESCHREIBUNG                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | Ruft asynchron eine Lizenz von einer angegebenen URL ab.<br/>                                                      |
| [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)                                     | Erstellt eine Sicherung der Lizenzen im lokalen Lizenzspeicher.<br/>                                                 |
| [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | Entfernt markierte Lizenzen aus dem Lizenzspeicher und defragmentiert den Speicher, um die Leistung zu verbessern.<br/>             |
| [**CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | Erstellt ein Lizenzenumeratorobjekt, das mit Lizenzinformationen auf der Grundlage von Parameterwerten aufgefüllt wird.<br/>            |
| [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | Generiert eine Lizenzsperrungsaufforderung.<br/>                                                                    |
| [**DeleteLicense**](iwmdrmlicensemanagement-deletelicense.md)                                       | Löscht eine Lizenz aus dem temporären lokalen Lizenzspeicher.<br/>                                                    |
| [**MonitorLicenseAcquisition**](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | Initiiert die Überwachung für einen Lizenzerwerbsprozess.<br/>                                                      |
| [**ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | Löscht eine Lizenz, die für Inhalte importiert wurde, die ursprünglich mit einem anderen Inhaltsschutzsystem geschützt wurden.<br/> |
| [**ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | Widerruft Lizenzen aus dem lokalen Lizenzspeicher.<br/>                                                               |
| [**RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md)                                   | Stellt zuvor sicherungslizenzen wieder her.<br/>                                                                      |
| [**StoreLicense**](iwmdrmlicensemanagement-storelicense.md)                                         | Fügt dem lokalen Lizenzspeicher eine Lizenz hinzu.<br/>                                                                   |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





