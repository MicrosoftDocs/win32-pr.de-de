---
description: Die-API enthält einen Mechanismus, mit dem Anbieter von Dienstanbietern die telefonieapi mithilfe von gerätespezifischen Erweiterungen erweitern können.
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: Erweiterte Telefoniedienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a319f59f51643fb5bf13ec95800d40ffa6d8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363461"
---
# <a name="extended-telephony-services"></a>Erweiterte Telefoniedienste

Die-API enthält einen Mechanismus, mit dem Anbieter von Dienstanbietern die telefonieapi mithilfe von gerätespezifischen Erweiterungen erweitern können. Erweiterte Telefoniedienste (oder gerätespezifische Dienste) beinhalten alle Erweiterungen der API, die von einem bestimmten Dienstanbieter definiert werden. Da die API nur den Erweiterungsmechanismus definiert, muss der Dienstanbieter die Definition des Extended-Telephony Dienst Verhaltens vollständig angeben.

## <a name="tapi-2x-extended-telephony"></a>Erweiterte Telefonie von TAPI 2. x

Der Erweiterungsmechanismus ermöglicht Anbietern von Dienstanbietern das Definieren neuer Werte für einige Enumerationstypen und Bitflags und das Hinzufügen von Membern zu den meisten Datenstrukturen. Die Interpretation der Erweiterungen wird von der Erweiterungs-ID des Dienstanbieters abgeblendet, einem Bezeichner für die Spezifikation des unterstützten Erweiterungs Satzes, der mehrere Hersteller überschreiten kann. Spezielle Funktionen und Meldungen wie [**linedevspecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) und [**phonedevspecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) werden in der API bereitgestellt, damit eine Anwendung direkt mit einem Dienstanbieter kommunizieren kann. Der Dienstanbieter definiert auch die Parameter für jede Funktion.

Es ist nicht erforderlich, dass sich die Anbieter registrieren, um den Erweiterungs bezeichtern zugewiesen zu werden. Stattdessen wird im Platform Software Development Kit (SDK) ein Hilfsprogramm mit dem Namen extidgen (Extidgen.exe) bereitgestellt, das die lokale Generierung von Erweiterungs bezeichlern ermöglicht. Dieser eindeutige Bezeichner besteht aus einer Ethernet-Adapter Adresse, einer Zufallszahl und der Tageszeit. Ein Bezeichner wird einem Satz von Erweiterungen (vor der Verteilung) zugewiesen, nicht für jede einzelne Instanz einer Implementierung dieser Erweiterungen.

 

 
