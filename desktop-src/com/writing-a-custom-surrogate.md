---
title: Schreiben eines benutzerdefinierten Ersatz Zeichens
description: Schreiben eines benutzerdefinierten Ersatz Zeichens
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316514"
---
# <a name="writing-a-custom-surrogate"></a>Schreiben eines benutzerdefinierten Ersatz Zeichens

Das vom System bereitgestellte Ersatz Zeichen ist für die meisten Situationen mehr als ausreichend. es gibt jedoch einige Fälle, in denen das Schreiben eines benutzerdefinierten Ersatz Zeichens sinnvoll sein könnte. Nachstehend sind einige Beispiele aufgeführt:

-   Ein benutzerdefiniertes Ersatz Zeichen kann einige Optimierungen oder Semantik bereitstellen, die nicht im System-Ersatz Zeichen vorhanden sind.
-   Wenn eine in-Process-DLL Code enthält, der davon abhängt, dass Sie sich im gleichen Prozess wie der Client befinden, funktioniert der DLL-Server nicht ordnungsgemäß, wenn er im System-Ersatz Zeichen ausgeführt wird. Ein benutzerdefiniertes Ersatz Zeichen kann auf eine bestimmte dll zugeschnitten werden, um dies zu tun.
-   Das System-Ersatz Zeichen unterstützt ein gemischtes Threading Modell, sodass es sowohl kostenlose als auch Apartment-Modell-DLLs laden kann. Ein benutzerdefiniertes Ersatz Zeichen ist möglicherweise so angepasst, dass nur Apartment-DLLs geladen werden. Dies kann aus Gründen der Effizienz oder das akzeptieren eines Befehlszeilen Arguments für den Typ der DLL erfolgen, die geladen werden darf.
-   Ein benutzerdefiniertes Ersatz Zeichen kann zusätzliche Befehlszeilenparameter verwenden, die vom System-Ersatz Zeichen nicht unterstützt werden.
-   Der System Ersatz ruft [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) auf und weist ihn an, alle vorhandenen Sicherheitseinstellungen zu verwenden, die unter dem [AppID](appid-key.md) -Schlüssel in der Registrierung gefunden werden. Ein benutzerdefiniertes Ersatz Zeichen könnte einen anderen Sicherheitskontext verwenden.
-   Schnittstellen, die nicht Remote fähig sind (z. b. die für die letzten okxs), funktionieren nicht mit dem System Ersatz Zeichen. Ein benutzerdefiniertes Ersatz Zeichen kann die Schnittstellen der DLL-Datei mit einer eigenen Implementierung umschließen und Proxy-/Stub-DLLs mit einer Remote fähigen IDL-Definition verwenden, die eine Remote Schnittstelle der Schnittstelle ermöglichen würde.

Der Haupt-Ersatz Thread sollte in der Regel die folgenden Setup Schritte ausführen:

1.  [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, um den Thread zu initialisieren und das Threading Modell festzulegen.
2.  Wenn Sie möchten, dass die DLL-Server, die auf dem Server ausgeführt werden sollen, die Sicherheitseinstellungen im **AppID** -Registrierungsschlüssel verwenden können, müssen Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) mit der eoac- \_ AppID-Funktion abrufen. Andernfalls werden ältere Sicherheitseinstellungen verwendet.
3.  Ruft [**coregisterersatz**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) auf, um die Ersatz Schnittstelle für com zu registrieren.
4.  Nennen Sie [**isurrogate:: loaddllserver**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) für die angeforderte CLSID.
5.  Platzieren Sie den Haupt Thread in einer Schleife, um [**cofreunusedlibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) in regelmäßigen Abständen aufzurufen.
6.  Wenn com [**isurrogate:: freesurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate)aufruft, widerrufen Sie alle Klassenfactorys, und beenden Sie.

Ein Ersatzprozess muss die [**isurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) -Schnittstelle implementieren. Diese Schnittstelle muss registriert werden, wenn ein neuer Ersatz Zeichen gestartet wird und nach dem Aufrufen von [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Wie in den vorherigen Schritten angegeben, verfügt die **isurrogate** -Schnittstelle über zwei Methoden, die com aufruft: [**loaddllserver**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), um neue dll-Server dynamisch in vorhandene Surrogates zu laden. und [**freesurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), um das Ersatz Zeichen freizugeben.

Die Implementierung von [**loaddllserver**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), die com mit einer Lade Anforderung aufruft, muss zunächst ein klassenfactoryobjekt erstellen, das [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)und [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)unterstützt, und dann [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) aufrufen, um das Objekt als Klassenfactory für die angeforderte CLSID zu registrieren.

Die vom Ersatzprozess registrierte Klassenfactory ist nicht die tatsächliche Klassenfactory, die vom dll-Server implementiert wird. Sie ist jedoch eine generische Klassenfactory, die von dem Ersatzprozess implementiert wird, der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) und [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)unterstützt. Da es sich um die Klassenfactory des Ersatz Zeichens handelt, anstatt um die des dll-Servers, die registriert wird, muss die Klassenfactory des Ersatz dienstangs die echte Klassenfactory verwenden, um eine Instanz des Objekts für die registrierte CLSID zu erstellen. Die [**IClassFactory::**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) -Methode des Ersatz Zeichens sollte in etwa wie im folgenden Beispiel aussehen:


```C++
STDMETHODIMP CSurrogateFactory::CreateInstance(
  IUnknown* pUnkOuter, 
  REFIID iid, 
  void** ppv)
{
    void* pcf;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, IID_IClassFactory, &pcf);
    if ( FAILED(hr) )
        return hr;
    hr = ((IClassFactory*)pcf)->CreateInstance(pUnkOuter, iid, ppv);
    ((IClassFactory*)pcf)->Release();
    return hr;
}
 
```



Die Klassenfactory des Ersatz Zeichens muss auch " [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) " unterstützen, da ein [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) -aufrufen eine beliebige Schnittstelle aus der registrierten Klassenfactory anfordern kann, nicht nur " [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)". Da die generische Klassenfactory nur [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) und **IClassFactory** unterstützt, müssen Anforderungen für andere Schnittstellen an das echte Objekt weitergeleitet werden. Daher sollte eine [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) -Methode vorhanden sein, die der folgenden ähnelt:


```C++
STDMETHODIMP CSurrogateFactory::MarshalInterface(
  IStream *pStm,  
  REFIID riid, void *pv, 
  WORD dwDestContext, 
  void *pvDestContext, 
  DWORD mshlflags )
{   
    void * pCF = NULL;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, riid, &pCF);
    if ( FAILED(hr) )
        return hr;   
    hr = CoMarshalInterface(pStm, riid, (IUnknown*)pCF, dwDestContext, pvDestContext,  mshlflags);
    ((IUnknown*)pCF)->Release();
    return S_OK;
 
```



Das Ersatz Zeichen, das einen dll-Server enthält, muss die Klassen Objekte des dll-Servers mit einem [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)-Aufrufer veröffentlichen. Alle Klassenfactorys für dll-Surrogates müssen als REGCLS-Ersatz Zeichen registriert werden \_ . REGCLS \_ singluse und REGCLS \_ multipleuse sollten nicht für dll-Server verwendet werden, die in Surrogates geladen werden.

Befolgen Sie diese Richtlinien, um einen Ersatzprozess zu erstellen, wenn dies erforderlich ist, sollten Sie das richtige Verhalten sicherstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLL-Surrogates](dll-surrogates.md)
</dt> </dl>

 

 