---
description: Ein Anbieter ist nicht erforderlich, um Teilinstanzvorgänge zu unterstützen. Ein Anbieter muss jedoch entweder die gesamte Semantik eines partiellen Instanzvorgangs unterstützen, eine vollständige Instanz verarbeiten oder WBEM \_ E \_ UNSUPPORTED \_ PARAMETER zurückgeben.
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Unterstützen von Partial-Instance Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2043c09ca129acab6976cabda2b854be464d26036cb5b9df1bc5b82989ccc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922850"
---
# <a name="supporting-partial-instance-operations"></a>Unterstützen von Partial-Instance Vorgängen

Ein Anbieter ist nicht erforderlich, um Teilinstanzvorgänge zu unterstützen. Ein Anbieter muss jedoch entweder die gesamte Semantik eines partiellen Instanzvorgangs unterstützen, eine vollständige Instanz verarbeiten oder **WBEM \_ E \_ UNSUPPORTED \_ PARAMETER** zurückgeben.

Beim Erstellen eines Anbieters, der Teilinstanzvorgänge unterstützt, müssen Sie die folgenden Regeln beachten:

-   Verwenden Sie dasselbe Kontextobjekt wieder, das WMI an den Anbieter sendet. WMI verwendet den \_ \_ benannten Wert "GET \_ EXT \_ CLIENT \_ REQUEST", um Deadlocks zu verhindern und diesen Client zu entfernen, bevor das Kontextobjekt an einen Anbieter weitergeleitet wird.
-   Stellen Sie bei erneuten Aufrufen an WMI, die keinen Teilinstanzvorgang erfordern, sicher, dass dasselbe Kontextobjekt ohne Änderungen zurückübergibt. WMI empfängt das Kontextobjekt ohne den \_ \_ benannten Wertsatz "GET \_ EXT \_ CLIENT \_ REQUEST" und löscht alle benannten Werte, die Teilinstanzvorgängen zugeordnet sind, aus dem Kontextobjekt, bevor es an andere Anbieter übergeben wird. Wenn das Kontextobjekt nicht geändert wird, wird verhindert, dass andere Anbieter Teilweiseinstanzabrufvorgänge empfangen, die für ein anderes, nicht verknüpftes Objekt vorgesehen sind.
-   Legen Sie den fehlenden "GET EXT CLIENT REQUEST"-Wert und die fehlende \_ \_ Eigenschaft "GET EXT CLIENT REQUEST" als \_ \_ "clear" fest, um einen erneuten, teilweisen Instanzvorgang auszuführen, während eine Anforderung ausgeführt \_ wird. Optional können Sie die Eigenschaften im \_ \_ benannten Wert "GET EXT PROPERTIES" ändern, \_ bevor Sie das \_ Kontextobjekt mit dem erneuten Aufruf an WMI zurücksenden.
-   Greifen Sie nicht auf das Kontextobjekt zu, nachdem Sie es während eines erneuten Aufrufs an WMI zurückgegeben haben. andere Anbieter können die Eigenschaftenlisten oder andere Werte während der Erneutinvarianz ändern. Sie können das Kontextobjekt nur für die Dauer des von Ihnen implementierten [**IWbemServices-Aufrufs**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) untersuchen oder ändern.

 

 



