---
description: 'Der Dispatch-Mapper wird mit COM CoCreateInstance erstellt und macht eine Schnittstelle verfügbar: ITDispatchMapper.'
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Dispatch-Mapper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0880228ab608abe5f599d58bb47d211d1458dd49636a9bdc992f31dfa26c028
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866684"
---
# <a name="dispatch-mapper"></a>Dispatch-Mapper

Der Dispatch-Mapper wird mit COM **CoCreateInstance** erstellt und macht eine Schnittstelle verfügbar: [**ITDispatchMapper.**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper) Mit dieser Schnittstelle kann eine Anwendung den Dispatchzeiger einer anderen Schnittstelle für ein Objekt abrufen, wenn der Verteilungszeiger einer Schnittstelle und die GUID einer anderen Schnittstelle angegeben werden. Diese Schnittstelle wird bereitgestellt, um Programmierer bei der Verwendung von Skriptanwendungen zu unterstützen, die keine Möglichkeit bieten, die Schnittstellen für ein Objekt einfach abzufragen.

Der Dispatch-Mapper verwendet die **IObjectSafety-Schnittstelle** eines Objekts, um sicherzustellen, dass das Objekt für die Skripterstellung auf der angeforderten Schnittstelle sicher ist. Wenn das Objekt **IObjectSafety** nicht implementiert oder das Objekt für diese bestimmte Schnittstelle nicht sicher ist, schlägt der Aufruf fehl.

 

 



