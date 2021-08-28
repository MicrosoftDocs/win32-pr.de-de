---
description: Ein Methodenanbieter sollte IWbemServices als primäre Schnittstelle implementieren. Ein reiner Methodenanbieter erfordert jedoch nur, dass Sie die IWbemServices::ExecMethodAsync-Methode implementieren.
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementieren der primären Schnittstelle für einen Methodenanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fcc698155ad0a9e786636045654b08d1cd2b7dfabd946b2d3ee9e8192485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244230"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Implementieren der primären Schnittstelle für einen Methodenanbieter

Ein Methodenanbieter sollte [**IWbemServices als**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) primäre Schnittstelle implementieren. Ein reiner Methodenanbieter erfordert jedoch nur, dass Sie die [**IWbemServices::ExecMethodAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) implementieren.

Da andere Anbieter [**IWbemServices verwenden,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)enthält die Schnittstelle viele Methoden, die für einen reinen Methodenanbieter irrelevant sind. Ihr reiner Methodenanbieter sollte eine Stubimplementierung bereitstellen, die WBEM E PROVIDER NOT CAPABLE für alle anderen \_ \_ \_ \_ **IWbemServices-Methoden** außer [**ExecMethodAsync zurückgibt.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) Viele Methodenanbieter dienen jedoch auch als Instanz- oder Klassenanbieter. Kombinationsmethoden- und Instanzanbieter müssen mehr **IWbemServices-Methoden** unterstützen.

 

 



