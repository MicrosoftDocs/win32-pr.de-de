---
title: Informationen zum Netzwerkobjekt
description: Informationen zum Netzwerkobjekt
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Windows Media Player,Netzwerkobjekt
- Windows Media Player-Objektmodell, Netzwerkobjekt
- Objektmodell, Netzwerkobjekt
- Windows Media Player ActiveX,Netzwerkobjekt
- ActiveX,Netzwerkobjekt
- Windows Media Player Mobile ActiveX-Steuerelement, Netzwerkobjekt
- Windows Media Player Mobil,Netzwerkobjekt
- Netzwerkobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0378b1cd4469f6141a4ea60021f2d54e5c32b33ae1943624f7c65f70aa2a655f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903290"
---
# <a name="about-the-network-object"></a>Informationen zum Netzwerkobjekt

Das **Network-Objekt** steuert die Eigenschaften, mit denen Sie bestimmen können, wie gut der Inhalt über das Netzwerk gestreamt wird. Beispielsweise können Sie herausfinden, ob Pakete verloren gehen, und entsprechende Maßnahmen ergreifen. Auf **das Network-Objekt** wird nur über die **Netzwerkeigenschaft** des **Player-Objekts** zugegriffen. Die **Netzwerkeigenschaft** gibt das **Network-Objekt** zurück. Sie können erst auf die Eigenschaften des **Network-Objekts zugreifen,** nachdem Sie es erstellt haben. Um beispielsweise die **Bandwidth-Eigenschaft zu** verwenden, müssen Sie den folgenden Code verwenden:


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




