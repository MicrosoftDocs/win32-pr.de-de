---
title: Meldungslektion
description: Meldungslektion
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9191e0e189f8653518aaabb3c31785cde960538b0828d56669096ebf1d63f1e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048048"
---
# <a name="message-reflection"></a>Meldungslektion

Es wird dringend empfohlen, dass ein ActiveX-Steuerelementcontainer die Nachrichtenlektion unterstützt. Dies führt zu einem effizienteren Vorgang für Steuerelemente mit Unterklassen. Wenn Die Meldungsreflektion unterstützt wird, muss die Ambient-Eigenschaft MessageReflect unterstützt werden und den Wert **TRUE haben.** Wenn ein Container keine Nachrichtenlektion implementiert, erstellt das OLE CDK zwei Fenster für jedes Steuerelement mit Unterklassen, um im Namen des Steuerelementcontainers Nachrichtenlektion zu ermöglichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

 




