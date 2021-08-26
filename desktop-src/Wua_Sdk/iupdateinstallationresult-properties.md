---
description: Die IUpdateInstallationResult-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: IUpdateInstallationResult-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7574d6fd84afc737d67147c8b40e1e501857f6c19d69bcce4b4b7216bb9c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994410"
---
# <a name="iupdateinstallationresult-properties"></a>IUpdateInstallationResult-Eigenschaften

Die [**IUpdateInstallationResult-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) definiert die folgenden Eigenschaften.



| Eigenschaft                                                           | BESCHREIBUNG                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Hresult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | Ruft den **HRESULT-Ausnahmewert** ab, der während des Vorgangs für ein Update ausgelöst wird.                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | Ruft einen booleschen Wert ab, der angibt, ob ein Systemneustart auf einem Computer erforderlich ist, um die Installation eines Updates abzuschließen. |
| [**Resultcode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | Ruft einen [**OperationResultCode-Wert**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) ab, der das Ergebnis eines Vorgangs für ein Update angibt.          |



 

 

 



