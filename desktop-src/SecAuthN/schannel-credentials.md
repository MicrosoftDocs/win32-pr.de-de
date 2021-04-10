---
description: SChannel-Protokolle erfordern Anmelde Informationen, um Server und optional Clients zu authentifizieren.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: SChannel-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959636"
---
# <a name="schannel-credentials"></a>SChannel-Anmelde Informationen

SChannel-Protokolle erfordern Anmelde Informationen, um Server und optional Clients zu authentifizieren. Die Server Authentifizierung, bei der der Server einen Nachweis seiner Identität für den Client bereitstellt, ist für die SChannel- [*Sicherheitsprotokolle*](../secgloss/s-gly.md)erforderlich. Die Client Authentifizierung kann vom Server jederzeit angefordert werden.

SChannel-Anmelde Informationen sind [*X. 509*](../secgloss/x-gly.md) -Zertifikate. Informationen zu [*öffentlichen*](../secgloss/p-gly.md) und [*privaten Schlüsseln*](../secgloss/p-gly.md) von Zertifikaten werden verwendet, um den Server und optional den Client zu authentifizieren. Diese Schlüssel werden auch zum Bereitstellen der Nachrichten [*Integrität*](../secgloss/i-gly.md) verwendet, während der Client und der Server die zum Generieren und Austauschen von [*Sitzungs Schlüsseln*](../secgloss/s-gly.md)erforderlichen Informationen austauschen.

Informationen zur Programmierung finden Sie unter [beschaffen von SChannel-Anmelde](obtaining-schannel-credentials.md)Informationen.

 

 
