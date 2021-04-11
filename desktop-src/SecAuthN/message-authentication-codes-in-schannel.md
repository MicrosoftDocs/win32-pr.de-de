---
description: Ein Nachrichtenauthentifizierungscode (Mac) wird verwendet, um Manipulationen und Fälschung von Nachrichten zu erkennen.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Nachrichten Authentifizierungs Codes in Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217324"
---
# <a name="message-authentication-codes-in-schannel"></a>Nachrichten Authentifizierungs Codes in Schannel

Ein [*Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (Mac) wird verwendet, um Manipulationen und Fälschung von Nachrichten zu erkennen. Der Absender einer Nachricht erstellt einen Mac durch Verschlüsseln eines unidirektionalen [*Hashs*](../secgloss/h-gly.md) des Nachrichten Texts mithilfe eines [*Sitzungsschlüssels*](../secgloss/s-gly.md) , der vom Absender und Empfänger gemeinsam genutzt wird. Der Mac wird an die Nachricht angehängt, die an den Empfänger gesendet wird. Der Empfänger der Nachricht generiert den Mac mithilfe des freigegebenen Sitzungsschlüssels und des Nachrichten Texts erneut und vergleicht den generierten Mac mit dem Mac, der vom Absender empfangen wurde. Wenn beide identisch sind, muss der Absender über den gemeinsamen Sitzungsschlüssel verfügen, und die Nachricht wurde während der Übertragung nicht geändert.

In Schannel-Protokollen wird der Algorithmus, der verwendet wird, um den Mac zu generieren, durch die Verschlüsselungs [Sammlung](cipher-suites-in-schannel.md) bestimmt, die vom Absender und Empfänger verwendet wird.

 

 
