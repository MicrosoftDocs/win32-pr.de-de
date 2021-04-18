---
description: Ein Anbieter muss keine partiellen instanzvorgänge unterstützen. Ein Anbieter muss jedoch entweder die gesamte Semantik eines partiellen instanzvorgangs unterstützen, eine vollständige Instanz verarbeiten oder den \_ nicht unterstützten WBEM E-Parameter zurückgeben \_ \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Unterstützung Partial-Instance Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347317"
---
# <a name="supporting-partial-instance-operations"></a>Unterstützung Partial-Instance Vorgänge

Ein Anbieter muss keine partiellen instanzvorgänge unterstützen. Ein Anbieter muss jedoch entweder die gesamte Semantik eines partiellen instanzvorgangs unterstützen, eine vollständige Instanz verarbeiten oder den **\_ \_ nicht unterstützten \_ WBEM E-Parameter** zurückgeben.

Beim Erstellen eines Anbieters, der partielle instanzvorgänge unterstützt, müssen Sie die folgenden Regeln beachten:

-   Wieder verwenden des gleichen Kontext Objekts, das von WMI an den Anbieter gesendet wird. WMI verwendet den \_ \_ \_ benannten Wert "Get Ext \_ Client \_ Request", um Deadlocks zu verhindern und den Client zu entfernen, bevor das Kontext Objekt an einen Anbieter weitergeleitet wird.
-   Für Wiedereintritts fähige Aufrufe an WMI, die keinen partiellen Instanzvorgang erfordern, müssen Sie sicherstellen, dass das gleiche Kontext Objekt ohne Änderungen zurückgegeben wird. WMI empfängt das Kontext Objekt ohne den \_ \_ \_ benannten Wert "Get Ext \_ Client \_ Request" und löscht alle benannten Werte, die partiellen instanzvorgängen zugeordnet sind, aus dem Kontext Objekt, bevor es an andere Anbieter übergeben wird. Wenn Sie das Kontext Objekt nicht ändern, werden von anderen Anbietern keine partiellen Instanzen Abruf Vorgänge empfangen, die für ein anderes, nicht verwandtes Objekt vorgesehen sind.
-   Zum Ausführen eines wieder eintretende partiellen instanzvorgangs bei der Ausführung einer Anforderung legen Sie den fehlenden " \_ \_ get \_ Ext \_ Client \_ Request"-Wert und die Eigenschaft "Clear" fest. Optional können Sie die Eigenschaften im \_ \_ \_ benannten Wert "Get Ext \_ Properties" ändern, bevor Sie das Kontext Objekt mit dem Wiedereintritts fähige-Befehl zurück an WMI senden.
-   Greifen Sie nicht auf das Kontext Objekt zu, nachdem Sie es während eines Wiedereinstiegs Aufrufes an WMI zurückgegeben haben. andere Anbieter können die Eigenschaften Listen oder andere Werte während des erneuten Eintritts ändern. Sie können das Kontext Objekt nur für die Dauer des von Ihnen implementierten [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Aufrufes überprüfen oder ändern.

 

 



