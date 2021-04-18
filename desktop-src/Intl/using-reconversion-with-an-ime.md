---
description: Ein IME implementiert eine Funktion mit dem Namen &\# 0034; Neukonvertierung&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Verwenden der erneuten Konvertierung mit einem IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340144"
---
# <a name="using-reconversion-with-an-ime"></a>Verwenden der erneuten Konvertierung mit einem IME

Ein IME implementiert eine Funktion namens "Reconversion". Normalerweise bestimmt der imm die Listen der Kandidaten nur auf der Grundlage von Einträgen, die vom Benutzer eingegeben wurden. Die erneute Konvertierung ermöglicht dem imm, eine oder mehrere Kandidaten basierend auf dem enthaltenden Satz (dem Kontext) zu bestimmen. Die definierten neukonvertierungs Typen sind einfach, normal und erweitert.

Eine erneute Konvertierung ist nützlich, wenn ein Benutzer einen Kompositions Fehler in einem Dokument bemerkt. Der Benutzer kann den Fehler auswählen und in einem Menü neu konvertieren auswählen. Der IME verwendet den Kontext, um die beste Ersetzung zu ermitteln. Die Anwendung kann " [**immsetcompositionstring**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) " verwenden, um die erneute Konvertierung zu unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Eingabemethoden-Managers](using-input-method-manager.md)
</dt> </dl>

 

 



