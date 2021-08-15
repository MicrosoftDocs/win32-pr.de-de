---
description: Mergemodule funktionieren nur mit Komponenten und nicht mit Features. Einige Tabellen in Mergemodulen, z. B. die PublishComponent-Tabelle, enthalten jedoch Felder, die auf Features verweisen.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Verweisen auf Features in Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2857b71fd651955319457092d9cf689ded954af758e7906b44a761dfa6ad782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375950"
---
# <a name="referencing-features-in-merge-modules"></a>Verweisen auf Features in Mergemodulen

Mergemodule funktionieren nur mit Komponenten und nicht mit Features. Einige Tabellen in Mergemodulen, z. B. die [PublishComponent-Tabelle,](publishcomponent-table.md)enthalten jedoch Felder, die auf Features verweisen.

Eine NULL-GUID: {00000000-0000-0000-0000-000000000000} muss in jedem Feld einer Mergemoduldatenbank erstellt werden, die auf ein Feature verweist. Wenn das Mergemodul in einem Installationspaket zusammengeführt wird, ersetzt das Mergetool die NULL-GUID durch das im Installationspaket angegebene Feature, mit Ausnahme von Tabellen, die eine besondere Behandlung erfordern, z. B. die [Tabelle ModuleSignature](modulesignature-table.md) und die ModuleSequence-Tabellen.

Beachten Sie Folgendes: Wenn eine NULL-GUID als Primärschlüssel verwendet wird, ist nicht garantiert, dass der durch das Mergetool ersetzte Wert eindeutig ist. Autoren von Mergemodulen sind dafür verantwortlich, sicherzustellen, dass kein vorhandener Primärschlüssel in der Benutzeroberfläche dupliziert wird, wenn das Mergetool NULL-GUIDs durch Funktionen ersetzt.

 

 



