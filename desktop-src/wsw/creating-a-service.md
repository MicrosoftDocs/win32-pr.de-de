---
title: Erstellen eines Diensts
description: Das Erstellen eines Webdiensts wird in WWSAPI durch die Dienstmodell-API und das WsUtil.exe-Tool erheblich vereinfacht.
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f6daadbfcd1d06f76bf5bef97559214e36015d3f72ff440e77f4293a47ea57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805740"
---
# <a name="creating-a-service"></a>Erstellen eines Diensts

Das Erstellen eines Webdiensts wird in WWSAPI durch die [Dienstmodell-API](service-model-layer-overview.md) und das [WsUtil.exe-Tool ](wsutil-compiler-tool.md) erheblich vereinfacht. Das Dienstmodell stellt eine API bereit, mit der der Dienst und der Client [Nachrichten](message.md) über einen [Kanal](channel.md) als C-Methodenaufrufe senden und empfangen können. Das WsUtil-Tool generiert Stubs und Header für die Implementierung des Diensts.

## <a name="implementing-a-calculator-service-using-wwsapi"></a>Implementieren eines Rechnerdiensts mit WWSAPI

Implementieren Sie den Dienst mithilfe der generierten Quellen aus dem [Wsutil.exe](wsutil-compiler-tool.md) Tool, indem Sie die folgenden Schritte ausführen.

Schließen Sie die Header in Ihre Anwendungsquelle ein.

``` syntax
#include "CalculatorProxyStub.h"
```

Implementieren Sie die Dienstvorgänge. In diesem Beispiel sind die Dienstvorgänge die Funktionen Hinzufügen und Subtrahieren des Rechnerdiensts.

``` syntax
HRESULT CALLBACK Add (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a + b;
    printf ("%d + %d = %d\n", a, b, *result);
    return NOERROR;
}

HRESULT CALLBACK Subtract (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a - b;
    printf ("%d - %d = %d\n", a, b, *result);
    return NOERROR;
}
```

Definieren Sie den Dienstvertrag, indem Sie die Felder einer [**WS \_ SERVICE \_ CONTRACT-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) festlegen.

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

Erstellen Sie nun einen Diensthost, und öffnen Sie ihn für die Kommunikation.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
serviceEndpoint.uri.chars = L"https://+:80/example"; // address given as uri
serviceEndpoint.binding.channelBinding =  WS_HTTP_CHANNEL_BINDING; // channel binding for the endpoint
serviceEndpoint.channelType = WS_CHANNEL_TYPE_REPLY; // the channel type
serviceEndpoint.uri.length = (ULONG)wcslen(serviceEndpoint.uri.chars);
serviceEndpoint.contract = (WS_SERVICE_CONTRACT*)&calculatorContract;  // the contract
serviceEndpoint.properties = serviceProperties;
serviceEndpoint.propertyCount = WsCountOf(serviceProperties);

if (FAILED (hr = WsCreateServiceHost (&serviceEndpoint, 1, NULL, 0, &host, error)))
    goto Error;

// WsOpenServiceHost  to start the listeners in the service host 
if (FAILED (hr = WsOpenServiceHost (host, NULL, error)))
    goto Error;
```

Eine vollständige Implementierung des Rechnerdiensts finden Sie im Codebeispiel unter [HttpCalculatorServiceExample.](httpcalculatorserviceexample.md)

 

 




