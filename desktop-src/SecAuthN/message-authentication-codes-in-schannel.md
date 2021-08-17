---
description: Ein Nachrichtenauthentifizierungscode (MAC) wird verwendet, um Manipulationen und Fälschungen von Nachrichten zu erkennen.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Nachrichtenauthentifizierungscodes in Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db81efbaa71dc94094e5efb14d11dde600798cc8f58855a3a3ae116a624b679f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786982"
---
# <a name="message-authentication-codes-in-schannel"></a>Nachrichtenauthentifizierungscodes in Schannel

Ein [*Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (MAC) wird verwendet, um Manipulationen und Fälschungen von Nachrichten zu erkennen. Der Absender einer Nachricht erstellt einen MAC, [](../secgloss/h-gly.md) indem er einen in [](../secgloss/s-gly.md) eine Richtung gehenden Hash des Nachrichtentexts mithilfe eines Sitzungsschlüssels verschlüsselt, der vom Absender und Empfänger gemeinsam verwendet wird. Der MAC wird an die Nachricht angefügt, die an den Empfänger gesendet wird. Der Nachrichtenempfänger generiert den MAC erneut unter Verwendung des freigegebenen Sitzungsschlüssels und des Nachrichtentexts und vergleicht den generierten MAC mit dem vom Absender empfangenen MAC. Wenn beide identisch sind, muss der Absender über den gemeinsam genutzten Sitzungsschlüssel verfügen, und die Nachricht wurde während der Übertragung nicht geändert.

In Schannel-Protokollen wird der Algorithmus, der [](cipher-suites-in-schannel.md) zum Generieren des MAC verwendet wird, durch die Verschlüsselungssammlung bestimmt, die vom Absender und Empfänger verwendet wird.

 

 
