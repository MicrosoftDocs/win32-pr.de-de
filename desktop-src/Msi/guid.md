---
description: Der GUID-Datentyp ist eine Text Zeichenfolge, die einen Klassen Bezeichner (ID) darstellt. COM muss in der Lage sein, die Zeichenfolge in eine gültige Klassen-ID zu konvertieren. Alle GUIDs müssen in Großbuchstaben erstellt werden.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297c9995d537f6cf4b9d2ccf35488e27dc35903f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347665"
---
# <a name="guid"></a>GUID

Der GUID-Datentyp ist eine Text Zeichenfolge, die einen Klassen Bezeichner (ID) darstellt. COM muss in der Lage sein, die Zeichenfolge in eine gültige Klassen-ID zu konvertieren. Alle GUIDs müssen in Großbuchstaben erstellt werden.

Das gültige Format für eine GUID ist {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}, wobei X eine hexadezimale Ziffer ist (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, B, C, D, E, F).

Beachten Sie, dass Hilfsprogramme, wie z. b. GUIDGEN, GUIDs mit Kleinbuchstaben generieren können. Diese müssen alle in Großbuchstaben geändert werden, bevor die GUID vom Installer als gültiger Produktcode, Paketcode oder Komponenten Code verwendet werden kann.

 

 



