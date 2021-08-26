---
description: Um eine Datei, eine Schriftart oder einen Registrierungsschlüssel so zu installieren, dass sie nicht entfernt wird, wenn das Produkt deinstalliert wird, muss die gesamte Komponente, die die Datei, schriftart oder den Registrierungsschlüssel enthält, dauerhaft sein.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungsschlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87818c2b9a80d582992dd964daa632575f51e5fa24f17a97af0191277e880df6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105100"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungsschlüsseln

Um eine Datei, eine Schriftart oder einen Registrierungsschlüssel so zu installieren, dass sie nicht entfernt wird, wenn das Produkt deinstalliert wird, muss die gesamte Komponente, die die Datei, schriftart oder den Registrierungsschlüssel enthält, dauerhaft sein. Um eine Komponente dauerhaft zu machen, legen Sie **msidbComponentAttributesPermanent** in der Attributes -Spalte der [Component-Tabelle](component-table.md)fest.

Beachten Sie, dass das Installationsprogramm einen Registrierungsschlüssel entfernt, nachdem der letzte Wert oder Unterschlüssel unter dem Schlüssel entfernt wurde. Um zu verhindern, dass ein leerer Registrierungsschlüssel bei der Deinstallation entfernt wird, schreiben Sie einen Dummywert unter dem Schlüssel, den Sie beibehalten müssen, und geben Sie + in die Spalte Name der [Registrierungstabelle](registry-table.md)ein.

 

 



