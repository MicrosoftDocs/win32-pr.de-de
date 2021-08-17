---
description: Eine umhumhierte Nachricht ist eine Nachricht, die für einen Empfänger oder eine Gruppe von Empfängern verschlüsselt ist.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Erstellen und Empfangen von Umschlagdatennachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63abf31d582ae9ae184dc15d85d827a3741d317e3bad75c8b07cce25e457bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768905"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a>Erstellen und Empfangen von Umschlagdatennachrichten

Eine umhumhierte Nachricht ist eine Nachricht, die für eine Gruppe von Empfängern verschlüsselt ist. Während des Umschrägevorgangs wird ein Sitzungsverschlüsselungsschlüssel generiert, und die Nachricht wird mit diesem Schlüssel verschlüsselt. Der Verschlüsselungsschlüssel selbst wird dann separat für jeden Empfänger mithilfe der öffentlichen Schlüssel aus dem Zertifikat jedes vorgesehenen Empfängers verschlüsselt. Die umhumschlagte Nachricht besteht aus der verschlüsselten Nachricht, den Zertifikaten der vorgesehenen Empfänger und dem Satz verschlüsselter Schlüssel, einen für jeden Empfänger. Die generierte Nachricht hat das [*FORMAT PKCS \# 7*](../secgloss/p-gly.md)/CMS.

In den folgenden Abschnitten werden Prozeduren und Beispiele für Umschlagnachrichtenaufgaben gezeigt:

-   [Codieren von umhumhierten Daten](encoding-enveloped-data.md)
-   [Decodieren von umumschlagten Daten](decoding-enveloped-data.md)
-   [Alternativer Code zum Codieren einer umschlagten Nachricht](alternate-code-for-encoding-an-enveloped-message.md)
-   [Beispiel C-Programm: Codieren einer umschlagenden, signierten Nachricht](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
