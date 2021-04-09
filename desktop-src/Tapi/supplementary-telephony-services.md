---
description: Ergänzende Telefoniedienste sind die Auflistung aller Dienste, die durch die API definiert sind, außer denen, die in der grundlegenden telefonieteilmenge enthalten sind.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Ergänzende Telefoniedienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d93a7d12840e2001c6a2742e6bbd870d291e836
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864991"
---
# <a name="supplementary-telephony-services"></a>Ergänzende Telefoniedienste

Ergänzende Telefoniedienste sind die Auflistung aller Dienste, die durch die API definiert sind, außer denen, die in der grundlegenden telefonieteilmenge enthalten sind. Sie enthält alle so genannten ergänzenden Features, die auf modernen PBXs, wie z. b. Hold, Transfer, Conference, Park usw., gefunden werden. Alle ergänzenden Features gelten als optional. Dies bedeutet, dass der Dienstanbieter entscheidet, welche dieser Dienste Sie übernimmt oder nicht bereitstellt.

Eine Anwendung kann eine Zeile oder ein Telefongerät für die zusätzlichen Dienste Abfragen, die Sie mithilfe von Funktionen wie [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) oder [**linegetaddresscaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)bereitstellt. Ein einzelner zusätzlicher Dienst besteht möglicherweise aus mehreren Funktionsaufrufen und Nachrichten. Die Telefonie-API und nicht der Dienstanbieter Entwickler definiert das Verhalten der einzelnen ergänzenden Features. Ein Dienstanbieter sollte einen ergänzenden Telefoniedienst nur dann bereitstellen, wenn er die genaue Bedeutung implementieren kann, wie er durch die API definiert wurde. Andernfalls sollte die Funktion als erweiterter Telefoniedienst bereitgestellt werden.

Wie in grundlegenden Telefoniediensten erwähnt, werden Telefongeräte Dienste als optional eingestuft. Daher sind alle Telefongeräte Dienste Teil der ergänzenden Telefoniedienste. Eine Liste der Funktionen von ergänzenden Telefoniefunktionen finden Sie unter [TAPI-schnell Funktionsreferenz](./tapi-quick-function-reference.md).

 

 
