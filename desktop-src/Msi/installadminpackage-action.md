---
description: Die InstallAdminPackage-Aktion kopiert die Produktdatenbank auf den Administratorinstallationspunkt, der durch die TARGETDIR-Eigenschaft definiert wird.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: InstallAdminPackage-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1879d711e1a52a7121326ba170bb3a004fbfb4ee988b35d19a16e1a53c3e2811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996590"
---
# <a name="installadminpackage-action"></a>InstallAdminPackage-Aktion

Die InstallAdminPackage-Aktion kopiert die Produktdatenbank auf den Administratorinstallationspunkt, der durch die [**TARGETDIR-Eigenschaft definiert**](targetdir.md) wird.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                                 |
|-------|------------------------------------------------------------|
| \[1\] | Name der Installationsdateien.                                     |
| \[6\] | Größe der Datenbank.                                          |
| \[9\] | Bezeichner des Administratorinstallations-Punktverzeichnisses. |



 

## <a name="remarks"></a>Hinweise

Die Aktion InstallAdminPackage aktualisiert auch die Zusammenfassungsinformationen der Datenbank und entfernt alle In-Stream-Dateien, nachdem die Datenbank kopiert wurde.

 

 



