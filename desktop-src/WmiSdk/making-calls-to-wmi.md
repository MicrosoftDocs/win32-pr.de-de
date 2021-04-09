---
description: Anbieter können von WMI implementierte Methoden in ihren Methoden Implementierungen abrufen.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Aufrufen von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042305"
---
# <a name="making-calls-to-wmi"></a>Aufrufen von WMI

Anbieter können von WMI implementierte Methoden in ihren Methoden Implementierungen abrufen. Es gibt jedoch besondere Überlegungen, wenn ein Anbieter die WMI-Implementierung einer [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methode aus einer eigenen Implementierung derselben Methode aufruft. Diese Überlegungen sind unabhängig davon wichtig, ob der Anbieter die synchrone oder asynchrone Version der Methode aufruft.

Jede [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methode, die ein Anbieter implementieren kann, verfügt über einen *pctX* -Parameter, einen Zeiger auf eine [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Schnittstellen Implementierung. Wenn WMI den Anbieter aufruft, übergibt WMI einen gültigen Zeiger in diesem Parameter. Ein Anbieter muss denselben Zeiger immer bei WMI-aufrufen übergeben, die er während der Wartung von Anforderungen vornimmt. Die angemessene Festlegung von *pctX* kann bewirken, dass WMI eine Endlosschleife startet.

Das folgende Codebeispiel zeigt die korrekte Methode zum Aufrufen der WMI-Implementierung von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) aus einer Implementierung von [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).


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



Für das C++-Codebeispiel in diesem Thema sind die folgenden Verweise und \# include-Anweisungen erforderlich, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Instanzen, Klassen und Eigenschaften Anbieter dürfen keine Aufrufe von WMI ausgeben, die die Änderung von Daten anfordern, während eine Lese Anforderung verarbeitet wird. Die einzigen Anbieter, die Ausnahmen für diese Regel sind, sind pushanbieter. Ein Push-Anbieter ist ein Klassen Anbieter, der Daten im WMI-Repository speichert und von WMI zum Verarbeiten von Anforderungen von Clients abhängig ist. Bei der Verarbeitung einer Lese Anforderung kann ein pushanbieter zwar das WMI-Repository aktualisieren, muss den *lFlags* -Parameter jedoch im entsprechenden [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Befehl auf das **WBEM- \_ Flag " \_ Besitzer \_ Update** " festlegen.

Ereignis Anbieter dürfen während der Wartung eines Aufrufes keine Klassenänderungen vornehmen. Sie können auch keine ereignisbezogenen Aufrufe ausgeben, wie z. b. das Ändern eines Ereignis Filters.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sichern Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 



