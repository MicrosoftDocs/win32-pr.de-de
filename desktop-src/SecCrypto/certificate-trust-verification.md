---
description: Zwischen dem Empfänger einer signierten Nachricht und dem Absender der Nachricht muss eine Vertrauensstellung bestehen.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Überprüfung der Zertifikatvertrauensstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9f88d9c944de8f1c6c40e7657c463740fa94fb94a55a8b9bb0f6e33c69d81f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126820"
---
# <a name="certificate-trust-verification"></a>Überprüfung der Zertifikatvertrauensstellung

Zwischen dem Empfänger einer signierten Nachricht und dem Absender der Nachricht muss eine Vertrauensstellung bestehen. Eine Methode zum Einrichten dieser Vertrauensstellung ist ein [*Zertifikat,*](../secgloss/c-gly.md)ein elektronisches Dokument, das überprüft, ob Entitäten oder Personen die person sind, die sie als solches beanspruchen. Ein Zertifikat wird von einem Drittanbieter an eine Entität ausgestellt, der von beiden anderen Parteien als vertrauenswürdig eingestuft wird. Daher entscheidet jeder Empfänger einer signierten Nachricht, ob der Aussteller des Zertifikats des Signers vertrauenswürdig ist. [*CryptoAPI hat*](../secgloss/c-gly.md) eine Methodik implementiert, mit der Anwendungsentwickler Anwendungen erstellen können, die Zertifikate automatisch mit einer vordefinierten Liste vertrauenswürdiger Zertifikate oder [*Stammzertifikate überprüfen.*](../secgloss/r-gly.md) Diese Liste vertrauenswürdiger Entitäten (sogenannte Themen) wird als [*Zertifikatvertrauensliste*](../secgloss/c-gly.md) (Certificate Trust List, CTL) bezeichnet.

Das folgende Beispiel für die Verwendung einer CTL umfasst einen Intranetadministrator (unternehmensinternes Netzwerk), der steuern möchte, welche externen Quellen vertrauenswürdig sind. In diesem Fall kann der Administrator eine Liste mit vertrauenswürdigen Zertifikaten oder Stammzertifikaten erstellen, signieren und die Liste allen Clients im Netzwerk in Form einer CTL zur Verfügung stellen. Eine Anwendung, die für die Verwendung dieser CryptoAPI-Funktionalität entwickelt wurde, akzeptiert dann nur signierte Nachrichten oder heruntergeladene Software, die von Entitäten in der Liste signiert wurde.

Eine Liste dieser Funktionen finden Sie unter [Certificate Verification Functions](cryptography-functions.md).

 

 
