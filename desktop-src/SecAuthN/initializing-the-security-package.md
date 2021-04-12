---
description: Listet die Schritte auf, die zum Initialisieren eines Sicherheitspakets erforderlich sind, und erläutert diese.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Initialisieren des Sicherheitspakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131181"
---
# <a name="initializing-the-security-package"></a>Initialisieren des Sicherheitspakets

Diese Schritte sind vor der Verwendung von SSPI erforderlich:

1.  Die Initialisierungsfunktion muss aufgerufen werden, um die Adresse der Sicherheits Funktions Tabelle abzurufen.

    Der Client und der Server aufrufen [**initsecurityinterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) für einen Zeiger auf eine [**securityfunctiontable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) Dispatch-Tabelle. Diese Tabelle enthält Zeiger auf Rückruf Funktionen, die in SSPI. h deklariert werden. Diese Zeiger ermöglichen den Zugriff auf die dll-Implementierungen der verschiedenen SSPI-Funktionen.

2.  Informationen zu den unterstützten Sicherheitspaketen finden Sie hier.

    Wenngleich die meisten Anwendungen Sicherheitspakete verwenden, die standardmäßige oder allgemeine Funktionen unterstützen, können Sicherheitspakete über einzigartige Funktionen für die Anwendung verfügen. Eine Anwendung, die besondere Funktionen benötigt, kann ein Paket verwenden, das diese Funktionen bietet. Weitere Informationen finden Sie unter [Informationen zu Sicherheitspaketen](getting-information-about-security-packages.md).

An diesem Punkt hat die Anwendung einen SSP erfolgreich initialisiert und ein Sicherheitspaket mit ausreichenden Funktionen ausgewählt.

Das [*Aushandlungs*](../secgloss/n-gly.md) Paket kann verwendet werden, wenn eine Vereinbarung zwischen Client und Server verwendet wird, um zu erfahren, welches [*Sicherheitspaket*](../secgloss/s-gly.md) verwendet werden soll. Wenn das Aushandlungs Paket nicht verwendet wird, müssen der Client und der Server dem spezifischen Sicherheitspaket zustimmen, das verwendet werden soll, bevor die obigen Setup Schritte ausgeführt werden.

 

 
