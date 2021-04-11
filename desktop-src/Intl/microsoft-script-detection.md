---
description: Der Els-Skript Erkennungsdienst heißt Microsoft Script-Erkennung.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Microsoft-Skript Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130312"
---
# <a name="microsoft-script-detection"></a>Microsoft-Skript Erkennung

Der Els-Skript Erkennungsdienst heißt Microsoft Script-Erkennung. Dieser Dienst ermöglicht es Anwendungen, die Skripts zu erkennen, in denen Text geschrieben wurde. Die NLS-Entsprechung (National Language Support) eines Skript Erkennungs Dienstanbieter ist die [getstringscripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) -Funktion. Der Els-Dienst ruft jedoch zusätzlich die Textbereiche ab, die zu jedem Schreibsystem gehören.

## <a name="input-to-microsoft-script-detection"></a>Eingabe für die Microsoft-Skript Erkennung

Die Eingabe für den Microsoft Script-Erkennungsdienst ist UTF-16-Text, für den der Dienst Skript Bereiche bestimmt.

## <a name="output-of-microsoft-script-detection"></a>Ausgabe der Microsoft-Skript Erkennung

Die Ausgabe des Microsoft Script-Erkennungs Dienstanbieter ist ein Array von Bereichen, die jeweils eine mit NULL endenden UTF-16-Zeichenfolge mit dem Unicode-angegebenen Namen des zugeordneten Schreibsystems enthalten. Der Dienst meldet reguläre allgemeine (zyyy) und geerbte (Qaai) Zeichen, die dem vorherigen Skript Bereich angehören. Beginnende gängige und geerbte Zeichen werden als zum nächsten Skript Bereich gehörend gemeldet. Wenn alle Zeichen im Eingabetext allgemein oder vererbt sind, ist die Ausgabe des dienstantrags ein einzelner Bereich mit der leeren Zeichenfolge als Daten.

## <a name="microsoft-script-detection-operation"></a>Microsoft-Skript Erkennungs Vorgang

Der Microsoft Script-Erkennungsdienst ordnet dem vorangehenden Schreibsystem die Code Punkte zu, die dem allgemeinen Bereich angehören. Alternativ kann der Dienst die Code Punkte dem nächsten Schreibsystem zuordnen, wenn sich die Code Punkte am Anfang der Eingabe Zeichenfolge befinden. Die Anwendung muss sich nicht mit dem allgemeinen Bereich beschäftigen.

## <a name="microsoft-script-detection-guid"></a>Microsoft-Skript Erkennungs-GUID

Die GUID für den Microsoft Sprachenerkennung-Dienst wird in elssrvc. h deklariert, wie im folgenden Code gezeigt.


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu erweiterten linguistischen Diensten](about-extended-linguistic-services.md)
</dt> </dl>

 

 



