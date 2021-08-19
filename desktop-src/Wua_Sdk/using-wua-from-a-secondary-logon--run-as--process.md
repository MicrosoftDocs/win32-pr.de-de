---
description: Updates, für die eine Benutzerinteraktion erforderlich ist, können nicht von WUA-Anwendungen (Windows Update Agent) installiert werden, wenn die WUA-Anwendungen im Kontext des sekundären Anmeldediensts ausgeführt werden.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Verwenden von WUA aus einem sekundären Anmeldeprozess (ausführen als)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a659b9c46429100393138751039fdc1ce529191970a35c76d36e45bb16eb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049088"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>Verwenden von WUA aus einem sekundären Anmeldeprozess (ausführen als)

Updates, für die eine Benutzerinteraktion erforderlich ist, können nicht von WUA-Anwendungen (Windows Update Agent) installiert werden, wenn die WUA-Anwendungen im Kontext des sekundären Anmeldediensts ausgeführt werden.

Wenn der Prozess, der WUA aufruft, im Kontext des RunAs-Diensts oder des sekundären Anmeldediensts ausgeführt wird, schlägt ein Versuch, ein Update zu installieren, das eine Benutzerinteraktion erfordert, fehl und gibt den **WU E NO INTERACTIVE \_ \_ \_ \_ USER-Fehler** zurück.

In Microsoft Windows können Sie Programme als Benutzer ausführen, der sich von dem benutzer unterscheidet, der gerade angemeldet ist. Hierzu muss der sekundäre Anmeldedienst ausgeführt werden.

 

 



