---
title: Verwenden eines Sitzungsmonikers
description: Die Sitzungs-zu-Sitzung-Aktivierung ermöglicht es einem Clientprozess, einen lokalen Serverprozess für eine bestimmte Sitzung zu aktivieren.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fc5c65c3e2efd3e566a3fdde6982fefe5bb14fbefd98ca8abd335955b7efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868850"
---
# <a name="using-a-session-moniker"></a>Verwenden eines Sitzungsmonikers

Die Sitzungs-zu-Sitzung-Aktivierung ermöglicht es einem Clientprozess, einen lokalen Serverprozess für eine bestimmte Sitzung zu aktivieren. Hierzu können Sie sitzungsbezogen einen vom System bereitgestellten Sitzungsmoniker verwenden. Weitere Informationen zum Erstellen eines Sitzungsmonikers finden Sie unter [Session-to-Session Activation with a Session Moniker (Sitzungs-zu-Sitzungsaktivierung mit einem Sitzungsmoniker).](session-to-session-activation-with-a-session-moniker.md)

Das folgende Beispiel zeigt, wie Sie einen lokalen Serverprozess mit der Klassen-ID "10000013-0000-0000-0000-000000000001" für die Sitzung mit der Sitzungs-ID 3 aktivieren.

Zunächst ruft das Beispiel die [**CoInitialize-Funktion**](/windows/win32/api/objbase/nf-objbase-coinitialize) auf, um die COM-Bibliothek zu initialisieren. Anschließend ruft das Beispiel [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) auf, um einen Zeiger auf eine Implementierung der [**IBindCtx-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ibindctx) abzurufen. Dieses Objekt speichert Informationen zu Monikerbindungsvorgängen. der Zeiger ist erforderlich, um Methoden der [**IMoniker-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-imoniker) aufzurufen. Als Nächstes ruft das Beispiel die [MkParseDisplayNameEx-Funktion](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) auf, um den zusammengesetzten Sitzungsmoniker zu erstellen, und dann die [**IMoniker::BindToObject-Methode,**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) um die Verbindung zwischen dem Client und dem Serverprozess mithilfe des neu erstellten Sitzungsmonikers zu aktivieren. An diesem Punkt können Sie den Schnittstellenzeiger verwenden, um die gewünschten Vorgänge für das Objekt auszuführen. Schließlich gibt das Beispiel den Bindungskontext frei und ruft die [**CoUninitialize-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) auf.


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



Da "{klassen-ID des Klassenmonikers}" auch eine Möglichkeit zum Benennen eines Klassenmonikers ist, können Sie die folgende Zeichenfolge verwenden, um den zusammengesetzten Moniker (den mit dem Klassenmoniker zusammengesetzten Sitzungsmoniker) zu benennen, anstatt wie im vorherigen Beispiel gezeigt.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Wenn derselbe Benutzer während einer sitzungsübergreifenden Aktivierung bei jeder Sitzung angemeldet ist, können Sie jeden Serverprozess aktivieren, der für die Ausführung im Interaktiven Benutzeraktivierungsmodus "RunAs" konfiguriert ist. Wenn verschiedene Benutzer bei jeder Sitzung angemeldet sind, muss der Server die [**CoInitializeSecurity-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufrufen, um die entsprechenden Benutzerrechte festzulegen, bevor eine erfolgreiche Aktivierung und Verbindung zwischen dem Client und dem Server hergestellt werden kann. Eine Möglichkeit, dies zu erreichen, besteht darin, dass der Server eine benutzerdefinierte [**IAccessControl-Schnittstelle**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) implementiert und die Implementierung an **CoInitializeSecurity** übergibt. In jedem Fall muss der Clientbenutzer über die entsprechenden [**Start-**](../com/launchpermission.md) und [**Zugriffsberechtigungen**](../com/accesspermission.md) verfügen, die von der anwendung angegeben werden, die auf dem Server ausgeführt wird. Weitere Informationen finden Sie unter [Sicherheit in COM.](../com/security-in-com.md)

 

Weitere Informationen zu vom System bereitgestellten Monikern und Monikern und Aktivierungsmodi finden Sie unter [Moniker](../com/monikers.md), die [**IMoniker-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-imoniker) und [AppId Key](/windows/desktop/com/appid-key) in der COM-Dokumentation im Platform Software Development Kit (SDK).

 

 