---
title: Erstellen eines Dialog Felds zum Auswählen eines Formats zum Speichern
description: Erstellen eines Dialog Felds zum Auswählen eines Formats zum Speichern
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager), Erstellen von Dialogfeldern
- ACM-Beispiele, Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmformatchoose-Funktion
- Audiokomprimierungs-Manager (ACM), auswählen des zu speichenden Formats
- ACM (Audiokomprimierungs-Manager), auswählen des zu speichenden Formats
- ACM-Beispiele, auswählen des Formats zum Speichern
- Auswählen des Formats zum Speichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2020
ms.locfileid: "104389988"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a>Erstellen eines Dialog Felds zum Auswählen eines Formats zum Speichern

Möglicherweise möchten Sie, dass eine Anwendung vorhandene Waveform-Audiodaten in einem anderen Format speichert. Beispielsweise könnte ein Waveform-Audioeditor eine Waveform-Audiodatei als komprimierte Datei speichern. Um nur die vorgeschlagenen Zielformate für ein angegebenes Quellformat im Dialogfeld aufzulisten, das von der [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Funktion erstellt wurde, geben Sie das Quellformat im **pwfxenum** -Element und das ACM \_ formatenumf-Vorschlags \_ Flag im **fdwenum** -Member der [**acmformatchoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) -Struktur an.

Um gültige Zielformate für ein bestimmtes Format aufzulisten, verwenden Sie das ACM \_ formatenumf \_ Convert-Flag anstelle des ACM \_ formatenumf- \_ Flag zum vorschlagen.

 

 




