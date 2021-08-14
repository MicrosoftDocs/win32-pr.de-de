---
description: Ergänzende Telefoniedienste sind die Sammlung aller dienste, die von der API definiert werden, mit Denen, die nicht in der Teilmenge "Basic-Telefonie" enthalten sind.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Ergänzende Telefoniedienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9762b2d9ca74d0212170e1e87662242d3983663db024ce52018d108cc37fb883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760752"
---
# <a name="supplementary-telephony-services"></a>Ergänzende Telefoniedienste

Ergänzende Telefoniedienste sind die Sammlung aller dienste, die von der API definiert werden, mit Denen, die nicht in der Teilmenge "Basic-Telefonie" enthalten sind. Sie enthält alle so genannten ergänzenden Features, die auf modernen PBX-Dateien zu finden sind, z. B. Hold, Transfer, Conference, Park und so weiter. Alle ergänzenden Features werden als optional betrachtet. Das heißt, der Dienstanbieter entscheidet, welche dieser Dienste er bietet oder nicht.

Eine Anwendung kann eine Linie oder ein Telefongerät mithilfe von Funktionen wie [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) oder [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)nach dem Satz zusätzlicher Dienste abfragen. Ein einzelner ergänzender Dienst kann aus mehreren Funktionsaufrufen und Nachrichten bestehen. Die Telefonie-API und nicht der Entwickler des Dienstanbieters definiert das Verhalten der einzelnen ergänzenden Features. Ein Dienstanbieter sollte nur dann einen ergänzenden Telefoniedienst bereitstellen, wenn er die genaue Bedeutung implementieren kann, wie von der API definiert. Falls nicht, sollte das Feature als erweiterter Telefoniedienst bereitgestellt werden.

Wie unter Grundlegende Telefoniedienste erwähnt, werden Telefongerätedienste als optional betrachtet. Daher sind alle Telefongerätedienste Teil der ergänzenden Telefonie. Eine Liste der Funktionen der ergänzenden Telefonie finden Sie in der [TAPI-Kurzfunktionsreferenz.](./tapi-quick-function-reference.md)

 

 
