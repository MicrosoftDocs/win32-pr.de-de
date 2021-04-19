---
description: Geräte Attribute erfassen
ms.assetid: dd24671a-0689-4490-8d18-2a33ed461e9d
title: Geräte Attribute erfassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dd8dbcdf0a441ddb8a5ef2794526e961c22033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342797"
---
# <a name="capture-device-attributes"></a>Geräte Attribute erfassen

Die folgenden Attribute beziehen sich auf Erfassungsgeräte:



| Attribut                                                                                                                     | BESCHREIBUNG                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Anzeige Name für das MF- \_ devsource- \_ Attribut \_ \_](mf-devsource-attribute-friendly-name.md)                                          | Der Anzeige Name des Geräts.                                                          |
| [MF \_ devsource \_ - \_ Attribut \_ Medientyp](mf-devsource-attribute-media-type.md)                                                | Das Ausgabeformat des Geräts.                                                         |
| [Quelltyp des MF- \_ devsource- \_ Attributs \_ \_](mf-devsource-attribute-source-type.md)                                              | Der Typ des Geräts, z. b. Audioerfassung oder Video Erfassung.                         |
| [MF \_ devsource \_ - \_ Attribut \_ Quelltyp " \_ audcap"- \_ Endpunkt- \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md)     | Die Endpunkt-ID für ein audioerfassungs Gerät.                                        |
| [MF \_ devsource \_ - \_ Attribut \_ Quelltyp " \_ audcap \_ "-Rolle](mf-devsource-attribute-source-type-audcap-role.md)                    | Die Geräte Rolle für ein audioerfassungs-Gerät.                                        |
| [MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ Kategorie](mf-devsource-attribute-source-type-vidcap-category.md)            | Die Gerätekategorie für ein Videogerät.                                             |
| [MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ HW- \_ Quelle](mf-devsource-attribute-source-type-vidcap-hw-source.md)         | Gibt an, ob es sich bei einer Video Erfassungs Quelle um ein Hardware Gerät oder ein Software Gerät handelt. |
| [MF \_ devsource \_ - \_ Attribut \_ Quelltyp, \_ VidCap \_ Max. \_ Puffer](mf-devsource-attribute-source-type-vidcap-max-buffers.md)     | Gibt die maximale Anzahl von Frames an, die von der Video Erfassungs Quelle gepuffert werden.   |
| [MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ symbolische \_ Verknüpfung](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) | Die symbolische Verknüpfung für einen Video Erfassungs Treiber.                                       |
| [MFT- \_ HW- \_ Zeitstempel \_ mit \_ QPC- \_ Attribut](mft-hw-timestamp-with-qpc-attribute.md)                                           | Gibt an, ob die Geräte Quelle die Systemzeit für Zeitstempel verwendet.           |



 

Diese Attribute werden mit den folgenden Funktionen verwendet:

-   [**MF | atedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MF | atedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**Mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



