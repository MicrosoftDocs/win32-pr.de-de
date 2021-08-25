---
title: WCS-spezifische Fehlercodes
description: Im Folgenden wird eine Liste der Fehlercodes aufgeführt, die sich speziell auf die Verwendung von WCS 1.0 beziehen.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46127e27b0f0890e305fee65534b0cce743c086e9e89934797bf2b16b15e9f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814600"
---
# <a name="error-codes-specific-to-wcs"></a>WCS-spezifische Fehlercodes

Im Folgenden wird eine Liste der Fehlercodes aufgeführt, die sich speziell auf die Verwendung von WCS 1.0 beziehen. Dies bedeutet nicht, dass WCS-Funktionen nur diese Fehlercodes zurückgeben. Dies bedeutet, dass die Codes in der folgenden Tabelle nur von WCS-Funktionen zurückgegeben werden. Sie können auch andere Win32-Fehlercodes zurückgeben, die an anderer Stelle in der Win32-API des Plattform-SDK dokumentiert sind.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>FEHLER \_ BEIM LÖSCHEN ICM \_ \_ XFORM
</dt> <dd>

Die angegebene Farbtransformation konnte nicht gelöscht werden.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERROR \_ DUPLICATE \_ TAG
</dt> <dd>

Das angegebene Farbprofilelementtag ist bereits im Farbprofil vorhanden.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>FEHLER \_ ICM \_ NICHT \_ AKTIVIERT
</dt> <dd>

Die Bildfarbverwaltung ist derzeit nicht aktiviert.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>FEHLER: \_ UNGÜLTIGER \_ CMM
</dt> <dd>

Der angegebene Dateiname verweist nicht auf ein gültiges Farbverwaltungsmodul.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>FEHLER: \_ UNGÜLTIGER \_ COLORSPACE
</dt> <dd>

Der angegebene Farbraum ist ungültig.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>FEHLER: \_ UNGÜLTIGES \_ PROFIL
</dt> <dd>

Der angegebene Dateiname verweist nicht auf ein gültiges Farbprofil.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>FEHLER: \_ UNGÜLTIGE \_ TRANSFORMATION 
</dt> <dd>

Die angegebene Farbtransformation ist keine gültige Farbtransformation.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>FEHLERPROFIL \_ \_ NICHT DEM \_ \_ GERÄT ZUGEORDNET \_
</dt> <dd>

Das angegebene Farbprofil ist keinem Gerät zugeordnet.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>FEHLERPROFIL \_ \_ NICHT \_ GEFUNDEN 
</dt> <dd>

Der angegebene Farbprofildateiname wurde nicht gefunden. Der Dateiname oder Pfad ist falsch.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>FEHLERTAG \_ \_ NICHT \_ GEFUNDEN
</dt> <dd>

Das angegebene Farbprofilelementtag wurde im Farbprofil nicht gefunden.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>FEHLERTAG \_ \_ NICHT \_ VORHANDEN
</dt> <dd>

Ein Farbprofilelementtag, das erforderlich ist, damit die Funktion erfolgreich ausgeführt werden kann, wurde nicht an die Funktion übergeben.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Farbverwaltungskonzepte](basic-color-management-concepts.md)
</dt> <dt>

[WCS-Konstanten](wcs-constants.md)
</dt> </dl>

 

 




