---
description: Stellt Schannel-spezifische Informationen zu einem Sicherheitskontext bereit.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Abfragen der Attribute eines Schannel-Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48f00f6d5f0660bbb3a0d4ce5890ab415325707dbda4087d025a010efdb3fd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919939"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Abfragen der Attribute eines Schannel-Kontexts

Die [**QueryContextAttributes (Schannel)-Funktion**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) stellt Schannel-spezifische Informationen zu einem [*Sicherheitskontext*](../secgloss/s-gly.md)bereit. Die meisten Informationen werden ursprünglich angegeben, wenn der Kontext mithilfe der Clientfunktion [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) oder des [**Servers AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) erstellt wird. Einige Informationen werden beim Abrufen eines Handles für die Anmeldeinformationen angegeben, die zum Erstellen des Kontexts verwendet werden. Weitere Informationen finden Sie unter [Abrufen von Schannel-Anmeldeinformationen.](obtaining-schannel-credentials.md)

 

 
