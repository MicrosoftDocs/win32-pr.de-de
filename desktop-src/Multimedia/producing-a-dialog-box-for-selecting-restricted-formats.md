---
title: Erstellen eines Dialogfelds zum Auswählen von eingeschränkten Formaten
description: Erstellen eines Dialogfelds zum Auswählen von eingeschränkten Formaten
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager),Erstellen von Dialogfeldern
- ACM-Beispiele, Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmFormatChoose-Funktion
- Audiokomprimierungs-Manager (ACM), Auswählen eingeschränkter Formate
- ACM (Audiokomprimierungs-Manager),Auswählen eingeschränkter Formate
- ACM-Beispiele, Auswählen von eingeschränkten Formaten
- Auswählen von eingeschränkten Formaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994fffa7ef13f6febe41eb766b4ecaef7eb735f11f58d36f37adfccbb152bffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802040"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a>Erstellen eines Dialogfelds zum Auswählen von eingeschränkten Formaten

Möglicherweise möchten Sie das von der [**acmFormatChoose-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) erstellte Dialogfeld verwenden, aber die Formate im Dialogfeld einschränken oder steuern. Hierzu können Sie das FLAG ACMFORMATCHOOSE \_ STYLEF \_ ENABLEHOOK verwenden, um die Dialogprozedur zu verknüpfen. Die Anwendung kann dann die Formate filtern, indem sie auf die [**MM \_ ACM \_ FORMATCHOOSE-Nachricht**](mm-acm-formatchoose.md) im Meldungsverfahren für das Dialogfeld antwortet.

 

 




