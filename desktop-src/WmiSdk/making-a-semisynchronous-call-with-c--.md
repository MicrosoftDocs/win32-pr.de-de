---
description: 'Semisynchrone Aufrufe sind die empfohlenen Methoden zum Aufrufen von WMI-Methoden, wie z. b. IWbemServices:: ExecMethod und Provider-Methoden, wie z. b. die CHKDSK-Methode der Win32 \_ LogicalDisk-Klasse.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Erstellen eines semisynchronen Aufrufes mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529615"
---
# <a name="making-a-semisynchronous-call-with-c"></a>Erstellen eines semisynchronen Aufrufes mit C++

Semisynchrone Aufrufe sind die empfohlenen Methoden zum Aufrufen von WMI-Methoden, wie z. b. [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) und Provider-Methoden, wie z. b. die [**chkdsk-Methode der Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).

Ein Nachteil der synchronen Verarbeitung ist, dass der aufruferthread blockiert wird, bis der Aufruf abgeschlossen ist. Die Blockierung hin kann zu einer Verzögerung bei der Verarbeitungszeit führen. Im Gegensatz dazu muss ein asynchroner-Befehl in einem Skript " [**Swap-Sink**](swbemsink.md) " implementieren. In C++ muss der asynchrone Code die [**iwbebobjectsink**](iwbemobjectsink.md) -Schnittstelle implementieren, mehrere Threads verwenden und den Informationsfluss zurück an den Aufrufer steuern. Große Resultsets aus Abfragen können z. b. sehr viel Zeit in Anspruch nehmen und erzwingen, dass der Aufrufer beträchtliche Systemressourcen für die Übermittlung bereitstellt.

Durch die semisynchrone Verarbeitung werden sowohl die Probleme beim Blockieren von Threads als auch bei der Übertragung durch Abfragen eines speziellen Status Objekts, das die [**iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) -Schnittstelle implementiert Mithilfe von **iwbemcallresult** können Sie die Geschwindigkeit und Effizienz von Abfragen, Enumerationen und Ereignis Benachrichtigungen verbessern.

Im folgenden Verfahren wird beschrieben, wie Sie einen semisynchronen-Befehl mit der [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle erstellen.

**So führen Sie mit der IWbemServices-Schnittstelle einen semisynchronen Befehl aus**

1.  Führen Sie den-Befehl wie gewohnt aus, aber mit dem WBEM-Flag wird sofort das Flag im *IFlags* -Parameter **\_ \_ zurück \_ gegeben** .

    Sie können das **WBEM \_ - \_ Flag \_ direkt** mit anderen Flags kombinieren, die für die jeweilige Methode gültig sind. Verwenden Sie z. b. für alle Aufrufe, die Enumeratoren zurückgeben, das **WBEM-Flag für den \_ \_ Vorwärts \_ -Flag** . Das Festlegen dieser Flags in Kombination spart Zeit und Speicherplatz und verbessert die Reaktionsfähigkeit.

2.  Abrufen der Ergebnisse.

    Wenn Sie eine Methode aufrufen, die einen Enumerator zurückgibt, wie z. b. [**IWbemServices:: kreateclassenum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) oder [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), können Sie die Enumeratoren mit der [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) -Methode oder der [**ienumwbemclassobject:: nextasync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) -Methode Abfragen. Der **ienumwbemclassobject:: nextasync** -Aufrufwert ist nicht blockierend und wird sofort zurückgegeben. Im Hintergrund beginnt WMI mit dem übermitteln der angeforderten Anzahl von Objekten durch Aufrufen von [**iwbemubjectsink:: angeben**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate). WMI hält dann an und wartet auf einen anderen **nextasync** -Aufruf.

    Wenn Sie eine Methode aufrufen, die keinen Enumerator zurückgibt (z. b. [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)), müssen Sie den Parameter *ppcallresult* auf einen gültigen Zeiger festlegen. Verwenden Sie [**iwbemcallresult:: getcallstatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) für den zurückgegebenen Zeiger, um **WBEM \_ S \_ No \_ Error** abzurufen.

3.  Beenden Sie den-Befehl.

    Für einen Aufruf, der einen Enumerator zurückgibt, ruft WMI [**iwbewbjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) auf, um den Abschluss des Vorgangs zu melden. Wenn Sie das gesamte Ergebnis nicht benötigen, geben Sie den Enumerator durch Aufrufen der [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode frei. Das Aufrufen von **Release** führt dazu, dass WMI die Übermittlung aller verbleibenden Objekte abbricht.

    Rufen Sie für einen Aufruf, der keinen Enumerator verwendet, das [**getcallstatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) -Objekt über den *plstatus* -Parameter der Methode ab.

Das C++-Codebeispiel in diesem Thema erfordert, dass die folgenden \# include-Anweisungen ordnungsgemäß kompiliert werden.


```C++
#include <comdef.h>
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird gezeigt, wie Sie einen semisynchronen aufzurufenden [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)-Befehl erstellen.


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

 

 
