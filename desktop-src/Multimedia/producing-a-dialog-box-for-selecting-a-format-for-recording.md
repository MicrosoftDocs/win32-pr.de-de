---
title: Erstellen eines Dialog Felds zum Auswählen eines Formats für die Aufzeichnung
description: Erstellen eines Dialog Felds zum Auswählen eines Formats für die Aufzeichnung
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager), Erstellen von Dialogfeldern
- ACM-Beispiele, Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmformatchoose-Funktion
- Audiokomprimierungs-Manager (ACM), auswählen des Formats für das umherstellen
- ACM (Audiokomprimierungs-Manager), auswählen des Formats für das umherstellen
- ACM-Beispiele, auswählen des Formats für das umherstellen
- Auswählen des Formats für das Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2020
ms.locfileid: "104389987"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a>Erstellen eines Dialog Felds zum Auswählen eines Formats für die Aufzeichnung

Eine Anwendung kann es Benutzern ermöglichen, ein Format auszuwählen, für das ein installiertes Waveform-Audiogerät Native Unterstützung bietet. Angenommen, Sie möchten, dass ein Waveform-Audioeditor neue Waveform-Audiodaten aufzeichnen kann, ohne einen ACM-Kompressor oder-Debug zum Bereitstellen einer übersetzungsebene zu verwenden. Verwenden Sie hierzu die [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Funktion, und geben Sie dabei die ACM \_ formatenumf \_ -Hardware und die ACM \_ formatenumf- \_ eingabeflags im **fdwenum** -Member der [**acmformatchoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) -Struktur an.

 

 




