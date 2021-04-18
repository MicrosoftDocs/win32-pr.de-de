---
description: Abrufen einer leeren mergemoduldatenbank. Sie können die Datei Schema. msm verwenden, die mit dem Windows Installer SDK bereitgestellt wird, als Start Datenbank für das Mergemodul. Weitere Informationen finden Sie unter Windows SDK Komponenten für Windows Installer Entwickler.
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: Abrufen von leeren mergemoduldatenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba75d55763d30b0ab545d2dbddbc19c1b0c279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343804"
---
# <a name="obtaining-blank-merge-module-databases"></a>Abrufen von leeren mergemoduldatenbanken

Abrufen einer leeren mergemoduldatenbank. Sie können die Datei Schema. msm verwenden, die mit dem Windows Installer SDK bereitgestellt wird, als Start Datenbank für das Mergemodul. Weitere Informationen finden Sie unter [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md).

Entwickler sollten Mergemodule mithilfe des einfachsten Datenbankschemas erstellen, das Ihre Komponenten installiert. Durch die Verwendung eines einfachen Schemas wird die höchste Kompatibilität für das Mergemodul sichergestellt. Das Zusammenführen eines Mergemoduls in ein Installationspaket mit einem anderen Datenbankschema führt in der Regel zu Mergekonflikten.

Eine vollständige Liste aller erforderlichen und optionalen Tabellen in Mergemodulen finden Sie unter [Merge Module Database Tables](merge-module-database-tables.md).

 

 



