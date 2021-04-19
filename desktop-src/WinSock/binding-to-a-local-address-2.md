---
description: Bevor ein Socket verwendet werden kann, um eine Verbindung einzurichten oder eine Verbindungsanforderung zu empfangen, muss er an eine lokale Adresse gebunden werden.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Binden an eine lokale Adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348394"
---
# <a name="binding-to-a-local-address"></a>Binden an eine lokale Adresse

Bevor ein Socket verwendet werden kann, um eine Verbindung einzurichten oder eine Verbindungsanforderung zu empfangen, muss er an eine lokale Adresse gebunden werden. Dies kann explizit durch Aufrufen von [**wspbind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))oder implizit durch [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) erfolgen, wenn der Socket beim Aufrufen dieser Funktion nicht gebunden ist.

 

 
