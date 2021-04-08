---
description: Mergemodule funktionieren nur mit-Komponenten und nicht mit-Funktionen. Einige Tabellen in Mergemodulen, wie z. b. die PublishComponent-Tabelle, enthalten jedoch Felder, die auf Funktionen verweisen.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Verweisen auf Features in Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959658"
---
# <a name="referencing-features-in-merge-modules"></a>Verweisen auf Features in Mergemodulen

Mergemodule funktionieren nur mit-Komponenten und nicht mit-Funktionen. Einige Tabellen in Mergemodulen, wie z. b. die [PublishComponent-Tabelle](publishcomponent-table.md), enthalten jedoch Felder, die auf Funktionen verweisen.

Eine NULL-GUID: {00000000-0000-0000-0000-000000000000} muss in einem beliebigen Feld einer mergemoduldatenbank erstellt werden, die auf eine Funktion verweist. Wenn das Mergemodul in ein Installationspaket zusammengeführt wird, ersetzt das Mergetool die NULL-GUID durch die im Installationspaket angegebene Funktion, mit Ausnahme von Tabellen, die eine besondere Behandlung erfordern, wie z. b. die [ModuleSignature-Tabelle](modulesignature-table.md) und die modulesequence-Tabellen.

Wenn eine NULL-GUID als Primärschlüssel verwendet wird, ist nicht sichergestellt, dass der durch das Mergetool ersetzte Wert eindeutig ist. Autoren von Mergemodulen sind dafür verantwortlich, sicherzustellen, dass kein vorhandener Primärschlüssel in der Benutzeroberfläche dupliziert wird, wenn das Mergetool NULL-GUIDs durch Funktionen ersetzt.

 

 



