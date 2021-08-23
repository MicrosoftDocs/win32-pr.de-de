---
title: Informationen zu Multimediadatei-E/A
description: Informationen zu Multimediadatei-E/A
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows Multimedia, Datei-E/A
- Multimedia, Datei-E/A
- Multimediaeingabe, Datei-E/A
- Multimediadatei-E/A, Informationen
- Datei-E/A, Informationen
- Eingabe und Ausgabe (E/A), Informationen
- E/A (Eingabe und Ausgabe),Informationen
- Grundlegende E/A
- Resource Interchange File Format (DOSSIER)
- DATEIFORMAT (Resource Interchange File Format)
- IGE E/A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584b736ba41fb0ea7dd5f3e6411e1783964db21a9819fbb98364708196dc2943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526640"
---
# <a name="about-multimedia-file-io"></a>Informationen zu Multimediadatei-E/A

Die meisten Multimediaanwendungen erfordern Dateieingabe und -ausgabe (E/A), d. h. die Möglichkeit, Datenträgerdateien zu erstellen, zu lesen und zu schreiben. Multimedia-Datei-E/A-Dienste bieten gepufferte und nicht gepufferte Datei-E/A- und Unterstützung für CSV-Dateien. Die Dienste sind mit benutzerdefinierten E/A-Prozeduren erweiterbar, die von Anwendungen gemeinsam genutzt werden können.

Die meisten Anwendungen benötigen nur die grundlegenden Datei-E/A-Dienste und die CSV-Datei-E/A-Dienste. Anwendungen, die für die Datei-E/A-Leistung sensibel sind, z. B. Anwendungen, die Daten von Compact Discs in Echtzeit streamen, können die Leistung optimieren, indem Dienste verwendet werden, um direkt auf den Datei-E/A-Puffer zuzugreifen. Anwendungen, die auf benutzerdefinierte Speichersysteme wie Dateiarchive und Datenbanken zugreifen, können eine eigene E/A-Prozedur bereitstellen, die Elemente des Speichersystems liest und schreibt.

 

 




