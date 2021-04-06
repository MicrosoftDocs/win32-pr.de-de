---
title: Suchen nach einem bestimmten Format
description: Suchen nach einem bestimmten Format
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- Audiokomprimierungs-Manager (ACM), suchen nach Formaten
- ACM (Audiokomprimierungs-Manager), suchen nach Formaten
- ACM-Beispiele, suchen nach Formaten
- Suchen nach Formaten
- acmformatenum-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c148c075df09cb702caf6b1d192fe8ce41b48ad0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947983"
---
# <a name="finding-a-specific-format"></a>Suchen nach einem bestimmten Format

Eine Anwendung verfügt möglicherweise nur über eine partielle Spezifikation für ein Format, wenn Sie die vollständige Spezifikation benötigt. Beispielsweise kann die Spezifikation ein 11-kHz-Mono-, 4-Bit-ADPCM-Format, jedoch nicht die durchschnittlichen Bytes pro Sekunde festlegen. Die Anwendung kann das vollständige Format ohne Benutzereingriff mit der [**acmformatenum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) -Funktion und der Angabe von Flags im Parameter " *sdwenum* " erhalten.

 

 




