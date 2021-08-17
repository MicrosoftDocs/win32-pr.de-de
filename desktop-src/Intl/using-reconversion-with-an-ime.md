---
description: Ein IME implementiert ein Feature namens &\# 0034;reconversion&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Verwenden von Reconversion mit einem IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5a0453b6ac94da805e00639d2a7a56fd79deca4027d23d47e33aab93e4009b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146843"
---
# <a name="using-reconversion-with-an-ime"></a>Verwenden von Reconversion mit einem IME

Ein IME implementiert ein Feature namens "reconversion". Normalerweise bestimmt der IMM die Listen der Kandidaten nur basierend auf Einträgen, die vom Benutzer typiert wurden. Reconversion ermöglicht es im IMM, einen oder mehrere Kandidaten basierend auf dem enthaltenden Satz (dem Kontext) zu bestimmen. Die definierten Reconversionstypen sind einfach, normal und erweitert.

Die Neukonvertierung ist nützlich, wenn ein Benutzer einen Kompositionsfehler in einem Dokument bemerkt. Der Benutzer kann den Fehler auswählen und in einem Menü reconversion auswählen. Der IME verwendet den Kontext, um den besten Ersatz zu ermitteln. Die Anwendung kann [**ImmSetCompositionString verwenden,**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) um die Reconversion zu unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Eingabemethode-Managers](using-input-method-manager.md)
</dt> </dl>

 

 



