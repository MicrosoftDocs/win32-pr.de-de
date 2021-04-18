---
description: Updates, für die eine Benutzerinteraktion erforderlich ist, können nicht von Windows Update-Agent (WUA)-Anwendungen installiert werden, wenn die WUA-Anwendungen im Kontext des sekundären Anmelde Diensts ausgeführt werden.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Verwenden von WUA über einen sekundären Anmeldungs Prozess (Ausführen als)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343323"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>Verwenden von WUA über einen sekundären Anmeldungs Prozess (Ausführen als)

Updates, für die eine Benutzerinteraktion erforderlich ist, können nicht von Windows Update-Agent (WUA)-Anwendungen installiert werden, wenn die WUA-Anwendungen im Kontext des sekundären Anmelde Diensts ausgeführt werden.

Wenn der Prozess, der WUA aufruft, im Kontext des runas-Diensts oder des sekundären Anmelde Diensts ausgeführt wird, tritt beim Versuch, ein Update zu installieren, für das eine Benutzerinteraktion erforderlich ist, **ein Fehler auf \_ \_ \_ \_** .

In Microsoft Windows können Sie Programme als Benutzer ausführen, der sich von dem aktuell angemeldeten Benutzer unterscheidet. Zu diesem Zweck muss der sekundäre Anmeldedienst ausgeführt werden.

 

 



