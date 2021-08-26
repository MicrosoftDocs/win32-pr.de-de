---
description: Die umschlagige Nachricht besteht aus der verschlüsselten Nachricht, den Zertifikaten der vorgesehenen Empfänger und dem Satz verschlüsselter Schlüssel, einer für jeden Empfänger. Die generierte Nachricht hat das PKCS \# 7/CMS-Format.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Erstellen und Empfangen von Umschlagdatennachrichten in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4024516333b7dd416f788f181f2ac36e5e0f4e015953cdab26d08b48da16c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876539"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>Erstellen und Empfangen von Umschlagdatennachrichten in CAPICOM

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM.](alternatives-to-using-capicom.md)\]

Eine Umschlagnachricht ist eine Nachricht, die für eine Gruppe von Empfängern verschlüsselt wird. Während des Einschlussprozesses wird ein Sitzungsverschlüsselungsschlüssel generiert, und die Nachricht wird mit diesem Schlüssel verschlüsselt. Der Verschlüsselungsschlüssel selbst wird dann separat für jeden Empfänger verschlüsselt, wobei die öffentlichen Schlüssel aus dem Zertifikat jedes vorgesehenen Empfängers verwendet werden. Die umschlagige Nachricht besteht aus der verschlüsselten Nachricht, den Zertifikaten der vorgesehenen Empfänger und dem Satz verschlüsselter Schlüssel, einer für jeden Empfänger. Die generierte Nachricht hat das PKCS \# 7/CMS-Format.

In den folgenden Abschnitten werden Prozeduren und Beispiele für Umschlagnachrichtentasks gezeigt:

-   [Senden einer Umschlagdatennachricht](sending-an-enveloped-data-message.md)
-   [Empfangen einer Umschlagdatennachricht](receiving-an-enveloped-data-message.md)

 

 



