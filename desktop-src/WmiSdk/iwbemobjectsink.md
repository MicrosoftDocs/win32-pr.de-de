---
description: Die iwbeporbjectsink-Schnittstelle erstellt eine Sink-Schnittstelle, die alle Arten von Benachrichtigungen innerhalb des WMI-Programmiermodells empfangen kann.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Iwbemubjectsink-Schnittstelle (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368237"
---
# <a name="iwbemobjectsink-interface"></a>Iwbemubjectsink-Schnittstelle

Die **iwbeporbjectsink** -Schnittstelle erstellt eine Sink-Schnittstelle, die alle Arten von Benachrichtigungen innerhalb des WMI-Programmiermodells empfangen kann. Clients müssen diese Schnittstelle implementieren, um sowohl die Ergebnisse der [asynchronen Methoden](making-an-asynchronous-call-with-c--.md) von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)als auch bestimmte Arten von Ereignis Benachrichtigungen zu empfangen. Anbieter verwenden, implementieren diese Schnittstelle jedoch nicht, um der WMI Ereignisse und Objekte bereitzustellen.

In der Regel wird von Anbietern eine von WMI bereitgestellte Implementierung aufgerufen. In diesen Fällen [**geben**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) Sie an, um-Objekte für den WMI-Dienst bereitzustellen. Anschließend wird [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) aufgerufen, um das Ende der Benachrichtigungs Sequenz anzugeben. Sie können auch **SetStatus** aufrufen, um Fehler anzugeben, wenn die Senke keine Objekte enthält.

Beim Programmieren von asynchronen WMI-Clients stellt der Benutzer die-Implementierung bereit. WMI Ruft die Methoden zum Übermitteln von Objekten auf und legt den Status des Ergebnisses fest.

> [!Note]  
> Wenn eine Client Anwendung die gleiche Senke-Schnittstelle in zwei unterschiedlichen asynchronen Aufrufen übergibt, garantiert WMI nicht die Reihenfolge des Rückrufs. Client Anwendungen, die überlappende asynchrone Aufrufe durchführen, sollten entweder unterschiedliche Sink-Objekte übergeben oder Ihre Aufrufe serialisieren.

 

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, empfiehlt es sich, anstelle der asynchronen Kommunikation semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

## <a name="members"></a>Member

Die **iwbeporbjectsink** -Schnittstelle verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwbemubjectsink** -Schnittstelle verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Aufgezeigt**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | Empfängt Benachrichtigungsobjekte.<br/>                                                                               |
| [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | Wird von Quellen aufgerufen, um das Ende einer Benachrichtigungs Sequenz anzugeben, oder, um andere Statuscodes an die Senke zu senden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Ereignis-Abonnement-Senke (**iwbewbjectsink** oder [**iwbemeventsink**](iwbemeventsink.md)) implementieren, sollten Sie in der Methode " [**angeben**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) " oder " [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) " für das senkentabbild keine WMI aufrufen. Beispiels [**Weise kann das Aufrufen von**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) [**IWbemServices:: cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) zum Abbrechen der Senke aus einer Implementierung von den WMI-Zustand beeinträchtigen. Um ein Ereignis Abonnement abzubrechen, legen Sie ein Flag fest, und rufen Sie **IWbemServices:: cancelasynccall** von einem anderen Thread oder Objekt auf. Bei Implementierungen, die sich nicht auf eine Ereignis Senke beziehen, wie z. b. Object-, enum-und Abfrage-Abruf Werte, können Sie einen Rückruf in WMI durchlaufen.

Sink-Implementierungen sollten die Ereignis Benachrichtigung innerhalb von 100 MS verarbeiten, weil der WMI-Thread, der die Ereignis Benachrichtigung übermittelt, erst dann andere Aufgaben ausführen kann, wenn die Verarbeitung des Sink-Objekts abgeschlossen ist. Wenn für die Benachrichtigung eine große Menge an Verarbeitung erforderlich ist, kann die Senke eine interne Warteschlange für einen anderen Thread verwenden, um die Verarbeitung zu verarbeiten.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel ist eine einfache Implementierung einer Objekt Senke. Dieses Beispiel kann mit [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) oder [**IWbemServices:: | ateinstanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) verwendet werden, um die zurückgegebenen Instanzen zu empfangen:


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                           |
| Header<br/>                   | <dl> <dt>Wbemcli. h (Include wbemittell. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Wbemuuid. lib</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl>                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM-API für WMI](com-api-for-wmi.md)
</dt> <dt>

[Erstellen eines asynchronen Aufrufes mit C++](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[Festlegen der Sicherheit für einen asynchronen-Befehl](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[Empfangen von Ereignissen für die Dauer der Anwendung](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




