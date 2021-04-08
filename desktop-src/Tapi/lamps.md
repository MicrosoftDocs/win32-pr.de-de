---
description: Die Lampen auf einem Telefongerät können in einer Vielzahl verschiedener beleuchtungsmodi beleuchtet werden.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Aufleuchten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050310"
---
# <a name="lamps"></a>Aufleuchten

Die Lampen auf einem Telefongerät können in einer Vielzahl verschiedener beleuchtungsmodi beleuchtet werden. Im Gegensatz zu klingeln Mustern sind Lamp-Modi in Telefon Sätzen verschiedener Lieferanten eher einheitlich. Eine gemeinsame Gruppe von LAMP-Modi wird von der-API definiert. Eine von der Lamp-Schaltflächen-ID identifizierte Lamp kann in einem bestimmten Lamp-Modus beleuchtet werden. Eine Lamp kann auch für den aktuellen Lamp-Modus abgefragt werden.

Die für die-Leuchten verwendeten TAPI-Funktionen sind [**phonesetlamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), das eine LAMP auf einem angegebenen geöffneten Telefongerät in einem bestimmten Lamp-Beleuchtungs Modus und [**phonegetlamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), das den aktuellen Lamp-Modus der angegebenen Lamp zurückgibt, beleuchtet.

Wenn eine Lamp-Anlage eines Mobiltelefons geändert wird, wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendung gesendet, um die Anwendung über die Statusänderung zu benachrichtigen. Die Parameter für diese Nachricht geben Aufschluss über die Änderung.

 

 



