---
title: Erstellen eines Dialogfelds zum Auswählen eines Formats für die Aufzeichnung
description: Erstellen eines Dialogfelds zum Auswählen eines Formats für die Aufzeichnung
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager), Erzeugen von Dialogfeldern
- ACM-Beispiele,Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmFormatChoose-Funktion
- Audiokomprimierungs-Manager (ACM), Auswählen des Formats für die Neuformatierung
- ACM (Audiokomprimierungs-Manager), Auswählen des Formats für die Neuformatierung
- ACM-Beispiele,Auswählen des Formats für die Neuformatierung
- Auswählen des Formats für die Neuformatierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4650732e290b626eb26cd2eea321124f16b5572a7660aabf09bbe3740934e52d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037680"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a>Erstellen eines Dialogfelds zum Auswählen eines Formats für die Aufzeichnung

Eine Anwendung kann es dem Benutzer ermöglichen, ein Format auszuwählen, für das ein installiertes Waveform-Audio-Gerät native Unterstützung bietet. Beispielsweise möchten Sie, dass ein Waveform-Audio-Editor neue Waveform-Audiodaten aufzeichnen kann, ohne eine ACM-Komprimierung oder einen Dekomprimierer zu verwenden, um eine Übersetzungsebene zu bieten. Verwenden Sie hierzu die [**acmFormatChoose-Funktion,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) und geben Sie die \_ ACM FORMATENUMF HARDWARE- und \_ ACM \_ FORMATENUMF \_ INPUT-Flags im **fdwEnum-Member** der [**ACMFORMATCHOOSE-Struktur**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) an.

 

 




