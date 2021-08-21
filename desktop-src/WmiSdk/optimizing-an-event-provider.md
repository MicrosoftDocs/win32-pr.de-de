---
description: Ein Ereignisanbieter kann sehr viel Zeit für das Erstellen von Ereignissen auf sich haben.
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: Optimieren eines Ereignisanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613fa6b054f979d0f7d1a33a87f927df9ef129a280cf7cd1675cbe0cf9818473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923407"
---
# <a name="optimizing-an-event-provider"></a>Optimieren eines Ereignisanbieters

Ein Ereignisanbieter kann sehr viel Zeit für das Erstellen von Ereignissen auf sich haben. Wenn keine Clientanwendungen die erstellten Ereignisse verwenden, verschwendung der Anbieter Systemressourcen. Darüber hinaus gibt WMI eine beträchtliche Menge an Ressourcen für die Analyse und das Senden komplexer Abfragen an den entsprechenden Anbieter aus. Um die Verschwendung von Systemressourcen zu vermeiden und die Leistung Ihres Ereignisanbieters zu verbessern, können Sie die [**IWbemEventProviderQuerySink-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) implementieren. **IWbemEventProviderQuerySink** überwacht die Abfragen, die Clientanwendungen mithilfe der [**Methoden NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) und [**CancelQuery bei**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) WMI registrieren. Durch die Überwachung der registrierten Clientabfragen kann Ihr Anbieter bestimmen, was passiert, wenn Nachrichten an WMI gesendet werden müssen.

WMI ruft [**NewQuery für**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) einen Ereignisanbieter auf, wenn ein Clientverbraucher eine Ereignisfilterabfrage registriert, die Verweise auf Ereignisse enthält, die von diesem Ereignisanbieter unterstützt werden. Daher kann der Ereignisanbieter, der für Instanzänderungsereignisse für die **EmailClass-Klasse** verantwortlich ist, so eingerichtet werden, dass nur Benachrichtigungen für den Absender **generiert werden.** Wenn der Anbieter eine Abfrage empfängt, die eine Benachrichtigung über Änderungen an der **subject-Eigenschaft** anfragt, kann der Anbieter mit dem Generieren dieser Benachrichtigungen beginnen. In diesem Szenario ist WMI nicht erforderlich, um die Benachrichtigungen zu verwerfen, die nur **Empfängeränderungen** melden.

Auf ähnliche Weise ruft WMI [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) für einen Ereignisanbieter auf, wenn ein Clientverbraucher die Registrierung einer Ereignisfilterabfrage aufbricht, die Verweise auf Ereignisse enthält, die vom Ereignisanbieter unterstützt werden. Der Zweck von **CancelQuery** besteht darin, dass der Ereignisanbieter die Liste der ereignisse aktualisiert, die gesendet werden sollen.

> [!Note]  
> Wenn Ihr Anbieter [**sowohl IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) als auch [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)unterstützt, stellen Sie sicher, dass Ihre Implementierung der **IUnknown::QueryInterface-Methode** Zeiger auf beide Schnittstellen zurückgibt.

 

 

 



