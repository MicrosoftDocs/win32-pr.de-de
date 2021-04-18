---
description: Eine eingeschlossene Nachricht ist eine Nachricht, die für einen Empfänger oder eine Gruppe von Empfängern verschlüsselt ist.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Erstellen und empfangen von eingeschlossenen Daten Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354455"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a>Erstellen und empfangen von eingeschlossenen Daten Nachrichten

Eine eingeschlossene Nachricht ist eine Nachricht, die für eine Gruppe von Empfängern verschlüsselt ist. Im Umschlag Prozess wird ein Sitzungs Verschlüsselungsschlüssel generiert, und die Nachricht wird mit diesem Schlüssel verschlüsselt. Der Verschlüsselungsschlüssel selbst wird dann separat für jeden Empfänger verschlüsselt, wobei die öffentlichen Schlüssel aus dem Zertifikat des gewünschten Empfängers verwendet werden. Die eingeschlossene Nachricht besteht aus der verschlüsselten Nachricht, den Zertifikaten der vorgesehenen Empfänger und dem Satz verschlüsselter Schlüssel, einer für jeden Empfänger. Die generierte Nachricht weist das [*PKCS \# 7*](../secgloss/p-gly.md)/CMS-Format auf.

In den folgenden Abschnitten werden Prozeduren und Beispiele für eingeschlossene Nachrichten Aufgaben beschrieben:

-   [Codieren von eingeschlossenen Daten](encoding-enveloped-data.md)
-   [Decodieren von eingeschlossenen Daten](decoding-enveloped-data.md)
-   [Alternativer Code zum Codieren einer eingeschlossenen Nachricht](alternate-code-for-encoding-an-enveloped-message.md)
-   [Beispiel-C-Programm: Codieren einer eingeschlossenen, signierten Nachricht](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
