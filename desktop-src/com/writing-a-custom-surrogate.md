---
title: Schreiben eines benutzerdefinierten Ersatzzeichens
description: Schreiben eines benutzerdefinierten Ersatzzeichens
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c6098f4d0e9d99be86956bacce413e7e8a4b864a91212d6c2a1a257d9c1db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047658"
---
# <a name="writing-a-custom-surrogate"></a>Schreiben eines benutzerdefinierten Ersatzzeichens

Obwohl das vom System bereitgestellte Ersatzzeichen für die meisten Situationen mehr als ausreichend ist, gibt es einige Fälle, in denen das Schreiben eines benutzerdefinierten Ersatzzeichens sinnvoll sein kann. Nachstehend sind einige Beispiele aufgeführt:

-   Ein benutzerdefiniertes Ersatzzeichen kann einige Optimierungen oder Semantik bereitstellen, die im System-Ersatzzeichen nicht vorhanden sind.
-   Wenn eine in-process-DLL Code enthält, der davon abhängt, dass sie sich im selben Prozess wie der Client befindet, funktioniert der DLL-Server nicht ordnungsgemäß, wenn er im System-Ersatz ausgeführt wird. Ein benutzerdefiniertes Ersatzzeichen kann auf eine bestimmte DLL zugeschnitten werden, um dies zu behandeln.
-   Das System-Ersatzzeichen unterstützt ein Mixed-Threading-Modell, sodass sowohl kostenlose als auch Apartmentmodell-DLLs geladen werden können. Ein benutzerdefiniertes Ersatzzeichen kann aus Effizienzgründen so angepasst werden, dass nur Apartment-DLLs geladen werden oder ein Befehlszeilenargument für den Dll-Typ akzeptiert wird, der geladen werden darf.
-   Ein benutzerdefiniertes Ersatzzeichen kann zusätzliche Befehlszeilenparameter annehmen, die das System-Ersatzzeichen nicht verwendet.
-   Das System surrogate ruft [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) auf und weist es an, alle vorhandenen Sicherheitseinstellungen zu verwenden, die unter dem [AppID-Schlüssel](appid-key.md) in der Registrierung gefunden werden. Ein benutzerdefinierter Ersatz kann einen anderen Sicherheitskontext verwenden.
-   Schnittstellen, die nicht remotable sind (z. B. schnittstellen für aktuelle OCX-Dateien), funktionieren nicht mit dem System-Ersatzzeichen. Ein benutzerdefiniertes Ersatzzeichen könnte die Schnittstellen der DLL mit einer eigenen Implementierung umschließen und Proxy-/Stub-DLLs mit einer remotablen IDL-Definition verwenden, die die Remotezugriffssteuerung der Schnittstelle ermöglicht.

Der Haupt-Ersatzthread sollte in der Regel die folgenden Setupschritte ausführen:

1.  Rufen Sie [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) auf, um den Thread zu initialisieren und das Threadingmodell festzulegen.
2.  Wenn die DLL-Server, die auf dem Server ausgeführt werden sollen, die Sicherheitseinstellungen im **AppID-Registrierungsschlüssel** verwenden können sollen, rufen Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) mit der EOAC-APPID-Funktion \_ auf. Andernfalls werden Legacysicherheitseinstellungen verwendet.
3.  Rufen Sie [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) auf, um die Ersatzschnittstelle bei COM zu registrieren.
4.  Rufen Sie [**ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) für die angeforderte CLSID auf.
5.  Versetzen Sie den Hauptthread in eine Schleife, um [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) in regelmäßigen Abständen aufzurufen.
6.  Wenn COM [**ISurrogate::FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate)aufruft, widerrufen Sie alle Klassenfactorys, und beenden Sie.

Ein Ersatzprozess muss die [**ISurrogate-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) implementieren. Diese Schnittstelle sollte registriert werden, wenn ein neues Ersatzzeichen gestartet wird und nachdem [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)aufgerufen wurde. Wie in den vorherigen Schritten angegeben, verfügt die **ISurrogate-Schnittstelle** über zwei Methoden, die COM aufruft: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), um neue DLL-Server dynamisch in vorhandene Ersatzzeichen zu laden. und [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), um das Ersatzzeichen frei zu machen.

Die Implementierung von [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), die COM mit einer Ladeanforderung aufruft, muss zunächst ein Klassenfactoryobjekt erstellen, das [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)und [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)unterstützt, und dann [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) aufrufen, um das Objekt als Klassenfactory für die angeforderte CLSID zu registrieren.

Die vom Ersatzprozess registrierte Klassenfactory ist nicht die tatsächliche Klassenfactory, die vom DLL-Server implementiert wird, sondern eine generische Klassenfactory, die vom Ersatzprozess implementiert wird, der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) und [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)unterstützt. Da es sich um die Klassenfactory des Ersatzzeichens und nicht um die des DLL-Servers handelt, der registriert wird, muss die Klassenfactory des Ersatzzeichens die echte Klassenfactory verwenden, um eine Instanz des -Objekts für die registrierte CLSID zu erstellen. Die [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) des Ersatzzeichens sollte in etwa wie im folgenden Beispiel aussehen:


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



Die Klassenfactory des Ersatzzeichens muss auch [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) unterstützen, da ein Aufruf von [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) eine beliebige Schnittstelle von der registrierten Klassenfactory anfordern kann, nicht nur [**IClassFactory.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) Da die generische Klassenfactory nur [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) und **IClassFactory** unterstützt, müssen Anforderungen für andere Schnittstellen an das echte Objekt weitergeleitet werden. Daher sollte eine [**MarshalInterface-Methode**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) vorhanden sein, die der folgenden ähneln sollte:


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



Das Ersatzzeichen, das einen DLL-Server enthält, muss die Klassenobjekte des DLL-Servers mit einem Aufruf von [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)veröffentlichen. Alle Klassenfactorys für DLL-Ersatzzeichen sollten als REGCLS \_ SURROGATE registriert werden. REGCLS \_ SINGLUSE und REGCLS \_ MULTIPLEUSE sollten nicht für DLL-Server verwendet werden, die in Ersatzzeichen geladen werden.

Wenn Sie diese Richtlinien zum Erstellen eines Ersatzzeichenprozesses befolgen, wenn dies erforderlich ist, sollten Sie ein ordnungsgemäßes Verhalten sicherstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLL-Ersatzzeichen](dll-surrogates.md)
</dt> </dl>

 

 