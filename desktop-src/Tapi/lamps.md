---
description: Die Beleuchtung auf einem Telefongerät kann in einer Vielzahl verschiedener Beleuchtungsmodi entfacht werden.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lamps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150e499dbd66ca772d35855c4cdb086bbb1ecc12617f55bcd33dccf8435e8771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762284"
---
# <a name="lamps"></a>Lamps

Die Beleuchtung auf einem Telefongerät kann in einer Vielzahl verschiedener Beleuchtungsmodi entfacht werden. Im Gegensatz zu Ringmustern sind die Lampemodi für Telefongruppen verschiedener Anbieter einheitlicher. Ein allgemeiner Satz von Lampemodi wird von der API definiert. Eine Lampe, die durch ihren Lampe-Schaltflächenbezeichner identifiziert wird, kann in einem bestimmten Lampemodus angelichtet werden. Eine Lampe kann auch nach ihrem aktuellen Lampemodus abgefragt werden.

Die TAPI-Funktionen, die für die Beleuchtung verwendet werden, sind [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), die eine Lampe auf einem angegebenen geöffneten Telefongerät in einem bestimmten Lampe-Beleuchtungsmodus ausleuchten, und [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), das den aktuellen Lampemodus der angegebenen Lampe zurückgibt.

Wenn eine Lampe eines Telefongeräts geändert wird, wird eine [**PHONE \_ STATE-Nachricht**](phone-state.md) an die Anwendung gesendet, um die Anwendung über die Zustandsänderung zu benachrichtigen. Parameter für diese Meldung geben einen Hinweis auf die Änderung.

 

 



