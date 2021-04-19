---
description: Basierend auf dem Rückgabecode von einem vorherigen aufrufungskontext (allgemein) kann der Server auf eine Antwort vom Client warten und an zusätzlichen Austausch Vorgängen mit dem Client teilnehmen.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Server Fortsetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349195"
---
# <a name="server-continuation"></a>Server Fortsetzung

Basierend auf dem Rückgabecode von einem vorherigen [**aufrufungskontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)kann der Server auf eine Antwort vom Client warten und an zusätzlichen Austausch Vorgängen mit dem Client teilnehmen. Um das Authentifizierungsprotokoll fortzusetzen, wiederholt der Server Aufrufe von " **akzeptsecuritycontext (allgemein)**".

Der von " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) " zurückgegebene Status wird geprüft, um festzustellen, ob der Server auf Weitere Nachrichten vom Client warten muss. In den meisten Authentifizierungs Protokollen gibt es eine maximale Anzahl von Austausch Vorgängen für die gegenseitige Authentifizierung. Derzeit führen sowohl die NTLM-als auch die [*Kerberos-Protokolle*](../secgloss/k-gly.md) gegenseitige Authentifizierung mit drei Austausch Vorgängen durch.

 

 
