---
description: Sockaddr-Strukturen und Annahmen für die Bytebestellung in Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Annahmen für die Byte reihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21c1e680b0fe658994723b0a1d87c2a7d6adbf0a00a5452b185401b03099089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097910"
---
# <a name="byte-ordering-assumptions"></a>Annahmen für die Byte reihenfolge

Ein Dienstanbieter sollte alle [**Sockaddr-Komponenten,**](sockaddr-2.md) die den Adressfamilienparameter ausschließen, so behandeln, als ob sie sich in der Netzwerk-Byte-Reihenfolge befinden, und den Parameter für die Adressfamilie wie in der Byte reihenfolge des lokalen Computers. Es liegt in der Verantwortung der Winsock-Anwendung, sicherzustellen, dass adressen, die in **sockaddr-Strukturen** enthalten sind, ordnungsgemäß angeordnet sind. Die Winsock-API stellt eine Reihe von Konvertierungsroutinen bereit, um diese Aufgabe zu vereinfachen. Derzeit verstehen diese Routinen die Konvertierung zwischen der natürlichen Byte reihenfolge des lokalen Hosts und der Big-Endian- oder Little-Endian-Netzwerk-Byte reihenfolge. Die Winsock-Architektur kann in Zukunft andere Byte reihenfolgenschemas unterstützen.

 

 



