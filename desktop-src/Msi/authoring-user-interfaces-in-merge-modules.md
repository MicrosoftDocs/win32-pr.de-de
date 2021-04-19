---
description: Mergemodule erfordern selten eine Benutzeroberfläche.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Erstellen von Benutzeroberflächen in Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356681"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>Erstellen von Benutzeroberflächen in Mergemodulen

Mergemodule erfordern selten eine Benutzeroberfläche. Das Freigeben eines Mergemoduls, das sowohl installierbare Komponenten als auch eine Benutzeroberfläche enthält, schränkt letztendlich die Flexibilität des Modul Benutzers ein. Das Kombinieren von Komponenten und Benutzeroberflächen zu einem Modul kann verhindern, dass Entwickler ihre eigene Benutzeroberfläche verwenden oder unbeaufsichtigte Installationen bereitstellen. Eine bessere Alternative besteht darin, zwei Mergemodule freizugeben, eine, die die Komponenten im Hintergrund installiert, und ein zweites optionales Modul, das die Benutzeroberfläche enthält. Das Modul mit der Benutzeroberfläche sollte das Komponenten Modul in seiner [moduledepen-Tabelle](moduledependency-table.md)auflisten. Mit dieser Methode können Modul Autoren eine Benutzeroberfläche bereitstellen, ohne Sie für Entwickler zu erzwingen.

Wenn Benutzeroberflächen Tabellen in Mergemodulen verwendet werden, können Sie auf die gleiche Weise wie alle anderen Tabellen zusammengeführt werden.

 

 



