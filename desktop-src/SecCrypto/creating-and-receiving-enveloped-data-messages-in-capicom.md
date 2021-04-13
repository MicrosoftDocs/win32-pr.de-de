---
description: Die eingeschlossene Nachricht besteht aus der verschlüsselten Nachricht, den Zertifikaten der vorgesehenen Empfänger und dem Satz verschlüsselter Schlüssel, einer für jeden Empfänger. Die generierte Nachricht weist das PKCS \# 7/CMS-Format auf.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Erstellen und empfangen von eingeschlossenen Daten Nachrichten in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343149"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>Erstellen und empfangen von eingeschlossenen Daten Nachrichten in CAPICOM

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Eine eingeschlossene Nachricht ist eine Nachricht, die für eine Gruppe von Empfängern verschlüsselt ist. Im Umschlag Prozess wird ein Sitzungs Verschlüsselungsschlüssel generiert, und die Nachricht wird mit diesem Schlüssel verschlüsselt. Der Verschlüsselungsschlüssel selbst wird dann separat für jeden Empfänger verschlüsselt, wobei die öffentlichen Schlüssel aus dem Zertifikat des gewünschten Empfängers verwendet werden. Die eingeschlossene Nachricht besteht aus der verschlüsselten Nachricht, den Zertifikaten der vorgesehenen Empfänger und dem Satz verschlüsselter Schlüssel, einer für jeden Empfänger. Die generierte Nachricht weist das PKCS \# 7/CMS-Format auf.

In den folgenden Abschnitten werden Prozeduren und Beispiele für eingeschlossene Nachrichten Aufgaben beschrieben:

-   [Senden einer eingeschlossenen Daten Nachricht](sending-an-enveloped-data-message.md)
-   [Empfangen einer eingeschlossenen Daten Nachricht](receiving-an-enveloped-data-message.md)

 

 



