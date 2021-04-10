---
description: Die iupdateingestallationresult-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Iupdateingestallationresult-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214730"
---
# <a name="iupdateinstallationresult-properties"></a>Iupdateingestallationresult-Eigenschaften

Die [**iupdateingestallationresult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                           | BESCHREIBUNG                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HRESULT**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | Ruft den **HRESULT** -Ausnahme Wert ab, der während des Vorgangs bei einem Update ausgelöst wird.                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | Ruft einen booleschen Wert ab, der angibt, ob auf einem Computer ein Systemneustart erforderlich ist, um die Installation eines Updates abzuschließen. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | Ruft einen [**operationresultcode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) -Wert ab, der das Ergebnis eines Vorgangs bei einem Update angibt.          |



 

 

 



