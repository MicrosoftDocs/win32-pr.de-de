---
description: Zwischen dem Empfänger einer signierten Nachricht und dem Signatur Geber der Nachricht muss eine Vertrauensstellung bestehen.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Zertifikat Vertrauensstellungs Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b711e0a86dcc5ae9cdedea278d6a3a698dfd633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350796"
---
# <a name="certificate-trust-verification"></a>Zertifikat Vertrauensstellungs Überprüfung

Zwischen dem Empfänger einer signierten Nachricht und dem Signatur Geber der Nachricht muss eine Vertrauensstellung bestehen. Eine Methode zum Einrichten dieser Vertrauensstellung ist ein [*Zertifikat*](../secgloss/c-gly.md), ein elektronisches Dokument, das überprüft, ob es sich bei Entitäten oder Personen um die Ansprüche handelt. Ein Zertifikat wird für eine Entität von einem Drittanbieter ausgestellt, der von beiden anderen Parteien als vertrauenswürdig eingestuft wird. Daher entscheidet jeder Empfänger einer signierten Nachricht, ob der Aussteller des Zertifikats des Signatur Gebers vertrauenswürdig ist. [*CryptoAPI*](../secgloss/c-gly.md) hat eine Methodik implementiert, mit der Anwendungsentwickler Anwendungen erstellen können, die Zertifikate automatisch anhand einer vordefinierten Liste vertrauenswürdiger Zertifikate [*oder Stämme*](../secgloss/r-gly.md)überprüfen. Diese Liste vertrauenswürdiger Entitäten (so genannte Themen) wird als [*Zertifikats Vertrauens Liste (Certificate Trust List*](../secgloss/c-gly.md) , CTL) bezeichnet.

Das folgende Beispiel für die Verwendung einer CTL umfasst einen Intranetadministrator (Inner Company Network), der steuern möchte, welche externen Quellen vertrauenswürdig sind. In diesem Fall kann der Administrator eine Liste vertrauenswürdiger Zertifikate oder Stämme erstellen, Signieren und die Liste für alle Clients im Netzwerk in Form einer CTL verfügbar machen. Eine Anwendung, die diese CryptoAPI-Funktionalität verwendet, würde dann nur signierte Nachrichten oder heruntergeladene Software akzeptieren, die von Entitäten in der Liste signiert wurde.

Eine Liste dieser Funktionen finden Sie unter Funktionen für die [Zertifikat Überprüfung](cryptography-functions.md).

 

 
