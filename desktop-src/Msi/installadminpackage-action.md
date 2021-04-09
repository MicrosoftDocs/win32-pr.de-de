---
description: Mit der Aktion "installadminpackage" wird die Produktdatenbank auf den administrativen Installations Punkt kopiert, der durch die Eigenschaft "TARGETDIR" definiert wird.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Installadminpackage-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959496"
---
# <a name="installadminpackage-action"></a>Installadminpackage-Aktion

Mit der Aktion "installadminpackage" wird die Produktdatenbank auf den administrativen Installations Punkt kopiert, der durch die Eigenschaft " [**TARGETDIR**](targetdir.md) " definiert wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                                 |
|-------|------------------------------------------------------------|
| \[1\] | Name der Installationsdateien.                                     |
| \[6\] | Größe der Datenbank.                                          |
| \[9\] | Bezeichner der administrativen Installation – Punkt Verzeichnis. |



 

## <a name="remarks"></a>Bemerkungen

Die Aktion installadminpackage aktualisiert auch die Zusammenfassungs Informationen der Datenbank und entfernt alle CAB-Dateien, die sich in Streams befinden, nachdem die Datenbank kopiert wurde.

 

 



