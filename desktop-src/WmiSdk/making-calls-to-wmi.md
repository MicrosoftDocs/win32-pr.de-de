---
description: Anbieter können von WMI implementierte Methoden aus ihren Methodenimplementierungen aufrufen.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Aufrufen von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76adae33db786a8174879e6c7e88b62fb69f3c59598ae7f055f41865b32dbf7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317674"
---
# <a name="making-calls-to-wmi"></a>Aufrufen von WMI

Anbieter können von WMI implementierte Methoden aus ihren Methodenimplementierungen aufrufen. Es gibt jedoch besondere Überlegungen, wenn ein Anbieter die WMI-Implementierung einer [**IWbemServices-Methode**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) innerhalb seiner eigenen Implementierung derselben Methode aufruft. Diese Überlegungen sind wichtig, unabhängig davon, ob der Anbieter die synchrone oder asynchrone Version der Methode aufruft.

Jede [**IWbemServices-Methode,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) die ein Anbieter implementieren kann, verfügt über einen *pCtx-Parameter,* einen Zeiger auf eine Implementierung der [**IWbemContext-Schnittstelle.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) Wenn WMI den Anbieter aufruft, übergibt WMI einen gültigen Zeiger in diesem Parameter. Ein Anbieter muss diesen Zeiger immer in allen Aufrufen von WMI übergeben, die er während der Wartung von Anforderungen vorgibt. Wenn Sie *pCtx* nicht ordnungsgemäß festlegen, kann dies dazu führen, dass WMI eine Endlosschleife startet.

Das folgende Codebeispiel zeigt die richtige Methode zum Aufrufen der WMI-Implementierung von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) aus einer Implementierung von [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



Das C++-Codebeispiel in diesem Thema erfordert die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Instanz-, Klassen- und Eigenschaftenanbieter dürfen keine Aufrufe von WMI ausstellen, die die Änderung von Daten während der Wartung einer Leseanforderung anfordern. Die einzigen Anbieter, die Ausnahmen von dieser Regel sind, sind Pushanbieter. Ein Pushanbieter ist ein Klassenanbieter, der Daten im WMI-Repository speichert und WMI für die Verarbeitung von Anforderungen von Clients verwendet. Während der Wartung einer Leseanforderung kann ein Pushanbieter das WMI-Repository aktualisieren, muss jedoch den *lFlags-Parameter* im entsprechenden [**IWbemServices-Aufruf**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) auf **WBEM \_ FLAG OWNER \_ \_ UPDATE** festlegen.

Ereignisanbieter dürfen während der Wartung eines Aufrufs keine Klassenänderungen vornehmen. Sie können auch keine ereignisbezogenen Aufrufe ausstellen, z. B. das Ändern eines Ereignisfilters.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Festlegen von Namepace-Sicherheitsbeschreibungen](setting-namespace-security-descriptors.md)
</dt> <dt>

[Schützen Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 



