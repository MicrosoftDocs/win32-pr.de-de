---
description: Stellt SChannel-spezifische Informationen über einen Sicherheitskontext bereit.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Abfragen der Attribute eines SChannel-Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128284"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Abfragen der Attribute eines SChannel-Kontexts

Die [**QueryContextAttributes-Funktion (SChannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) stellt SChannel-spezifische Informationen über einen [*Sicherheitskontext*](../secgloss/s-gly.md)bereit. Die meisten Informationen werden ursprünglich angegeben, wenn der Kontext mithilfe der Client [**InitializeSecurityContext-Funktion (SChannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) oder der Server [**Akzeptanz Context-Funktion (SChannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) erstellt wird. Beim Abrufen eines Handles für die Anmelde Informationen, die zum Erstellen des Kontexts verwendet werden, werden einige Informationen angegeben. Weitere Informationen finden Sie unter Abrufen von [SChannel-Anmelde](obtaining-schannel-credentials.md)Informationen.

 

 
