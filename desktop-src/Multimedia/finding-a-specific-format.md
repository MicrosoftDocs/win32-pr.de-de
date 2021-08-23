---
title: Suchen eines bestimmten Formats
description: Suchen eines bestimmten Formats
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- Audiokomprimierungs-Manager (ACM), Suchen von Formaten
- ACM (Audiokomprimierungs-Manager), Suchen von Formaten
- ACM-Beispiele,Suchen von Formaten
- Suchen von Formaten
- acmFormatEnum-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc291a6dff0c6b2befec6afd001a32735a54e95fd65a464378adb690a95019c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691530"
---
# <a name="finding-a-specific-format"></a>Suchen eines bestimmten Formats

Eine Anwendung hat möglicherweise nur eine partielle Spezifikation für ein Format, wenn sie die vollständige Spezifikation benötigt. Die Spezifikation könnte beispielsweise ein 11-kHz-Mono- und 4-Bit-ADPCM-Format, aber nicht die durchschnittlichen Bytes pro Sekunde vorgaben. Die Anwendung kann das vollständige Format ohne Benutzereingriff erhalten, indem sie die [**acmFormatEnum-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) verwendet und Flags im *fdwEnum-Parameter angibt.*

 

 




