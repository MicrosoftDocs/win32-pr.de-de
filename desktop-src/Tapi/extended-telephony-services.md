---
description: Die API enthält einen Mechanismus, mit dem Anbieter von Dienstanbietern die Telefonie-API mit gerätespezifischen Erweiterungen erweitern können.
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: Erweiterte Telefoniedienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403f57904138b3797069222875086b0a4990b8e625f701f380120d65c235784e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140703"
---
# <a name="extended-telephony-services"></a>Erweiterte Telefoniedienste

Die API enthält einen Mechanismus, mit dem Anbieter von Dienstanbietern die Telefonie-API mit gerätespezifischen Erweiterungen erweitern können. Erweiterte Telefoniedienste (oder gerätespezifische Dienste) enthalten alle Erweiterungen der API, die von einem bestimmten Dienstanbieter definiert wurden. Da die API nur den Erweiterungsmechanismus definiert, muss der Dienstanbieter die Definition des Dienstverhaltens vollständig Extended-Telephony angeben.

## <a name="tapi-2x-extended-telephony"></a>TAPI 2.x Erweiterte Telefonie

Der Erweiterungsmechanismus ermöglicht es Dienstanbieteranbietern, neue Werte für einige Enumerationstypen und Bitflags zu definieren und den meisten Datenstrukturen Member hinzuzufügen. Die Interpretation von Erweiterungen wird vom Erweiterungsbezeichner des Dienstanbieters abgeschlüsselt. Dies ist ein Bezeichner für die Spezifikation der unterstützten Erweiterungen, die möglicherweise mehrere Hersteller übergreifend sind. Spezielle Funktionen und Nachrichten wie [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) und [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) werden in der API bereitgestellt, damit eine Anwendung direkt mit einem Dienstanbieter kommunizieren kann. Der Dienstanbieter definiert auch die Parameter für jede Funktion.

Anbieter müssen sich nicht registrieren, um Erweiterungsbezeichnern zugewiesen zu werden. Stattdessen wird im Platform Software Development Kit (SDK) ein Hilfsprogramm namens EXTIDGEN (Extidgen.exe) bereitgestellt, das die lokale Generierung von Erweiterungsbezeichnern ermöglicht. Dieser eindeutige Bezeichner besteht aus einer Ethernet-Adapteradresse, einer Zufallszahl und der Tageszeit. Ein Bezeichner wird einem Satz von Erweiterungen (vor der Verteilung) zugewiesen, nicht jeder einzelnen Instanz einer Implementierung dieser Erweiterungen.

 

 
