---
description: Mergemodule erfordern selten eine Benutzeroberfläche.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Erstellen von Benutzeroberflächen in Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931e539d8880c490853b20a6e53b3000f390c0b29f81bf8bb9d3e3703e3f7905
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829190"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>Erstellen von Benutzeroberflächen in Mergemodulen

Mergemodule erfordern selten eine Benutzeroberfläche. Das Freigeben eines Mergemoduls, das sowohl installierbare Komponenten als auch eine Benutzeroberfläche enthält, schränkt letztendlich die Flexibilität des Modulbenutzers ein. Die Kombination von Komponenten und Benutzeroberfläche in einem Modul kann entwickler daran hindern, ihre eigene Benutzeroberfläche zu verwenden oder automatische Installationen bereitzustellen. Eine bessere Alternative besteht darin, zwei Mergemodule freizugeben: eines, das die Komponenten automatisch installiert, und ein zweites optionales Modul, das die Benutzeroberfläche enthält. Das Modul mit der Benutzeroberfläche sollte das Komponentenmodul in seiner [ModuleDependency-Tabelle auflisten.](moduledependency-table.md) Mit dieser Methode können Modulautoren eine Benutzeroberfläche bereitstellen, ohne sie für Entwickler zu erzwingen.

Wenn Benutzeroberflächentabellen in Mergemodulen verwendet werden, können sie auf die gleiche Weise wie alle anderen Tabellen zusammengeführt werden.

 

 



