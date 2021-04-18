---
title: Informationen zu Multimedia-Datei-e/a
description: Informationen zu Multimedia-Datei-e/a
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows-Multimedia, Datei-e/a
- Multimedia, Datei-e/a
- Multimedia-Eingabe, Datei-e/a
- Multimedia-Datei-e/a, Informationen
- Datei-e/a, Informationen
- Eingabe und Ausgabe (e/a), Informationen zu
- E/a (Eingabe und Ausgabe), Informationen zu
- grundlegende e/a
- Format der Ressourcenaustausch Datei (Riff)
- Riff (Ressourcenaustausch-Dateiformat)
- Riff-e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340833"
---
# <a name="about-multimedia-file-io"></a>Informationen zu Multimedia-Datei-e/a

Die meisten Multimedia-Anwendungen erfordern Datei Eingaben und-Ausgaben (e/a) – d. h. die Fähigkeit, Datenträger Dateien zu erstellen, zu lesen und zu schreiben. Multimedia-Datei-e/a-Dienste bieten gepufferte und nicht gepufferte Datei-e/a und Unterstützung für Riff-Dateien. Die Dienste können durch benutzerdefinierte e/a-Prozeduren erweitert werden, die von den Anwendungen gemeinsam genutzt werden können.

Die meisten Anwendungen benötigen nur die grundlegenden Datei-e/a-Dienste und die Datei-e/a-Dienste von Riff Dateien. Anwendungen, die für die Datei-e/a-Leistung sensibel sind, z. b. Anwendungen, die Daten aus Compact Disk in Echtzeit streamen, können die Leistung optimieren, indem Sie Dienste direkt auf den Datei-e/a-Puffer zugreifen. Anwendungen, die auf benutzerdefinierte Speichersysteme (z. b. Dateiarchive und Datenbanken) zugreifen, können Ihre eigene e/a-Prozedur bereitstellen, mit der Elemente des Speichersystems gelesen und geschrieben werden.

 

 




