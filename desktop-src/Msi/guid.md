---
description: Der GUID-Datentyp ist eine Textzeichenfolge, die einen Klassenbezeichner (ID) darstellt. COM muss die Zeichenfolge in eine gültige Klassen-ID konvertieren können. Alle GUIDs müssen in Großbuchstaben geschrieben werden.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e92688e11d71a51c59a2edc6c3e50ed01ab246c83bf4cfb9ac67b8d6318766b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649340"
---
# <a name="guid"></a>GUID

Der GUID-Datentyp ist eine Textzeichenfolge, die einen Klassenbezeichner (ID) darstellt. COM muss die Zeichenfolge in eine gültige Klassen-ID konvertieren können. Alle GUIDs müssen in Großbuchstaben geschrieben werden.

Das gültige Format für eine GUID ist {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}, wobei X eine hexadezimale Ziffer ist (0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F).

Beachten Sie, dass Hilfsprogramme wie GUIDGEN GUIDs generieren können, die Kleinbuchstaben enthalten. Diese müssen alle in Großbuchstaben geändert werden, bevor die GUID vom Installationsprogramm als gültiger Produktcode, Paketcode oder Komponentencode verwendet werden kann.

 

 



