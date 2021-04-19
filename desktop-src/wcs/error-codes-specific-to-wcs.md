---
title: WCS-spezifische Fehlercodes
description: Im folgenden finden Sie eine Liste der Fehlercodes, die speziell mit der Verwendung von WCS 1,0 verknüpft sind.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3040f462ce226ebd3018070abc818884cee6ad6
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "106367257"
---
# <a name="error-codes-specific-to-wcs"></a>WCS-spezifische Fehlercodes

Im folgenden finden Sie eine Liste der Fehlercodes, die speziell mit der Verwendung von WCS 1,0 verknüpft sind. Dies bedeutet nicht, dass WCS-Funktionen nur diese Fehlercodes zurückgeben. Dies bedeutet, dass die Codes in der folgenden Tabelle nur von WCS-Funktionen zurückgegeben werden. Sie können auch andere Win32-Fehlercodes zurückgeben, die an anderer Stelle in der Win32-API des Platform SDK dokumentiert sind.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>Fehler beim \_ Löschen von \_ ICM \_ XForm.
</dt> <dd>

Die angegebene Farb Transformation konnte nicht gelöscht werden.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>Fehler \_ doppeltes \_ Tag
</dt> <dd>

Das angegebene Farbprofil-Elementtag ist im Farbprofil bereits vorhanden.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ICM-Fehler ist \_ \_ nicht \_ aktiviert.
</dt> <dd>

Die Abbild Farbverwaltung ist zurzeit nicht aktiviert.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>\_ungültiger \_ CMM-Fehler.
</dt> <dd>

Der angegebene Dateiname verweist nicht auf ein gültiges Farb Verwaltungsmodul.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>\_ungültiger \_ colorspace-Fehler.
</dt> <dd>

Der angegebene Farbraum ist ungültig.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>Fehler \_ ungültiges \_ Profil.
</dt> <dd>

Der angegebene Dateiname verweist nicht auf ein gültiges Farbprofil.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>Fehler \_ ungültige \_ Transformation 
</dt> <dd>

Die angegebene Farb Transformation ist keine gültige Farb Transformation.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>das Fehler \_ Profil ist \_ nicht \_ \_ mit dem \_ Gerät verknüpft.
</dt> <dd>

Das angegebene Farbprofil ist keinem Gerät zugeordnet.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>Fehler \_ Profil wurde \_ nicht \_ gefunden. 
</dt> <dd>

Der angegebene Name für die Farbprofil Datei wurde nicht gefunden. Der Dateiname oder der Pfad ist falsch.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>\_Fehlertag \_ nicht \_ gefunden.
</dt> <dd>

Das angegebene Farbprofil-Elementtag wurde im Farbprofil nicht gefunden.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>\_Fehlertag \_ nicht \_ vorhanden
</dt> <dd>

Ein Farbprofil-Elementtag, das erforderlich ist, damit die Funktion erfolgreich ausgeführt werden kann, wurde nicht an die Funktion übermittelt.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der grundlegenden Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[WCS-Konstanten](wcs-constants.md)
</dt> </dl>

 

 




