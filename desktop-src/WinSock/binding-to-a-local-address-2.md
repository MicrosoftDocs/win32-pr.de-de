---
description: Bevor ein Socket verwendet werden kann, um eine Verbindung einzurichten oder eine Verbindungsanforderung zu empfangen, muss er an eine lokale Adresse gebunden werden.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Binden an eine lokale Adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd4691e6581cbe1a3a2dee21d7dc4e0a0672812121028c515ad192b30279f61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132753"
---
# <a name="binding-to-a-local-address"></a>Binden an eine lokale Adresse

Bevor ein Socket verwendet werden kann, um eine Verbindung einzurichten oder eine Verbindungsanforderung zu empfangen, muss er an eine lokale Adresse gebunden werden. Dies kann explizit durch Aufrufen von [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))oder implizit durch [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) erfolgen, wenn der Socket beim Aufrufen dieser Funktion ungebunden ist.

 

 
