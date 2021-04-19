---
description: Zertifikate können über einen beliebigen Transportmechanismus angefordert und verteilt werden.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Transport Unabhängigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348472"
---
# <a name="transport-independence"></a>Transport Unabhängigkeit

Zertifikate können über einen beliebigen Transportmechanismus angefordert und verteilt werden. Zertifikat Dienste akzeptieren [*Zertifikat Anforderungen*](../secgloss/c-gly.md) von einem Antragsteller über HTTP, DCOM, RPC, eine Datenträger Datei oder einen benutzerdefinierten Transport. Zertifikat Dienste stellen Zertifikate an den Antragsteller über HTTP, DCOM, RPC, Datenträger Datei oder benutzerdefinierten Transport.

Transporte werden von Vermittler Anwendungen und Beendigungs Modul-DLLs unterstützt, die in der Regel in C/C++ geschrieben sind. Die zwischengeschalteten Anwendungen und Exit-Module isolieren Zertifikat Dienstfunktionen von der Kommunikation mit einem bestimmten Transport.

 

 
