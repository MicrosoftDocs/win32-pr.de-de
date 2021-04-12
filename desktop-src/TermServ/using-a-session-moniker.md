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
# <a name="using-a-session-moniker"></a><span data-ttu-id="97313-103">Verwenden eines sitzungsmonikers</span><span class="sxs-lookup"><span data-stu-id="97313-103">Using a Session Moniker</span></span>

<span data-ttu-id="97313-104">Die Sitzungs-zu-Sitzung-Aktivierung ermöglicht einem Client Prozess das Aktivieren eines lokalen Server Prozesses für eine bestimmte Sitzung.</span><span class="sxs-lookup"><span data-stu-id="97313-104">Session-to-session activation allows a client process to activate a local server process on a specified session.</span></span> <span data-ttu-id="97313-105">Dies kann pro Sitzung mithilfe eines vom System bereitgestellten sitzungsmonikers erfolgen.</span><span class="sxs-lookup"><span data-stu-id="97313-105">You can do this on a per-session basis by using a system-supplied session moniker.</span></span> <span data-ttu-id="97313-106">Weitere Informationen zum Erstellen eines sitzungsmonikers finden [Sie unter Sitzungs-zu-Sitzung-Aktivierung mit einem sitzungsmoniker](session-to-session-activation-with-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="97313-106">For more information about creating a session moniker, see [Session-to-Session Activation with a Session Moniker](session-to-session-activation-with-a-session-moniker.md).</span></span>

<span data-ttu-id="97313-107">Im folgenden Beispiel wird gezeigt, wie ein lokaler Server Prozess mit der Klassen-ID "10000013-0000-0000-0000-000000000001" in der Sitzung mit der Sitzungs-ID 3 aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="97313-107">The following example shows how to activate a local server process with the class ID "10000013-0000-0000-0000-000000000001" on the session with the session ID 3.</span></span>

<span data-ttu-id="97313-108">Zuerst Ruft das Beispiel die [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) -Funktion auf, um die com-Bibliothek zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="97313-108">First, the sample calls the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function to initialize the COM library.</span></span> <span data-ttu-id="97313-109">Anschließend ruft das Beispiel "" mit " [**kreatebindctx**](/windows/win32/api/objbase/nf-objbase-createbindctx) " auf, um einen Zeiger auf eine Implementierung der [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="97313-109">Then the sample calls [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) to retrieve a pointer to an implementation of the [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="97313-110">Dieses Objekt speichert Informationen zu monikerbindungsvorgängen. der-Zeiger ist erforderlich, um Methoden der [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) -Schnittstelle aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="97313-110">This object stores information about moniker-binding operations; the pointer is required to call methods of the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="97313-111">Im folgenden Beispiel wird die Funktion " [mksamsedisplaynameex](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) " aufgerufen, um den zusammengesetzten sitzungsmoniker zu erstellen, und anschließend die [**IMoniker:: bindesobject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) -Methode, um die Verbindung zwischen dem Client und dem Server Prozess mit dem neu erstellten sitzungsmoniker zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="97313-111">Next the sample calls the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function to create the composite session moniker and then the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to activate the connection between the client and the server process, using the newly created session moniker.</span></span> <span data-ttu-id="97313-112">An diesem Punkt können Sie den Schnittstellen Zeiger verwenden, um die gewünschten Vorgänge für das Objekt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="97313-112">At this point you can use the interface pointer to perform the desired operations on the object.</span></span> <span data-ttu-id="97313-113">Schließlich gibt das Beispiel den Bindungs kontextfrei und ruft die Funktion " [**zählinitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) " auf.</span><span class="sxs-lookup"><span data-stu-id="97313-113">Finally, the sample releases the bind context and calls the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


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



<span data-ttu-id="97313-114">Da "{Class ID of the Class Moniker}" auch eine Möglichkeit ist, einen klassenmoniker zu benennen, können Sie die folgende Zeichenfolge verwenden, um den zusammengesetzten Moniker (dem sitzungsmoniker, der mit dem klassenmoniker erstellt wurde) zu benennen, anstatt wie im vorherigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="97313-114">Because "{class id of the class moniker}" is also a way to name a class moniker, you can use the following string to name the composite moniker (the session moniker composed with the class moniker) instead of the way show in the preceding example.</span></span>

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> <span data-ttu-id="97313-115">Wenn derselbe Benutzer während einer Sitzungs übergreifenden Aktivierung bei jeder Sitzung angemeldet ist, können Sie jeden Server Prozess, der für die Ausführung im interaktiven runas-Benutzer Aktivierungs Modus konfiguriert ist, erfolgreich aktivieren.</span><span class="sxs-lookup"><span data-stu-id="97313-115">If the same user is logged on to each session during a cross-session activation, you can successfully activate any server process configured to run in the RunAs Interactive User activation mode.</span></span> <span data-ttu-id="97313-116">Wenn verschiedene Benutzer an jeder Sitzung angemeldet sind, muss der Server die [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion anrufen, um die entsprechenden Benutzerrechte vor einer erfolgreichen Aktivierung und Verbindung zwischen dem Client und dem Server festzulegen.</span><span class="sxs-lookup"><span data-stu-id="97313-116">If different users are logged on to each session, the server must call the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function to set the appropriate user rights before a successful activation and connection can occur between the client and the server.</span></span> <span data-ttu-id="97313-117">Eine Möglichkeit, dies zu erreichen, besteht darin, dass der Server eine benutzerdefinierte [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) -Schnittstelle implementiert und die Implementierung an **CoInitializeSecurity** übergibt.</span><span class="sxs-lookup"><span data-stu-id="97313-117">One way to accomplish this would be for the server to implement a custom [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) interface and pass the implementation to **CoInitializeSecurity**.</span></span> <span data-ttu-id="97313-118">In jedem Fall muss der Client Benutzer über die entsprechenden [**Start**](../com/launchpermission.md) -und [**Zugriffsberechtigungen**](../com/accesspermission.md) verfügen, die von der Anwendung, die auf dem Server ausgeführt wird, angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="97313-118">In any case, the client user must have the appropriate [**Launch**](../com/launchpermission.md) and [**Access Permissions**](../com/accesspermission.md) that are specified by the application running on the server.</span></span> <span data-ttu-id="97313-119">Weitere Informationen finden Sie [unter Sicherheit in com](../com/security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="97313-119">For more information see [Security in COM](../com/security-in-com.md).</span></span>

 

<span data-ttu-id="97313-120">Weitere Informationen über vom System bereitgestellte Moniker und Moniker und Aktivierungs Modi finden Sie in der com-Dokumentation des Platform Software Development Kit (SDK) unter [Moniker](../com/monikers.md), [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) Interface und [AppID Key](/windows/desktop/com/appid-key) .</span><span class="sxs-lookup"><span data-stu-id="97313-120">For more information about system-supplied monikers and monikers and activation modes, see [Monikers](../com/monikers.md), the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface, and [AppId Key](/windows/desktop/com/appid-key) in the COM documentation in the Platform Software Development Kit (SDK).</span></span>

 

 