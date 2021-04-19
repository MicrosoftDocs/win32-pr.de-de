---
description: Microsoft Telefonie modelliert eine Schaltfläche für Smartphones und Lampen als Schaltflächen-Lamp-Paare.
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: Schaltflächen (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355619"
---
# <a name="buttons-telephony-api"></a>Schaltflächen (telefonieapi)

Microsoft Telefonie modelliert die Schaltflächen und Lampen eines Telefons als Schaltflächen-Lamp-Paare. Eine Schaltfläche, auf der keine Lamp daneben steht, oder eine Lamp ohne Schaltfläche wird mit einem Dummy-Indikator für die fehlende Lamp oder Schaltfläche angegeben. Eine Schaltfläche mit mehreren Lampen wird mithilfe mehrerer Schaltflächen-Lamp-Paare modelliert.

Die einer Telefon Schaltfläche zugeordneten Informationen können festgelegt und abgerufen werden. Wenn eine Schaltfläche gedrückt wird, sendet der Dienstanbieter eine [**Telefon- \_ Schalt**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) Flächen Meldung an die TAPI-Rückruffunktion. Bei den Parametern dieser Nachricht handelt es sich um ein Handle für das Telefongerät und die Schaltfläche/Lamp-ID der Schaltfläche, die gedrückt wurde. Der Tastatur-Schaltfläche "0" bis "9", " \* " und " \# " werden die fixierten Schaltflächen-/Lamp-IDs 0 bis 11 zugewiesen.

Die Funktion [**TSPI \_ phonesetbuttoninfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) legt die Informationen fest, die mit einer Schaltfläche auf einem Telefongerät verknüpft sind. [**TSPI \_ phonegetbuttoninfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) gibt Informationen zurück, die mit einer Schaltfläche auf einem Telefongerät verknüpft sind. Der Dienstanbieter sendet eine Telefon- \_ Schaltflächen Meldung an die TAPI-Rückruffunktion, wenn eine Schaltfläche auf dem Telefon gedrückt wird.

Die einer Schaltfläche zugeordneten Informationen enthalten keine semantische Bedeutung, soweit dies für TSPI relevant ist. Dies ist nützlich für gerätespezifische Anwendungen, die diese Informationen für ein bestimmtes Telefongerät interpretieren, oder für die Anzeige für den Benutzer, z. b. im Hilfesystem einer Anwendung.

 

 
