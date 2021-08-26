---
description: Listet die Schritte auf, die zum Initialisieren eines Sicherheitspakets erforderlich sind, und erläutert sie.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Initialisieren des Sicherheitspakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d39cbbd9a1126a22d04c14bee3b6ac9b305b2feb3593d03756779e4cb0649b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015850"
---
# <a name="initializing-the-security-package"></a>Initialisieren des Sicherheitspakets

Diese Schritte sind vor der Verwendung von SSPI erforderlich:

1.  Die Initialisierungsfunktion muss aufgerufen werden, um die Adresse der Sicherheitsfunktionstabelle abzurufen.

    Client und Server rufen [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) für einen Zeiger auf eine [**SecurityFunctionTable-Dispatchtabelle**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) auf. Diese Tabelle enthält Zeiger auf Rückruffunktionen, die in "Sspi.h" deklariert sind. Diese Zeiger bieten Zugriff auf die Implementierungen der DLL der verschiedenen SSPI-Funktionen.

2.  Informationen zu den unterstützten Sicherheitspaketen müssen abgerufen werden.

    Während die meisten Anwendungen Sicherheitspakete verwenden, die Standardfunktionen oder allgemeine Funktionen unterstützen, können Sicherheitspakete eindeutige Funktionen aufweisen, die für die Anwendung von Interesse sind. Eine Anwendung, die spezielle Funktionen benötigt, kann ein Paket verwenden, das diese Funktionen bietet. Weitere Informationen finden Sie unter [Abrufen von Informationen zu Sicherheitspaketen.](getting-information-about-security-packages.md)

An diesem Punkt hat die Anwendung erfolgreich einen SSP initialisiert und ein Sicherheitspaket mit ausreichenden Funktionen ausgewählt.

Das [*Negotiate-Paket*](../secgloss/n-gly.md) kann verwendet werden, wenn die Vereinbarung zwischen Client und Server über das zu verwendende [*Sicherheitspaket*](../secgloss/s-gly.md) im Hintergrund erfolgt. Wenn das Negotiate-Paket nicht verwendet wird, müssen sich Client und Server auf das spezifische Sicherheitspaket einigen, das verwendet werden soll, bevor die obigen Setupschritte ausgeführt werden.

 

 
