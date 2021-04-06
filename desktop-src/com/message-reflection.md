---
title: Nachrichten Reflektion
description: Nachrichten Reflektion
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036283"
---
# <a name="message-reflection"></a>Nachrichten Reflektion

Es wird dringend empfohlen, dass ein ActiveX-Steuerelement Container Nachrichten Reflektion unterstützt. Dies führt zu einer effizienteren Operation für untergeordnete Steuerelemente. Wenn Nachrichten Reflektion unterstützt wird, muss die Ambient-Eigenschaft MessageReflect unterstützt werden und den Wert **true** aufweisen. Wenn ein Container keine Nachrichten Reflektion implementiert, erstellt das OLE CDK zwei Fenster für jedes untergeordnete Steuerelement, um Nachrichten Reflektion für den Steuerungs Container bereitzustellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

 




