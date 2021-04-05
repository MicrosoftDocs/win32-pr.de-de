---
title: Erstellen eines Dialog Felds zum Auswählen von eingeschränkten Formaten
description: Erstellen eines Dialog Felds zum Auswählen von eingeschränkten Formaten
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager), Erstellen von Dialogfeldern
- ACM-Beispiele, Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmformatchoose-Funktion
- Audiokomprimierungs-Manager (ACM), auswählen von eingeschränkten Formaten
- ACM (Audiokomprimierungs-Manager), auswählen von eingeschränkten Formaten
- ACM-Beispiele, auswählen von eingeschränkten Formaten
- Auswählen von eingeschränkten Formaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800945f4003c0fbe47d7916e0a1bf707745ff6d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037095"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a>Erstellen eines Dialog Felds zum Auswählen von eingeschränkten Formaten

Möglicherweise möchten Sie das Dialogfeld verwenden, das von der [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Funktion erstellt wurde, aber beschränken oder Steuern Sie die Formate im Dialogfeld. Hierfür können Sie das Flag "acmformatchoose \_ stylef \_ ENABLEHOOK" verwenden, um die Dialogfeld Prozedur zu verbinden. Die Anwendung kann dann die Formate filtern, indem Sie in der Nachrichten Prozedur für das Dialogfeld auf die Meldung [**mm \_ ACM \_ formatchoose**](mm-acm-formatchoose.md) antwortet.

 

 




