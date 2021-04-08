---
description: TAPI modelliert eine Schaltfläche für Smartphones und Lampen als Schaltflächen-Lamp-Paare.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Telefon Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755112"
---
# <a name="phone-buttons"></a>Telefon Schaltflächen

TAPI modelliert die Schaltflächen und Lampen eines Telefons als Schaltflächen-Lamp-Paare. Eine Schaltfläche, auf der keine Lamp daneben steht, oder eine Lamp ohne Schaltfläche wird mithilfe eines "Dummy"-Indikators für die fehlende Lamp oder Schaltfläche angegeben. Eine Schaltfläche mit mehreren Lampen wird mithilfe mehrerer Schaltflächen-Lamp-Paare modelliert.

Die einer Telefon Schaltfläche zugeordneten Informationen können festgelegt und abgerufen werden. Wenn eine Schaltfläche gedrückt wird, wird eine [**Telefon- \_ Schalt**](phone-button.md) Flächen Meldung an die Anwendungsfunktion gesendet. Bei den Parametern dieser Nachricht handelt es sich um ein Handle für das Telefongerät und den Schaltflächen-Lamp-Bezeichner der Schaltfläche, die gedrückt wurde. Die Tastatur-Schaltflächen "0" bis "9", " \* " und " \# " werden den fixierten Schaltflächen-Lamp-IDs 0 bis 11 zugewiesen.

Die den Schaltflächen zugeordneten Funktionen sind " [**phonesetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo)", mit dem die mit einer Schaltfläche auf einem Telefongerät verknüpften Informationen festgelegt werden, und [**phonegetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), das Informationen zurückgibt, die einer Schaltfläche auf einem Telefongerät zugeordnet sind. Die \_ Meldung Telefon Schaltfläche wird an eine Anwendung gesendet, wenn auf dem Telefon eine Schaltfläche gedrückt wird.

Die einer Schaltfläche zugeordneten Informationen enthalten keinerlei semantische Bedeutung, die von TAPI betroffen ist. Dies ist nützlich für gerätespezifische Anwendungen, die die Bedeutung dieser Informationen für ein bestimmtes Telefongerät oder für die Anzeige für den Benutzer verstehen, z. b. die Online Hilfe.

 

 



