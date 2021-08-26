---
description: Die IWbemObjectSink-Schnittstelle erstellt eine Senkenschnittstelle, die alle Arten von Benachrichtigungen innerhalb des WMI-Programmiermodells empfangen kann.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: IWbemObjectSink-Schnittstelle (Wbemcli.h)
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
ms.openlocfilehash: 6bfce21edca92c95276f382d16007f8b319b9f3b80fc5c3c721f7232ea0b4618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996540"
---
# <a name="iwbemobjectsink-interface"></a>IWbemObjectSink-Schnittstelle

Die **IWbemObjectSink-Schnittstelle** erstellt eine Senkenschnittstelle, die alle Arten von Benachrichtigungen innerhalb des WMI-Programmiermodells empfangen kann. Clients müssen diese Schnittstelle implementieren, um sowohl die Ergebnisse der [asynchronen](making-an-asynchronous-call-with-c--.md) Methoden von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)als auch bestimmte Typen von Ereignisbenachrichtigungen zu empfangen. Anbieter verwenden diese Schnittstelle, implementieren sie aber nicht, um Ereignisse und Objekte für WMI zur Verfügung zu stellen.

Anbieter rufen in der Regel eine Implementierung auf, die ihnen von WMI bereitgestellt wird. Rufen Sie in diesen Fällen [**Angeben auf,**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) um Dem WMI-Dienst Objekte zur Verfügung zu stellen. Rufen Sie anschließend [**SetStatus auf,**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) um das Ende der Benachrichtigungssequenz anzugeben. Sie können **setStatus** auch aufrufen, um Fehler anzugeben, wenn die Senke keine Objekte enthält.

Beim Programmieren asynchroner Clients von WMI stellt der Benutzer die Implementierung zur Verfügung. WMI ruft die Methoden auf, um Objekte zu liefern und den Status des Ergebnisses fest zu legen.

> [!Note]  
> Wenn eine Clientanwendung dieselbe Senkenschnittstelle in zwei verschiedenen überlappenden asynchronen Aufrufen übergibt, garantiert WMI die Reihenfolge des Rückrufs nicht. Clientanwendungen, die überlappende asynchrone Aufrufe ausführen, sollten entweder verschiedene Senkenobjekte übergeben oder ihre Aufrufe serialisieren.

 

> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf der vom Client benötigten Authentifizierungsebene zurückgegeben wird, wird empfohlen, anstelle der asynchronen Kommunikation eine semisynchrone Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

## <a name="members"></a>Member

Die **IWbemObjectSink-Schnittstelle** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWbemObjectSink-Schnittstelle** verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Anzugeben**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | Empfängt Benachrichtigungsobjekte.<br/>                                                                               |
| [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | Wird von Quellen aufgerufen, um das Ende einer Benachrichtigungssequenz anzugeben oder andere Statuscodes an die Senke zu senden.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie beim Implementieren einer Ereignisabonnementsenke **(IWbemObjectSink** oder [**IWbemEventSink)**](iwbemeventsink.md)nicht in WMI aus den [**Methoden Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) oder [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) für das Senkenobjekt auf. Beispielsweise kann der Aufruf [**von IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) zum Abbrechen der Senke innerhalb einer Implementierung von [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) den WMI-Zustand beeinträchtigen. Um ein Ereignisabonnement zu kündigen, legen Sie ein Flag fest, und rufen **Sie IWbemServices::CancelAsyncCall von** einem anderen Thread oder Objekt aus auf. Für Implementierungen, die nicht mit einer Ereignissenke verknüpft sind, z. B. Objekt-, Enum- und Abfrageabrufe, können Sie einen Rückruf in WMI ausführen.

Senkenimplementierungen sollten die Ereignisbenachrichtigung innerhalb von 100 MSEC verarbeiten, da der WMI-Thread, der die Ereignisbenachrichtigung übergibt, keine anderen Arbeiten mehr tun kann, bis die Verarbeitung des Senkenobjekts abgeschlossen ist. Wenn die Benachrichtigung eine große Menge an Verarbeitung erfordert, kann die Senke eine interne Warteschlange für einen anderen Thread verwenden, um die Verarbeitung zu verarbeiten.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel ist eine einfache Implementierung einer Objektsenke. Dieses Beispiel kann mit [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) oder [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) verwendet werden, um die zurückgegebenen Instanzen zu empfangen:


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
| Header<br/>                   | <dl> <dt>Wbemcli.h (einschließlich Wbemidl.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Wbemuuid.lib</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl>                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM-API für WMI](com-api-for-wmi.md)
</dt> <dt>

[Ausführen eines asynchronen Aufrufs mit C++](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[Festlegen der Sicherheit für einen asynchronen Aufruf](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[Empfangen von Ereignissen für die Dauer Ihrer Anwendung](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




