---
title: Informationen zum Netzwerk Objekt
description: Informationen zum Netzwerk Objekt
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Windows Media Player, Netzwerk Objekt
- Windows Media Player-Objektmodell, Netzwerk Objekt
- Objektmodell, Netzwerk Objekt
- Windows Media Player ActiveX-Steuerelement, Netzwerk Objekt
- ActiveX-Steuerelement, Netzwerk Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Netzwerk Objekt
- Windows Media Player Mobile, Netzwerk Objekt
- Netzwerk Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707800"
---
# <a name="about-the-network-object"></a>Informationen zum Netzwerk Objekt

Das **Netzwerk** Objekt steuert die Eigenschaften, mit denen Sie bestimmen können, wie gut der Inhalt über das Netzwerk gestreamt wird. Beispielsweise können Sie herausfinden, ob Pakete verloren gehen, und die entsprechende Aktion durchführen. Der Zugriff auf das **Netzwerk** Objekt erfolgt nur über die **Network** -Eigenschaft des **Player** -Objekts. Die **Network** -Eigenschaft gibt das **Netzwerk** Objekt zurück. Sie können nur auf die Eigenschaften des **Netzwerk** Objekts zugreifen, nachdem Sie es erstellt haben. Wenn Sie z. b. die **Bandbreiten** Eigenschaft verwenden möchten, müssen Sie den folgenden Code verwenden:


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




