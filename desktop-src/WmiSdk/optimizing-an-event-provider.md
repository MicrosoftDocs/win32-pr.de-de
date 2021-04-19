---
description: Ein Ereignis Anbieter kann sehr viel Zeit für das Erstellen von Ereignissen aufwenden.
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: Optimieren eines Ereignis Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70eaabfbbd462b831059b10590d7959bdef05cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352546"
---
# <a name="optimizing-an-event-provider"></a>Optimieren eines Ereignis Anbieters

Ein Ereignis Anbieter kann sehr viel Zeit für das Erstellen von Ereignissen aufwenden. Wenn keine Client Anwendungen die erstellten Ereignisse verwenden, verschwendet der Anbieter Systemressourcen. Außerdem verbringt WMI eine beträchtliche Menge an Ressourcen und sendet komplexe Abfragen an den entsprechenden Anbieter. Um die Verschwendung von Systemressourcen zu vermeiden und die Leistung Ihres Ereignis Anbieters zu verbessern, können Sie die [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) -Schnittstelle implementieren. **IWbemEventProviderQuerySink** überwacht die Abfragen, die von Client Anwendungen bei WMI registriert werden, mithilfe der [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) -Methode und der [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) -Methode. Wenn Sie die registrierten Client Abfragen überwachen, kann der Anbieter ermitteln, ob Nachrichten an WMI gesendet werden müssen.

WMI ruft [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) für einen Ereignis Anbieter auf, wenn ein Client Consumer eine Ereignis Filter Abfrage registriert, die Verweise auf Ereignisse enthält, die von diesem Ereignis Anbieter unterstützt werden. Daher kann der Ereignis Anbieter, der für Instanzen Änderungs Ereignisse für die **emailclass** -Klasse verantwortlich ist, so eingerichtet werden, dass nur Benachrichtigungen für den **Absender** generiert werden. Wenn der Anbieter eine Abfrage empfängt, die eine Benachrichtigung über Änderungen an der Eigenschaft " **Subject** " anfordert, kann der Anbieter damit beginnen, diese Benachrichtigungen zu erstellen. In diesem Szenario ist es nicht erforderlich, dass WMI die Benachrichtigungen verwerfen, die nur vom **Empfänger des Empfängers** geändert werden.

Ebenso ruft WMI [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) für einen Ereignis Anbieter auf, wenn ein Client Consumer eine Ereignis Filter Abfrage deregister, die Verweise auf Ereignisse enthält, die vom Ereignis Anbieter unterstützt werden. Der Zweck von **CancelQuery** besteht darin, dass der Ereignis Anbieter die Liste der Ereignisse aktualisiert, die gesendet werden sollen.

> [!Note]  
> Wenn Ihr Anbieter sowohl [**iwbemeventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) als auch [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)unterstützt, stellen Sie sicher, dass die Implementierung der **IUnknown:: QueryInterface** -Methode Zeiger auf beide Schnittstellen zurückgibt.

 

 

 



