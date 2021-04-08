---
description: Ein Ereignis Anbieter muss die iwbemeventprovider-Schnittstelle implementieren, um Ereignis Benachrichtigungen zu generieren.
ms.assetid: ae33c9f5-61f7-4488-a281-01d7f9c62c46
ms.tgt_platform: multiple
title: Implementieren der primären Schnittstelle für einen Ereignis Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5621a2c6d0901a7925828149dd5c1480c2b11456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960219"
---
# <a name="implementing-the-primary-interface-for-an-event-provider"></a>Implementieren der primären Schnittstelle für einen Ereignis Anbieter

Ein Ereignis Anbieter muss die [**iwbemeventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) -Schnittstelle implementieren, um Ereignis Benachrichtigungen zu generieren. WMI Ruft die [**iwbemeventprovider::P rovideevents**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents) -Methode des Anbieters auf und übergibt einen Zeiger auf das sink-Objekt, das eine Implementierung der [**iwbewbjectsink**](iwbemobjectsink.md) -Schnittstelle ist. Wenn der Ereignis Anbieter bereit ist, eine Benachrichtigung zu generieren, ruft der Anbieter die Methode [**iwbexbjectsink::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) Notification auf.

Ein Ereignis Anbieter sollte die über [**iwbemeventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) generierten Benachrichtigungen in Ereignis Objekten platzieren. Sie sollten Ereignis Objekte als Einträge in einem Array von [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Schnittstellen implementieren, die durch den *ppobjarray* -Parameter der-Methode [**angegeben**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) werden. Da **iwbemclassobjects** com-Objekte sind, muss der Anbieter den Verweis Zähler für die Senke erhöhen, indem er die [**iwbemubjectsink:: adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode aufrufen. Ereignis Anbieter, die viele Benachrichtigungen bereitstellen müssen (z. b. 400-Ereignisse), sollten ein eindeutiges Ereignis Objekt für jede Benachrichtigung erstellen, indem Sie entweder eine neue Instanz erstellen oder eine vorhandene Klonen. WMI hält auf einem Ereignis Objekt nach dem Abschluss des Anzeige Aufrufes niemals an und hat keine besonderen Anforderungen an die **Adressier** Ende **Angabe** oberhalb und über den com-Standard.

Beachten Sie die folgenden Richtlinien, wenn Sie einen Ereignis Anbieter implementieren:

-   Nehmen Sie während der Wartung eines Client Aufrufes keine Klassenänderungen vor.
-   Geben Sie keine ereignisbezogenen Aufrufe aus, z. b. einen Aufruf, der einen Ereignis Filter ändert.
-   Verarbeiten Sie alle Anforderungen, die der Windows-Verwaltungsdienst ausgibt (z. b. [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery)), bevor Sie ein Ereignis erneut auslösen.

    Wenn Sie die Anforderung nicht verarbeiten, kann das erneute Auslösen des Ereignisses dazu führen, dass das Ereignis nicht mehr akzeptiert wird.

-   Niemals Aufrufen von [**iwbemubjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) innerhalb eines Anbieters.

 

 
