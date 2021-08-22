---
description: Wenn die Regeln der Standardauswahl nicht den Anforderungen der Anwendung entsprechen, hat die Anwendung die Möglichkeit, das Terminal manuell auszuwählen.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Manuelle Terminalauswahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6eaa1e0a5b8b53b1037c51b0e628d7a27ece0be65a0f9a7e86e882c722360f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514640"
---
# <a name="manual-terminal-selection"></a>Manuelle Terminalauswahl

Wenn die Standardauswahlregeln die Anforderungen der Anwendung nicht erfüllen, hat die Anwendung die Möglichkeit, das Terminal wie immer auszuwählen. Das heißt, sie kann [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) verwenden, um die im Aufruf verfügbaren Streams aufzählen und das Terminal in den entsprechenden Streams auswählen (oder bei Multitrack-Terminals Spuren für die Streams erstellen und erstellte Spuren in den Streams auswählen).

 

 
