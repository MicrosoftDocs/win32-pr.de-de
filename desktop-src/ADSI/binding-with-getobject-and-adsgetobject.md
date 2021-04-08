---
title: Binden mit GetObject und ADsGetObject
description: Die Funktionen "GetObject" und "ADsGetObject" werden zum Binden an Verzeichnisdienst Objekte ohne Authentifizierung verwendet.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, Bindung mit GetObject und ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949102"
---
# <a name="binding-with-getobject-and-adsgetobject"></a><span data-ttu-id="0b59b-104">Binden mit GetObject und ADsGetObject</span><span class="sxs-lookup"><span data-stu-id="0b59b-104">Binding With GetObject and ADsGetObject</span></span>

<span data-ttu-id="0b59b-105">Die Funktionen " **GetObject** " und " [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) " werden zum Binden an Verzeichnisdienst Objekte ohne Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b59b-105">The **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) functions are used to bind to directory service objects with no authentication.</span></span> <span data-ttu-id="0b59b-106">Die Anwendung muss beim Zugriff auf die Verzeichnisdienst Daten keine Anmelde Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0b59b-106">The application is not required to provide credentials when accessing directory service data.</span></span> <span data-ttu-id="0b59b-107">ADSI verwendet den Sicherheitskontext des aufrufenden Threads.</span><span class="sxs-lookup"><span data-stu-id="0b59b-107">ADSI uses the security context of the calling thread.</span></span> <span data-ttu-id="0b59b-108">Wenn die sichere Authentifizierung jedoch fehlschlägt, versucht ADSI, eine einfache Bindung mit einem NULL-Benutzernamen und einem NULL-Kennwort auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0b59b-108">However, if secure authentication fails, ADSI attempts to perform a simple bind with a null user name and null password.</span></span> <span data-ttu-id="0b59b-109">Wenn die einfache Bindung erfolgreich ist, ist der Benutzer Kontext für die Bindung Guest.</span><span class="sxs-lookup"><span data-stu-id="0b59b-109">If the simple bind succeeds, the user context for the binding is Guest.</span></span> <span data-ttu-id="0b59b-110">Eine einfache Bindung verwendet Klartext-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="0b59b-110">A simple bind uses plaintext authentication.</span></span> <span data-ttu-id="0b59b-111">Da kein Benutzername oder Kennwort über das Netzwerk übertragen wird, ist dies kein Sicherheitsproblem.</span><span class="sxs-lookup"><span data-stu-id="0b59b-111">Because no user name or password is transmitted over the network, this is not a security issue.</span></span>

<span data-ttu-id="0b59b-112">Die **GetObject** -Funktion wird zum Binden an Verzeichnisdienst Objekte in Sprachen verwendet, die Automation unterstützen, z. b. Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0b59b-112">The **GetObject** function is used to bind to directory service objects in languages that support automation, such as Visual Basic.</span></span> <span data-ttu-id="0b59b-113">Die **GetObject** -Funktion erfordert eine Monikerzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0b59b-113">The **GetObject** function requires a moniker string.</span></span> <span data-ttu-id="0b59b-114">In ADSI ist die Bindungs Zeichenfolge die Monikerzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0b59b-114">In ADSI, the binding string is the moniker string.</span></span>

<span data-ttu-id="0b59b-115">In Sprachen, die Automation nicht direkt unterstützen, wie z. b. C oder C++, stellt ADSI die [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) -Funktion für die Bindung an Verzeichnisdienst Objekte bereit.</span><span class="sxs-lookup"><span data-stu-id="0b59b-115">In languages that do not directly support automation, such as C or C++, ADSI provides the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to directory service objects.</span></span> <span data-ttu-id="0b59b-116">Alternativ können die Funktionen " [**mktisedisplayname**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) " und " [**mkparamesedisplaynameex**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) " verwendet werden, um das gleiche Ergebnis wie " **GetObject**" zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="0b59b-116">Alternatively, the [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) and [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) functions can be used to achieve the same result as **GetObject**.</span></span>

<span data-ttu-id="0b59b-117">Für einen Dienst, der unter dem Konto "LocalSystem" ausgeführt wird, hängt der von **GetObject** und [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) verwendete Sicherheitskontext von dem Computer ab, auf dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b59b-117">For a service running under the LocalSystem account, the security context used by **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depends on the computer on which the service is running.</span></span> <span data-ttu-id="0b59b-118">Wenn der Dienst auf einem Domänen Controller als "LocalSystem" ausgeführt wird, verfügt der Dienst über vollständigen Zugriff auf die Systemebene auf Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0b59b-118">If the service is running as LocalSystem on a domain controller, the service has full system-level access to Active Directory.</span></span> <span data-ttu-id="0b59b-119">Wenn der Dienst nicht auf einem Domänen Controller ausgeführt wird, verfügt der Dienst über die Zugriffsrechte und-Berechtigungen, die dem Computer Konto für den Computer gewährt werden, auf dem der Dienst ausgeführt wird. Dies ist erheblich weniger leistungsfähiger als der Zugriff auf Systemebene.</span><span class="sxs-lookup"><span data-stu-id="0b59b-119">If the service is not running on a DC, the service has the access rights and privileges granted to the computer account for the computer on which the service is running; this is significantly less powerful than system-level access.</span></span>

## <a name="examples"></a><span data-ttu-id="0b59b-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b59b-120">Examples</span></span>

<span data-ttu-id="0b59b-121">Im folgenden Visual Basic Codebeispiel wird gezeigt, wie die **GetObject** -Funktion verwendet wird, um eine Bindung an ein-Objekt herzustellen.</span><span class="sxs-lookup"><span data-stu-id="0b59b-121">The following Visual Basic code example shows how to use the **GetObject** function to bind to an object.</span></span>


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



<span data-ttu-id="0b59b-122">Im folgenden C++-Codebeispiel wird gezeigt, wie die [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) -Funktion verwendet wird, um eine Bindung an ein-Objekt herzustellen.</span><span class="sxs-lookup"><span data-stu-id="0b59b-122">The following C++ code example shows how to use the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to an object.</span></span>


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 