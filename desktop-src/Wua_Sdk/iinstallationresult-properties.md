---
description: Die iinstallationresult-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Iinstallationresult-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041790"
---
# <a name="iinstallationresult-properties"></a>Iinstallationresult-Eigenschaften

Die [**iinstallationresult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                     | BESCHREIBUNG                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**HRESULT**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | Ruft das **HRESULT** der Ausnahme ab, sofern vorhanden, das während der Installation ausgelöst wird.                                                 |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | Ruft einen booleschen Wert ab, der angibt, ob der Computer neu gestartet werden muss, um die Installation oder die Installation eines Updates abzuschließen. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | Ruft einen [**operationresultcode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) -Wert ab, der das Ergebnis eines Vorgangs bei einem Update angibt.               |



 

 

 



