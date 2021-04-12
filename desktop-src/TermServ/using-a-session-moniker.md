---
title: Verwenden eines sitzungsmonikers
description: Die Sitzungs-zu-Sitzung-Aktivierung ermöglicht einem Client Prozess das Aktivieren eines lokalen Server Prozesses für eine bestimmte Sitzung.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700d251aa1136747529b66b975d4cbedf9b14dcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316184"
---
# <a name="using-a-session-moniker"></a>Verwenden eines sitzungsmonikers

Die Sitzungs-zu-Sitzung-Aktivierung ermöglicht einem Client Prozess das Aktivieren eines lokalen Server Prozesses für eine bestimmte Sitzung. Dies kann pro Sitzung mithilfe eines vom System bereitgestellten sitzungsmonikers erfolgen. Weitere Informationen zum Erstellen eines sitzungsmonikers finden [Sie unter Sitzungs-zu-Sitzung-Aktivierung mit einem sitzungsmoniker](session-to-session-activation-with-a-session-moniker.md).

Im folgenden Beispiel wird gezeigt, wie ein lokaler Server Prozess mit der Klassen-ID "10000013-0000-0000-0000-000000000001" in der Sitzung mit der Sitzungs-ID 3 aktiviert wird.

Zuerst Ruft das Beispiel die [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) -Funktion auf, um die com-Bibliothek zu initialisieren. Anschließend ruft das Beispiel "" mit " [**kreatebindctx**](/windows/win32/api/objbase/nf-objbase-createbindctx) " auf, um einen Zeiger auf eine Implementierung der [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) -Schnittstelle abzurufen. Dieses Objekt speichert Informationen zu monikerbindungsvorgängen. der-Zeiger ist erforderlich, um Methoden der [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) -Schnittstelle aufzurufen. Im folgenden Beispiel wird die Funktion " [mksamsedisplaynameex](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) " aufgerufen, um den zusammengesetzten sitzungsmoniker zu erstellen, und anschließend die [**IMoniker:: bindesobject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) -Methode, um die Verbindung zwischen dem Client und dem Server Prozess mit dem neu erstellten sitzungsmoniker zu aktivieren. An diesem Punkt können Sie den Schnittstellen Zeiger verwenden, um die gewünschten Vorgänge für das Objekt auszuführen. Schließlich gibt das Beispiel den Bindungs kontextfrei und ruft die Funktion " [**zählinitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) " auf.


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



Da "{Class ID of the Class Moniker}" auch eine Möglichkeit ist, einen klassenmoniker zu benennen, können Sie die folgende Zeichenfolge verwenden, um den zusammengesetzten Moniker (dem sitzungsmoniker, der mit dem klassenmoniker erstellt wurde) zu benennen, anstatt wie im vorherigen Beispiel gezeigt.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Wenn derselbe Benutzer während einer Sitzungs übergreifenden Aktivierung bei jeder Sitzung angemeldet ist, können Sie jeden Server Prozess, der für die Ausführung im interaktiven runas-Benutzer Aktivierungs Modus konfiguriert ist, erfolgreich aktivieren. Wenn verschiedene Benutzer an jeder Sitzung angemeldet sind, muss der Server die [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion anrufen, um die entsprechenden Benutzerrechte vor einer erfolgreichen Aktivierung und Verbindung zwischen dem Client und dem Server festzulegen. Eine Möglichkeit, dies zu erreichen, besteht darin, dass der Server eine benutzerdefinierte [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) -Schnittstelle implementiert und die Implementierung an **CoInitializeSecurity** übergibt. In jedem Fall muss der Client Benutzer über die entsprechenden [**Start**](../com/launchpermission.md) -und [**Zugriffsberechtigungen**](../com/accesspermission.md) verfügen, die von der Anwendung, die auf dem Server ausgeführt wird, angegeben werden. Weitere Informationen finden Sie [unter Sicherheit in com](../com/security-in-com.md).

 

Weitere Informationen über vom System bereitgestellte Moniker und Moniker und Aktivierungs Modi finden Sie in der com-Dokumentation des Platform Software Development Kit (SDK) unter [Moniker](../com/monikers.md), [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) Interface und [AppID Key](/windows/desktop/com/appid-key) .

 

 