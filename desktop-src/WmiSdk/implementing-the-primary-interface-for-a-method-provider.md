---
description: 'Ein Methoden Anbieter sollte IWbemServices als primäre Schnittstelle implementieren. Allerdings erfordert ein reiner Methoden Anbieter nur, dass Sie die IWbemServices:: ExecMethodAsync-Methode implementieren.'
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementieren der primären Schnittstelle für einen Methoden Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352197"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Implementieren der primären Schnittstelle für einen Methoden Anbieter

Ein Methoden Anbieter sollte [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) als primäre Schnittstelle implementieren. Allerdings erfordert ein reiner Methoden Anbieter nur, dass Sie die [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) -Methode implementieren.

Da andere Anbieter [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)verwenden, enthält die-Schnittstelle viele Methoden, die für einen reinen Methoden Anbieter irrelevant sind. Der reine Methoden Anbieter sollte eine Stub-Implementierung bereitstellen, die den WBEM E-Anbieter zurückgibt, \_ \_ \_ \_ der nicht für alle anderen **IWbemServices** -Methoden außer [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)geeignet ist. Viele Methoden Anbieter dienen jedoch auch als Instanz-oder Klassen Anbieter. Kombinationen von Methoden-und instanzanbietern müssen mehr der **IWbemServices** -Methoden unterstützen.

 

 



