---
title: Paket Abfrage-API
description: Erfahren Sie mehr über die Package Query-API, mit der Sie Informationen zu den App-Paketen erhalten, die auf dem System installiert sind. Jedes app-Paket enthält die Dateien, die eine Windows-App bilden, und eine Manifest-Datei, in der die Software für Windows beschrieben wird.
ms.assetid: EDDFC8B1-E224-4921-BED6-FC81711BA5BF
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5632edf661b4ea82177473bbb35f2674674500c6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038815"
---
# <a name="package-query-api"></a>Paket Abfrage-API

Erfahren Sie mehr über die Package Query-API, mit der Sie Informationen zu den App-Paketen erhalten, die auf dem System installiert sind. Jedes app-Paket enthält die Dateien, die eine Windows-App bilden, und eine Manifest-Datei, in der die Software für Windows beschrieben wird.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                 | BESCHREIBUNG                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Closepackageingefo**](/windows/desktop/api/AppModel/nf-appmodel-closepackageinfo)<br/>                                               | Schließt einen Verweis auf die angegebenen Paketinformationen.<br/>                                                                                              |
| [**Findpackagesbypackagefamily**](/windows/desktop/api/AppModel/nf-appmodel-findpackagesbypackagefamily)<br/>                         | Sucht die Pakete mit dem angegebenen Familiennamen für den aktuellen Benutzer. <br/>                                                                              |
| [**Formatapplicationusermodelid**](/windows/desktop/api/AppModel/nf-appmodel-formatapplicationusermodelid)<br/>                       | Erstellt eine [Anwendungs Benutzer Modell-ID](appx-packaging-glossary.md) aus dem Paket Familiennamen und der Paket relativen Anwendungs-ID (Praid). <br/> |
| [**Getapplicationusermodelid**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelid)<br/>                             | Ruft die [App-Benutzer Modell-ID](appx-packaging-glossary.md) für den angegebenen Prozess ab.<br/>                                                          |
| [**Getapplicationusermudelidfromtoken**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelidfromtoken)<br/>           | Ruft die [App-Benutzer Modell-ID](appx-packaging-glossary.md) für das angegebene Token ab.<br/>                                                            |
| [**Getcurrentapplicationusermodelid**](/windows/desktop/api/Appmodel/nf-appmodel-getcurrentapplicationusermodelid)<br/>               | Ruft die [App-Benutzer Modell-ID](appx-packaging-glossary.md) für den aktuellen Prozess ab.<br/>                                                            |
| [**Getcurrentpackagefamilyname**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefamilyname)<br/>                         | Ruft den Paket Familiennamen für den aufrufenden Prozess ab.<br/>                                                                                                 |
| [**Getcurrentpackagefullname**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefullname)<br/>                             | Ruft den vollständigen Namen des Pakets für den aufrufenden Prozess ab.<br/>                                                                                                   |
| [**Getcurrentpackageid**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageid)<br/>                                         | Ruft den Paket Bezeichner (ID) für den aufrufenden Prozess ab.<br/>                                                                                             |
| [**Getcurrentpackageingefo**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)<br/>                                     | Ruft die Paketinformationen für den aufrufenden Prozess ab.<br/>                                                                                                 |
| [**GetCurrentPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo2)<br/>                                     | Ruft die Paketinformationen für den aufrufenden Prozess mit der Option zum Angeben des Paket Ordner Typs ab.<br/>                                                                                               |
| [**Getcurrentpackagepath**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath)<br/>                                     | Ruft den Paketpfad für den aufrufenden Prozess ab.<br/>                                                                                                        |
| [**GetCurrentPackagePath2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath2)<br/>                                     | Ruft den Paketpfad für den aufrufenden Prozess mit der Option zum Angeben des Paket Ordner Typs ab.<br/>                                                                                                        |
| [**Getpackageapplicationids**](/windows/desktop/api/AppModel/nf-appmodel-getpackageapplicationids)<br/>                               | Ruft die IDs von apps im angegebenen Paket ab.<br/>                                                                                                        |
| [**Getpackagefamilyname**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilyname)<br/>                                       | Ruft den Paket Familiennamen für den angegebenen Prozess ab.<br/>                                                                                               |
| [**Getpackagefamilynamefromtoken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilynamefromtoken)<br/>                     | Ruft den Paket Familiennamen für das angegebene Token ab.<br/>                                                                                                 |
| [**Getpackagefullname**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullname)<br/>                                           | Ruft den vollständigen Paketnamen für den angegebenen Prozess ab.<br/>                                                                                                 |
| [**Getpackagefullnamefromtoken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullnamefromtoken)<br/>                         | Ruft den vollständigen Paketnamen für das angegebene Token ab.<br/>                                                                                                   |
| [**Getpackageid**](/windows/desktop/api/AppModel/nf-appmodel-getpackageid)<br/>                                                       | Ruft den Paket Bezeichner (ID) für den angegebenen Prozess ab.<br/>                                                                                           |
| [**Getpackageingefo**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)<br/>                                                   | Ruft die Paketinformationen für das angegebene Paket ab.<br/>                                                                                               |
| [**GetPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo2)<br/>                                                   | Ruft die Paketinformationen für das angegebene Paket ab, mit der Option zum Angeben des Paket Ordner Typs.<br/>                                                                                               |
| [**GetPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepath)<br/>                                                   | Ruft den Pfad für das angegebene Paket ab.<br/>                                                                                                              |
| [**Getpackagepathbyfullname**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname)<br/>                               | Ruft den Pfad des angegebenen Pakets ab.<br/>                                                                                                               |
| [**GetPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname2)<br/>                               | Ruft den Pfad des angegebenen Pakets mit der Option zum Angeben des Paket Ordner Typs ab.<br/>                                                                                                               |
| [**Getpackagesbypackagefamily**](/windows/desktop/api/AppModel/nf-appmodel-getpackagesbypackagefamily)<br/>                           | Ruft die Pakete mit dem angegebenen Familiennamen für den aktuellen Benutzer ab. <br/>                                                                               |
| [**Getstagedpackageorigin**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackageorigin)<br/>                                   | Ruft den Ursprung des angegebenen Pakets ab.<br/>                                                                                                             |
| [**Getstagedpackagepathbyfullname**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname)<br/>                   | Ruft den Pfad des angegebenen gestaffelten Pakets ab.<br/>                                                                                                        |
| [**GetStagedPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname2)<br/>                   | Ruft den Pfad des angegebenen gestaffelten Pakets mit der Option zum Angeben des Paket Ordner Typs ab.<br/>                                                                                                        |
| [**Openpackageinfobyfullname**](/windows/desktop/api/AppModel/nf-appmodel-openpackageinfobyfullname)<br/>                             | Öffnet die Paketinformationen des angegebenen Pakets.<br/>                                                                                               |
| [**Packagefamilynamefromfullname**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromfullname)<br/>                     | Ruft den Paket Familiennamen für den angegebenen vollständigen Namen des Pakets ab.<br/>                                                                                     |
| [**Packagefamilynamefromid**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromid)<br/>                                 | Ruft den Paket Familiennamen für den angegebenen Paket Bezeichner ab.<br/>                                                                                    |
| [**Packagefullnamefromid**](/windows/desktop/api/AppModel/nf-appmodel-packagefullnamefromid)<br/>                                     | Ruft den vollständigen Paketnamen für den angegebenen Paket Bezeichner (ID) ab.<br/>                                                                                 |
| [**Packageidfromfullname**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)<br/>                                     | Ruft den Paket Bezeichner (ID) für den vollständigen Namen des angegebenen Pakets ab.<br/>                                                                                 |
| [**Packagenameandpublisheridfromfamilyname**](/windows/desktop/api/AppModel/nf-appmodel-packagenameandpublisheridfromfamilyname)<br/> | Ruft den Paketnamen und den Verleger Bezeichner (ID) für den angegebenen Paket Familiennamen ab.<br/>                                                            |
| [**"Paramecationusermodelid"**](/windows/desktop/api/AppModel/nf-appmodel-parseapplicationusermodelid)<br/>                         | Dekonstruiert eine [Anwendungs Benutzer Modell-ID](appx-packaging-glossary.md) in den Paket Familiennamen und die zugehörige Paket relative Anwendungs-ID (Praid).<br/>      |
| [**Packageorigin**](/windows/desktop/api/AppModel/ne-appmodel-packageorigin)<br/>                                                     | Gibt den Ursprung eines Pakets an. <br/>                                                                                                                   |
| [**Identitäts Konstanten**](identity-constants.md)<br/>                                           | Gibt die Länge der Zeichen folgen für die Identitäts Felder des Pakets an.<br/>                                                                                |
| [**Paket Konstanten**](package-constants.md)<br/>                                             | Gibt an, wie Pakete verarbeitet werden sollen.<br/>                                                                                                           |
| [**Paket- \_ ID**](/windows/desktop/api/AppModel/ns-appmodel-package_id)<br/>                                                          | Stellt Paket Identifizierungs Informationen dar, z. b. Name, Version und Verleger.<br/>                                                                  |
| [**Paket \_ Informationen**](/windows/desktop/api/AppModel/ns-appmodel-package_info)<br/>                                                      | Stellt Paket Identifikationsinformationen dar, die den Paket Bezeichner, den vollständigen Namen und den Installationsort enthalten.<br/>                                  |
| [**Paket \_ Version**](/windows/desktop/api/AppModel/ns-appmodel-package_version)<br/>                                                | Stellt die Paket Versionsinformationen dar.<br/>                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzepte**
</dt> <dt>

[App-Pakete und-Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

[Glossar](appx-packaging-glossary.md)
</dt> <dt>

**Verweis**
</dt> <dt>

[App-Paketmanifestschema](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[Verpacken von APIs](interfaces.md)
</dt> <dt>

[Paketbereitstellungs-API](package-deployment-api.md)
</dt> </dl>

 

