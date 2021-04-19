---
description: Sockaddr-Strukturen und Annahmen der Byte Reihenfolge in Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Annahmen der Byte Reihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346943"
---
# <a name="byte-ordering-assumptions"></a>Annahmen der Byte Reihenfolge

Ein Dienstanbieter sollte alle [**sockaddr**](sockaddr-2.md) -Komponenten, die vom Adress familienparameter ausgenommen sind, so behandeln, als ob Sie sich in der Netzwerk-Byte Reihenfolge befinden, und der Adress familienparameter wie in der Byte Reihenfolge des lokalen Computers. Es liegt in der Verantwortung der Winsock-Anwendung, sicherzustellen, dass die in **sockaddr** -Strukturen enthaltenen Adressen ordnungsgemäß angeordnet sind. Die Winsock-API bietet eine Reihe von Konvertierungs Routinen, um diese Aufgabe zu vereinfachen. Derzeit verstehen diese Routinen die Konvertierung zwischen der natürlichen Byte Reihenfolge des lokalen Hosts und der Bytesortierung von Big-Endian oder Little-Endian. Die Winsock-Architektur kann in Zukunft andere Byte Reihenfolge Schemas unterstützen.

 

 



