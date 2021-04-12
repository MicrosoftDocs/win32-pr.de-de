---
title: Freigeben von anzeigen Listen
description: Wenn Sie einen renderingkontext erstellen, verfügt er über einen eigenen Anzeigelisten Bereich.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL unter Windows, Freigabe von anzeigen Listen
- Freigabe anzeigen listet OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311075"
---
# <a name="sharing-display-lists"></a>Freigeben von anzeigen Listen

Wenn Sie einen renderingkontext erstellen, verfügt er über einen eigenen Anzeigelisten Bereich. Die Funktion [**wglsharelists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) ermöglicht einem renderingkontext das Freigeben des Anzeigelisten Raums eines anderen renderingkontexts. Eine beliebige Anzahl von renderingkontexten kann einen einzelnen Anzeigelisten Bereich gemeinsam verwenden.

 

 




