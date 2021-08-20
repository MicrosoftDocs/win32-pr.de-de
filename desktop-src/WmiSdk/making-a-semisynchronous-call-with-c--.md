---
description: Semisynchrone Aufrufe sind die empfohlene Methode zum Aufrufen von WMI-Methoden wie IWbemServices::ExecMethod und Anbietermethoden, z. B. die Chkdsk-Methode der Win32 \_ LogicalDisk-Klasse.
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Erstellen eines semisynchronen Aufrufs mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a550c5ad659ab9b640a1fcb3060b5f6cc7671f80c209d238cd859ad0ef6f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050698"
---
# <a name="making-a-semisynchronous-call-with-c"></a>Erstellen eines semisynchronen Aufrufs mit C++

Semisynchrone Aufrufe sind die empfohlene Methode zum Aufrufen von WMI-Methoden wie [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) und Anbietermethoden, z. B. die [**Chkdsk-Methode der Win32 \_ LogicalDisk-Klasse.**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk)

Ein Nachteil der synchronen Verarbeitung ist, dass der Aufruferthread blockiert wird, bis der Aufruf abgeschlossen ist. Die Blockierung kann zu einer Verzögerung der Verarbeitungszeit führen. Im Gegensatz dazu muss ein asynchroner Aufruf [**SWbemSink**](swbemsink.md) im Skript implementieren. In C++ muss asynchroner Code die [**IWbemObjectSink-Schnittstelle**](iwbemobjectsink.md) implementieren, mehrere Threads verwenden und den Informationsfluss zurück an den Aufrufer steuern. Große Resultsets aus Abfragen können z. B. viel Zeit in Anspruch nehmen, um die Übermittlung zu übermitteln, und der Aufrufer muss erhebliche Systemressourcen für die Übermittlung aufwenden.

Die semisynchrone Verarbeitung löst sowohl die Threadblockierung als auch unkontrollierte Übermittlungsprobleme, indem ein spezielles Statusobjekt abgerufen wird, das die [**IWbemCallResult-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) implementiert. Mit **IWbemCallResult** können Sie die Geschwindigkeit und Effizienz von Abfragen, Enumerationen und Ereignisbenachrichtigungen verbessern.

Im folgenden Verfahren wird beschrieben, wie ein semisynchroner Aufruf mit der [**IWbemServices-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) durchgeführt wird.

**So erstellen Sie einen semisynchronen Aufruf mit der IWbemServices-Schnittstelle**

1.  Rufen Sie wie gewohnt auf, aber wenn das **Flag WBEM \_ FLAG RETURN \_ \_ IMMEDIATELY** im *IFlags-Parameter* festgelegt ist.

    Sie können **WBEM \_ FLAG RETURN \_ \_ IMMEDIATELY** mit anderen Flags kombinieren, die für die jeweilige Methode gültig sind. Verwenden Sie beispielsweise das **Flag WBEM \_ FLAG FORWARD \_ \_ ONLY** für alle Aufrufe, die Enumeratoren zurückgeben. Das Festlegen dieser Flags in Kombination spart Zeit und Speicherplatz und verbessert die Reaktionsfähigkeit.

2.  Suchen Sie nach Ihren Ergebnissen.

    Wenn Sie eine Methode aufrufen, die einen Enumerator zurückgibt, z. B. [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) oder [**IWbemServices::ExecQuery,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)können Sie die Enumeratoren mit den Methoden [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) oder [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) abrufen. Der **IEnumWbemClassObject::NextAsync-Aufruf** ist nicht blockierend und gibt sofort zurück. Im Hintergrund beginnt WMI mit der Bereitstellung der angeforderten Anzahl von Objekten, indem [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)aufgerufen wird. WMI beendet dann und wartet auf einen weiteren **NextAsync-Aufruf.**

    Wenn Sie eine Methode aufrufen, die keinen Enumerator zurückgibt, z. [**B. IWbemServices::GetObject,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)müssen Sie den *ppCallResult-Parameter* auf einen gültigen Zeiger festlegen. Verwenden Sie [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) für den zurückgegebenen Zeiger, um **WBEM \_ S NO \_ \_ ERROR** abzurufen.

3.  Beenden Sie Ihren Anruf.

    Bei einem Aufruf, der einen Enumerator zurückgibt, ruft WMI [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) auf, um den Abschluss des Vorgangs zu melden. Wenn Sie nicht das gesamte Ergebnis benötigen, geben Sie den Enumerator frei, indem Sie die [**Releasemethode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject):: aufrufen. Der Aufruf von **Release** führt dazu, dass WMI die Übermittlung aller noch erhaltenen Objekte abbricht.

    Rufen Sie für einen Aufruf, der keinen Enumerator verwendet, das [**GetCallStatus-Objekt**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) über den *plStatus-Parameter* Ihrer Methode ab.

Das C++-Codebeispiel in diesem Thema erfordert, dass die folgenden \# include-Anweisungen ordnungsgemäß kompiliert werden.


```C++
#include <comdef.h>
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird gezeigt, wie ein semisynchroner Aufruf von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)auftritt.


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
